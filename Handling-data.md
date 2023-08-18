---
title: Handling data
---
## Storing and manipulating your data.

CogStat is designed not to edit data, but only to run the statistical analysis. You must store and edit your data in other software package, and import your data to CogStat.

* One option to store and edit the data is to use a **spreadsheet program** (e.g., [LibreOffice Calc](http://www.libreoffice.org/) or Microsoft Excel), where basic analyses and data manipulations can also be performed. Spreadsheet packages are very powerful for data manipulation and they are also surprisingly appropriate for simple (and sometimes for more complex) statistical analysis.
* Also, you can use various **statistical packages** to manipulate your data and store it in various file formats. This can be ideal if you mainly use other statistical software, but want to use the analyses available in CogStat to make your work more efficient and precise.

## Key features of the imported data

In CogStat, variables have three key properties that have to be set: **their names**, **their measurement levels**, and obviously, **the data values** themselves.

**Technical constraints of variable names and data values**

Only English letters, numbers and underscore characters are supported at the moment in variable names and in values. Other characters may work in some cases, but it is better to avoid those other characters in your data because, in some cases, CogStat may not be able to run the analysis.

**Measurement levels**

Like in any other statistical software, variables can be nominal, ordinal and interval. (If you have ratio data, then handle it as an interval variable.)

In CogStat, it is essential to set the measurement levels because automatic data processing heavily relies on that information to decide what analyses to run.

In some software packages, you cannot set the measurement levels, and this information will not be available when you import your data. See below how CogStat will handle your data when measurement level is not available. If this causes an issue, use any other software that can handle measurement level to store with your data.

CogStat handles string variables as nominal, even if other measurement level was set in your data source. So string variables will be set to nominal, no matter what measurement level was given formerly.

If measurement level is not available, it will be set as `unk` (unkown), and for convenience reasons, in most analyses, it will be handled as interval variable. If this is not your intention, then the measurement level should be set.

## Available file formats

CogStat can import data from several file formats.

- File formats where measurement level should be set in a separate second row:
    - **Excel spreadsheet .xls and .xlsx files**
        - If there are multiple sheets in your file, the first sheet will be imported.
    - **OpenDocument Spreadsheet .ods files**
        - If there are multiple sheets in your file, the first sheet will be imported.
    - **Text .csv, .txt, tsv., .dat, and .log files**
       - If you save it from your spreadsheet, make sure that the measurement level row is included (see below). If you save it from other software (e.g., SPSS), then the measurement level will not be included,therefore, we do not recommend this file format.
- File formats where the measurement level can be set in the software and can be saved in the file format:
    - **SPSS .sav, .zsav, and .por files**
    - **JASP .jasp files**
    - **jamovi .omv files**
    - Since CogStat relies on the measurement level of the variables to decide which analyses to run, it is essential to set the measurement levels of the variables and save them before loading the data file to CogStat.
- File formats where the measurement level is not available:
    - **R .rdata, .rds, and .rda files**
    - **SAS .sas7bdat and .xpt files**
    - **STATA .dta files**
    - Since CogStat relies on the measurement level of the variables to decide which analyses to run and this information is not available in those file formats, it is not recommended to use these file formats unless it is still a better option for you than the other file formats.


Note that data of any other software can be imported into CogStat, when the data can be exported to any of these formats.

Note that various file formats have their limitations, such as how long the variable names can be, or whether measurement level is stored in the file.

### How should the data look like in your spreadsheet software?

For example, 

id|	Gender|	IQ 
---|---|---
nom|	nom|	int
lcf|	1|	96 
gok|	1|	121 
tf|	2|	118
trs|	1|	128
rs|	2|	99 

* Like in any statistical software, rows should be the cases, and columns should be the variables.
* First row should include the names.
   * Variables with missing names will be named by CogStat as Unnamed: 0, Unnamed: 1, etc.
   * If you forget to include the whole variable names row, the entire first row (first case in your data) will be handled by CogStat (erroneously) as names.
   * Different variables cannot have the same names. If variables with the same names are found, then variables with a name already in use will be renamed by CogStat.
* Second row includes the [measurement level of the variables](https://en.wikipedia.org/wiki/Level_of_measurement#Stevens's_typology).
    * Use `nom`, `ord` and `int` for nominal, ordinal and interval variables. If any other word is in that row, then CogStat considers the row as values, and measurement levels will not be recognized.
    * When you display your data in CogStat, a `Type` row (including `num `and `str` types) are shown, these types should *not* be added to the spreadsheet file. The type row will be detected automatically when you import your data.
* All other rows include values of the data.
    * For missing value, leave the cell empty, or write `nan`. (Note that many other common values will be imported as missing value, for example, `NA`, `<NA>`, `n/a`, etc.) New in v2.3: Error messages of the spreadsheet software in a cell when starting with `#` sign and ending with `!` sign (e.g., `#VALUE!`, `#DIV/0!`) will be handled by CogStat as missing value too. New in v2.4: Error messages of the spreadsheet software in a cell when starting with the `Err:` (e.g., `Err:502`) will be handled by CogStat as missing value, too.

## How to import your data?

There are two possibilities to import your data to CogStat:

* Open your file
    * by using the `Data > Open data file...` (or the `Data > Open demo data file...`) menu, 
    * or by dragging and dropping your file to the CogStat window.
    * (New in v2.4) If you change your source file and save it, you can simply reload your active data file with the `Data > Reload actual data file` command. After reloading the data, you can easily [rerun the analyses](Common-elements-of-the-analysis-results#rerun-the-analyses) seen in the Results pane.
* If you use a spreadsheet software, you can copy and paste your data.
    * Precision of the copied data depend on how the numbers were displayed in the spreadsheet, so change it according to your need. CogStat handles precision automatically after importing the data, e.g., means are displayed with the precision of the raw data.
    * The decimal separator should be dot (i.e., [not comma, or other signs](https://en.wikipedia.org/wiki/Decimal_separator#/media/File:DecimalSeparator.svg)). If your spreadsheet software uses other separator than dot, change your settings to modify the separator (see how to do it in [MicroSoft Office Excel](https://support.office.com/en-us/article/change-the-character-used-to-separate-thousands-or-decimals-c093b545-71cb-4903-b205-aebb9837bd1e) or in [LibreOffice Calc](https://help.libreoffice.org/Common/Languages)).
    * Note that other statistical software will copy only the selected data, but not the variable names and measurement levels, so copy-and-paste method is usable only with spreadsheet software.

After the data is opened, you'll see the first few cases in the Results pane, and (new in v2.4) the Data view on the left side will display all cases.

CogStat can store only a single datasheet: When you import a new data, the previous one will not be available anymore (until you import the previous one again). If you want to work on several datasets at the same time, open CogStat several times, and different datasets can be used.
