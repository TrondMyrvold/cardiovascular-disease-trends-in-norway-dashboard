// This README shows how the DAX measurements was created in Power BI. (View in "Code")

// Total Patients Measurement

Total Patients = 
SUM('Sheet1'[total patients1])

-----------------------------------------------------------------

// Previous Year Measurement

Previous Year Patients = 
CALCULATE(
    [Total Patients],
    FILTER(
        ALL('Sheet1'[Year]),
        'Sheet1'[Year] = MAX('Sheet1'[Year]) - 1
    )
)

-----------------------------------------------------------------

// Yearly Change Measurement

Yearly Change = 
IF(
    HASONEVALUE('Sheet1'[Year]),
    DIVIDE([YoY Change], [Previous Year Patients]),
    BLANK()
)

-----------------------------------------------------------------

// Growth Measurement

Growth % = 
VAR StartYear =
    IF(
        HASONEVALUE('Sheet1'[Year]),
        MAX('Sheet1'[Year]) - 1,
        2021
    )
VAR EndYear =
    IF(
        HASONEVALUE('Sheet1'[Year]),
        MAX('Sheet1'[Year]),
        2025
    )
VAR StartValue =
    CALCULATE(
        [Total Patients],
        ALL('Sheet1'[Year]),
        'Sheet1'[Year] = StartYear
    )
VAR EndValue =
    CALCULATE(
        [Total Patients],
        ALL('Sheet1'[Year]),
        'Sheet1'[Year] = EndYear
    )
RETURN
DIVIDE(EndValue - StartValue, StartValue)

-----------------------------------------------------------------

// Most Common Diagnosis Measurement

Most Common Diagnosis = 
VAR TopDiagnosis =
    TOPN(
        1,
        FILTER(
            ALLSELECTED('Sheet1'),
            'Sheet1'[Diagnosis Group] <> "Pasienter totalt"
                && 'Sheet1'[Diagnosis Group] <> "Hjerte- og karsykdommer (I00-I99)"
        ),
        [Total Patients],
        DESC
    )
RETURN
MAXX(
    TopDiagnosis,
    'Sheet1'[Diagnosis Group]
)

-----------------------------------------------------------------

// Fastest Growing Diagnosis Measurement

Fastest Growing Diagnosis = 
VAR TopDiagnosis =
    TOPN(
        1,
        FILTER(
            ALLSELECTED('Sheet1'[Diagnosis Group]),
            'Sheet1'[Diagnosis Group] <> "Pasienter totalt"
                && 'Sheet1'[Diagnosis Group] <> "Hjerte- og karsykdommer (I00-I99)"
        ),
        [Growth %],
        DESC
    )
RETURN
MAXX(
    TopDiagnosis,
    'Sheet1'[Diagnosis Group]
)

-----------------------------------------------------------------

// Largest Growth Measurement

Largest Growth = 
VAR TopDiagnosis =
    TOPN(
        1,
        FILTER(
            ALLSELECTED('Sheet1'[Diagnosis Group]),
            'Sheet1'[Diagnosis Group] <> "Pasienter totalt"
                && 'Sheet1'[Diagnosis Group] <> "Hjerte- og karsykdommer (I00-I99)"
        ),
        [Growth %],
        DESC
    )
RETURN
MAXX(
    TopDiagnosis,
    [Growth %]
)


