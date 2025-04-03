[Skip to main content](#main-content-wrapper)

**Rotorua office temporarily closed** | Our Rotorua office will be closed from 12pm 17 January 2025 until 30 January 2025. For anything urgent, you can call our contact centre.

[Search tips](/about-this-site/search-tips)

myIR error information and help
===============================

If something goes wrong when you’re filing or amending employment information or employee details in myIR we’ll tell you with an error message on screen.

If you’re using file upload or express file transfer, you can choose to correct errors by changing your file or, you can correct the errors on screen in myIR.

Viewing error information for uploaded files
--------------------------------------------

If there are errors on a file you've uploaded, you'll get an error notification.

For information about errors, select 'View and export error report'.

![Error alert showing in myIR for uploaded file "We have found errors in your file".](/-/media/project/ir/home/graphics/employing-staff/payday-filing/filing-employment-information-electronically/myir-errors/p1.png?modified=20210820001840)

The report tells you the error line locations and details. You can choose to export this information to a CSV file if you have multiple errors.

![Error information - "A tax code must be provided".](/-/media/project/ir/home/graphics/employing-staff/payday-filing/filing-employment-information-electronically/myir-errors/p2.png?modified=20210820001908)

There are 2 ways of clearing errors - edit directly in myIR or change the file and upload or transfer it again.

### Edit in myIR to clear errors

To correct errors in myIR, select 'Edit' and follow the error message link in myIR.

![Error notification showing next to the relevant employee line item.](/-/media/project/ir/home/graphics/employing-staff/payday-filing/filing-employment-information-electronically/myir-errors/p4.png?modified=20210820002006)

### Edit your file to clear errors and upload the file again

You can correct errors in your file using a text editor such as Notepad. Notepad is free and comes installed on all windows-based computers. Do not open with Excel as this will cause structural errors in the file.

Structural errors
-----------------

Structural errors indicate problems with the file, for example too many columns.

They can be caused by:

*   opening the file using Excel. Excel’s automatic formatting features will change date formats and add commas. If you need to edit the file, please use a text editor such as Notepad which is free and comes installed on all Windows-based computers.
*   adding commas in any field including the name field, for example adding a comma between an employee’s last name, first name.

Show all

File formats and fields

### Employment information (EI) list of fields and example file

#### Header (line 1)

| Field | Description |
| --- | --- |
| 1   | Header record indicator (HEI2) |
| 2   | Employer IRD number / Account ID |
| 3   | Pay date |
| 4   | Final return for employer |
| 5   | Nil return indicator |
| 6   | PAYE intermediary IRD number |
| 7   | Name of payroll contact person |
| 8   | Payroll contact work phone number |
| 9   | Email of payroll contact person |
| 10  | Total employee lines |
| 11  | Total gross earnings |
| 12  | Total prior period gross adjustments |
| 13  | Total earnings not liable for ACC Earners' levy |
| 14  | Total PAYE/tax |
| 15  | Total prior period PAYE adjustment |
| 16  | Total child support deductions |
| 17  | Total student loan deductions |
| 18  | total SLCIR deductions |
| 19  | Total SLBOR deductions |
| 20  | Total KiwiSaver deductions |
| 21  | Total net KiwiSaver employer contributions |
| 22  | Total ESCT deducted |
| 23  | Total amounts deducted |
| 24  | Total tax credits for payroll donations |
| 25  | Total family tax credits |
| 26  | Total employee Share Scheme |
| 27  | Payroll package and version identifier |
| 28  | IR form version number |

### **Employee information (line 2+)**

| Field | Description |
| --- | --- |
| 1   | File type (DEI) |
| 2   | Employee IRD no |
| 3   | Employee name |
| 4   | Tax code |
| 5   | Employment start date |
| 6   | Employment finish date |
| 7   | Employee pay period start date |
| 8   | Employee pay period end date |
| 9   | Employee pay cycle |
| 10  | Hours paid |
| 11  | Gross earnings and/or schedular payments |
| 12  | Prior period gross adjustments |
| 13  | Earnings and/or schedular payments not liable for ACC earner’s levy |
| 14  | Lump sum (extra pay) indicator |
| 15  | PAYE/tax |
| 16  | Prior period PAYE adjustments |
| 17  | Child support deductions |
| 18  | Child support code |
| 19  | Student loan deductions |
| 20  | SLCIR deductions |
| 21  | SLBOR deductions |
| 22  | KiwiSaver deductions |
| 23  | Net KiwiSaver employer contributions |
| 24  | ESCT deducted |
| 25  | Tax credits for payroll donations |
| 26  | Family tax credits |
| 27  | Employee share scheme |

| Employment information sample file |
| --- |
| HEI2,888888888,20210604,N,N,,Bill Smith,041234567,[\[email protected\]](/cdn-cgi/l/email-protection)<br>,4,143257,5000,2000,47024,40,0,16671,0,5750,85500,83660,2560,147100,2500,0,22500, |
| vendor\_package\_v1.0,0001 |
| DEI,111111111,Brown John,M,,,20210524,20210604,WK,3050,56875,0,0,0,34687,0,60000,0,0,0,4550,3565,756,0,0,0 |
| DEI,074444444,Cork Chelsea,M,,,20210524,20210604,WK,3750,65725,0,0,0,45695,0,0,,0,0,0,0,0,0,100,0,0 |
| DEI,075555555,French Carol,M SL,,,20210524,20210604,WK,2500,45678,2567,0,0,32785,1456,0,,2687,0,0,0,0,0,0,0,0 |

### Employment information amendment (EIA) list of fields and example files

#### **File format for amending returns filed before April 2021 (EIA)**

##### **Header (line 1)**

| Field | Description |
| --- | --- |
| 1   | Header record indicator EIA |
| 2   | Employer IRD number/account ID |
| 3   | Pay date |
| 4   | PAYE intermediary IRD number |
| 5   | Name of the payroll contact person |
| 6   | Payroll contact work phone number |
| 7   | IR form version number |

##### **Employee information (line 2+)**

| Field | Description |
| --- | --- |
| 1   | File type |
| 2   | Employee IRD number |
| 3   | Employee name |
| 4   | Employee tax code |
| 5   | Employment start date |
| 6   | Employment finish date |
| 7   | Employee pay period start date |
| 8   | Employee pay period end date |
| 9   | Employee pay cycle |
| 10  | Gross earnings and/or schedular payments |
| 11  | Earnings and/or schedular payments not liable for ACC earners' Levy |
| 12  | Lump sum (extra pay) indicator |
| 13  | PAYE/tax |
| 14  | Child support deductions |
| 15  | Child support code |
| 16  | Student loan deductions |
| 17  | KiwiSaver Deductions |
| 18  | Net KiwiSaver employer contributions |
| 19  | ESCT deducted |
| 20  | Tax credits for payroll donations |
| 21  | Family tax credits |

#### File format for amending returns filed from April 2021 (EIA2)

##### **Header (Line 1)**

| Field | Description |
| --- | --- |
| 1   | Header record indicator EIA2 |
| 2   | Employer IRD number/account ID |
| 3   | Pay date |
| 4   | PAYE intermediary IRD number |
| 5   | Name of the payroll contact person |
| 6   | Payroll contact work phone number |
| 7   | IR form version number |

##### **Employee info (Line 2+)**

| Field | Description |
| --- | --- |
| 1   | File type |
| 2   | Employee IRD number |
| 3   | Employee name |
| 4   | Employee tax code |
| 5   | Employment start date |
| 6   | Employment finish date |
| 7   | Employee pay period start date |
| 8   | Employee pay period end date |
| 9   | Employee pay cycle |
| 10  | Hours paid |
| 11  | Gross earnings and/or schedular payments |
| 12  | Prior period gross adjustments |
| 13  | Earnings and/or schedular payments not liable for ACC earners' Levy |
| 14  | Lump sum (extra pay) indicator |
| 15  | PAYE/tax |
| 16  | Prior period PAYE adjustments |
| 17  | Child support deductions |
| 18  | Child support code |
| 19  | Student loan deductions |
| 20  | SLCIR deductions |
| 21  | SLBOR deductions |
| 22  | KiwiSaver Deductions |
| 23  | Net KiwiSaver employer contributions |
| 24  | ESCT deducted |
| 25  | Tax credits for payroll donations |
| 26  | Family tax credits |
| 27  | Employee Share Scheme |

| Employment information amendment sample file |
| --- |
| EIA2,888888888,20210604,,Bill Smith,0912354321,0001DTI,111111111,Brown John,M,,,20210524,20210604,WK,3050,56875,0,0,0,34687, |
| 0,0,,0,0,0,4550,3565,756,0,0,0 |
| DAI,111111111,Brown John,M,,,20210524,20210604,WK,3050,56785,0,0,0,34687,0,0,,0,0,0,4550,3565,756,0,0,0 |

### Employee details list of fields and example file (ED) (includes KiwiSaver)

#### **Header (Line 1)**

| Field | Description |
| --- | --- |
| 1   | Header record indicator |
| 2   | Employer IRD number |
| 3   | Payroll package and version no. identifier |
| 4   | Total employee lines |

#### **Employee details (Line 2+)**

| Field | Description |
| --- | --- |
| 1   | Detail record indicator |
| 2   | Employee IRD # |
| 3   | Employee Name/ID on EI return |
| 4   | Employee title |
| 5   | Employee first name |
| 6   | Employee middle name |
| 7   | Employee last name |
| 8   | Date of birth |
| 9   | Employment start date |
| 10  | Employment end date |
| 11  | KiwiSaver eligibility |
| 12  | New employee KiwiSaver status |
| 13  | Employee exempt income |
| 14  | Email address |
| 15  | Mobile phone country |
| 16  | Mobile phone number |
| 17  | Mobile extension |
| 18  | Daytime phone country |
| 19  | Daytime phone number |
| 20  | Daytime phone extension |
| 21  | Country |
| 22  | Unit type |
| 23  | Unit number |
| 24  | Floor type |
| 25  | Floor number |
| 26  | Building |
| 27  | Street address |
| 28  | Suburb/rural |
| 29  | City |
| 30  | Post code |
| 31  | State |
| 32  | Employee opted-out from KiwiSaver |
| 33  | Employee’s bank account – bank |
| 34  | Employee’s bank account – branch |
| 35  | Employee’s bank account – account |
| 36  | Employee’s bank account – suffix |
| 37  | Employee’s bank account – reference number |
| 38  | Name of account holder |
| 39  | Date opt-out notice signed by the employee |
| 40  | Late opt-out reason |
| 41  | Other late opt-out reason |

| Employee details sample file |
| --- |
| HED2,88888888,SoftwarePlatform,2 |
| DED,123018635,Smith Mary,Mrs,Mary,,Smith,19850614,20191015,,NE,AK,,[\[email protected\]](/cdn-cgi/l/email-protection)<br>,NZL,021123456,,,,,NZL,,,,,, |
| 12 Small Street,,Springfield,6881,,N ,,,,,,,,, |
| DED,000000000,Hall Brian,Mr,Brian,Jack,Hall,19550308,20191015,,NE,CT ,,,,,,NZL,041234567,,NZL,,,,,, |
| 23 Tall Road,,Huttville,6547,,Y,08,0456,0123456,0025,,Brian J Hall,20191031,, |

Errors and solutions
--------------------

Show all

Amending employment information file errors

| Error | Solution |
| --- | --- |
| No filing exists for <IRD number> and tax code <code> for filing period <date> | If you’re adding an employee in an employment information amendment file you must include a DTI line followed by the DAI with the employee’s details (EIA or EIA2).  <br>  <br>**Example**  <br>  <br>DTI,,,,,,,,,0,0,0,0,0,0,0,0,,0,0,0,0,0,0,0,0,0  <br>DAI,111111111,Brown John,M,,,20210519,20210602,WK... |
| All DAI records must be preceded by a DTI record | The employment amendment file is missing the DTI record. Please insert the correct information before uploading.  <br>  <br>The DTI record is the information included in the return already filed. The DAI information is the amended information for that record. |
| You cannot file for <DD-MMM-CCYY> as the initial filing has not been made | You cannot amend this pay day period as no employment information return has been filed. Check the amended file is for the right period and pay date and change if required. If the dates are correct, upload an Employment information file instead. |
| You are unable to amend a return for IRD number <field> and filing period with this version of the file | Check if the pay period is missing from the return. Add a pay period using the format CCYYMMDD. For example, 30 May 2021 is entered as 20210530. |
| You are unable to amend to an empty employee IRD number | Make sure there is an IRD number in the DAI line.<br><br>If the employee cannot give you their IRD number enter 000-000-000 in the employee’s IRD number field and update the employee’s tax code to ND (non-notified rate). |

Amounts and number value errors

| Error | Solution |
| --- | --- |
| <field> contains a decimal point | Do not include decimal points. For example, 37.5 hours worked is entered as 3750. A deduction of $3.50 is entered as 350. |
| Please enter a value in <field> | Enter an amount or 0 for nil. |
| Header amount <field> must be equal to the sum of total amounts <field> | The employees’ combined figures for gross, PAYE and other deductions must balance with the field totals shown in the header. |
| The total amount payable for the employee is greater than the gross earnings | Check the amount entered for gross earnings. The sum of the employee’s PAYE and other deductions must be less than the gross amount. |
| <field> <amount> cannot be greater than gross earnings <amount><br><br>* * *<br><br><field> <amount> cannot be more than gross income <amount> | The amount in this field cannot be more than gross earnings. |
| PAYE has been deducted where the employee has no gross earnings | Check the gross earnings and PAYE amounts are correct. |
| Lump sum indicator has too many characters<br><br>* * *<br><br>Lump sum indicator is incorrect, found <field>. It must be 0 for “no” or 1 for “yes” | If a lump sum is being paid, the indicator is 1, else 0. |
| The total amount payable less child support deduction for the employee <amount> is greater than the gross earnings <amount> | Check the gross earnings and child support deduction amounts are correct. |
| Tax credits for payroll donations found <amount> cannot be greater than PAYE and/or tax on Schedular payments found <amount><br><br>* * *<br><br>Tax credits for payroll donations cannot be greater than PAYE and/or tax on schedular payments | Payroll donations must be less than the employee’ PAYE/tax amount. |
| The total amount payable for the employee is greater than the gross earnings | PAYE cannot be more than the employee’s gross earnings. |
| A negative number has been entered<br><br>* * *<br><br><field> cannot be negative<br><br>* * *<br><br>The top line of the schedule contains a field with a negative number | All field values must be positive. You cannot enter negative numbers.<br><br>If you need to make a downward adjustment for amounts already paid, please send an employer amendment file (EIA). |
| Number of employee entries does not match count specified in the header | Check the number of employees included in your file matches the number shown in the header line 1. Do not include line 1 in your count. |
| <field> is an invalid number value<br><br>* * *<br><br>A number field contains a character other than 0 – 9 for hours paid<br><br>* * *<br><br><field> contains an invalid character in a number only field | This is a number only field. Do not use commas letters or other special characters in a numeric field. |

Child support errors

| Error | Solution |
| --- | --- |
| The Child Support validation code entered <field> is not correct. It should be A,C,D,O,P,S or blank. | Enter the correct code corresponding to the employee’s circumstances.<br><br>**Child support codes**<br><br>*   A - Advanced payment<br>*   C - Ceased employment<br>*   D - Deducted previously<br>*   O - Other<br>*   P - Protected earnings<br>*   S - Short-term absence |

Date errors (period, pay day, start, end, birth dates)

| Error | Solution |
| --- | --- |
| Pay day period is required | Enter the pay day for the period. |
| The pay date period is required | Add a pay day period using the format CCYYMMDD. For example 30 May 2021 is shown as 20210530 (file upload/express file transfers). |
| You are not able to file for <DD-MMM-CCYY><br><br>* * *<br><br>You are not able to file within this pay day period<br><br>* * *<br><br>You cannot file for <DD-MMM-CCYY> | You can only file for periods already showing as available in myIR. Change the filing period if the wrong date has been used.<br><br>If you’re filing for a period before your employer registration started or you need to file a return ahead of time, please send a message from myIR to let us know so we can open the right period. |
| You are not able to file for <date> payday filing is required | You cannot commence pay day filing part way through a month. Pay day filing must start with the very first pay day in the month. |
| The start date is invalid. Start date must be valid with the format CCYYMMDD, ie. 24/05/2021 is 20210524 | Check date fields are in the correct format without spaces or separators. |
| The filing period from your file <field> is different from the filing period of this return <field> | Check the file you are uploading is for the right period and the filing period date matches the period. |
| The return end date is incorrect. It must be the last day of the period month and the format must be CCYYMMDD, ie. 31/05/2021 is 20210531. | Update the correct filing period date. |
| You must enter a date for the beginning of the employee’s pay period | Add the start date for the pay period. The date must be before pay period end date. |
| You must enter a date for the end of the employees pay period | Add the end date for the pay period. The date must be after pay period start date. |
| Start date not provided for the employee | Add the date this employee started working for you |
| Employee finish date may not be before employee start date | Finish date must be on or after the start date |
| <field> is an invalid date value | Date format must be CCYYMMDD. For example 30 May 2021 is shown as 20210530 |
| Employee date of birth cannot be in the future | Check the date of birth is correct. This is not a required field and can be left blank if date is not provided. |
| Return is time-barred | Amendments are prevented because the return was originally filed more than 4 years ago. |

Email and address errors

| Error | Solution |
| --- | --- |
| Invalid email | The email address format must be <username>@<domain>, for example [\[email protected\]](/cdn-cgi/l/email-protection) |
| Employee mailing address line 1 must be provided<br><br>* * *<br><br>Employee mailing address line 2 must be provided | If your adding the employee’s address information, both address lines must be completed. |
| <field> is not an allowed unit type for specified country<br><br>* * *<br><br>Emp unit num is too long. Maximum length is 10. | Enter a valid unit type for the employee’s country. |
| Emp floor type is too long. Maximum length is 30 | Check the floor type is correct. |
| Emp floor number is too long. Maximum length is 30 | Check the floor number is correct. |
| Emp suburb/rural is too long. Maximum length is 60 | Check the suburb/rural name is correct. |
| Emp city <name> is too long. Maximum length is 100 | Check the city name is correct. |
| Emp post code <code> is too long. Maximum length is 30 | Check the post code is correct. |
| <field> is not a recognised ISO3A state value for country <field> | Do not add a state for employees living in New Zealand.<br><br>For employee addresses from a country where a state is required, enter the ISO code in the correct format (ISO Alpha-2 country code first then the subdivision code). For example, the ISO code for Colorado in USA is US-CO).<br><br>If there is no state, leave the field blank.<br><br>Find the correct codes on the ISO Online Browsing Platform. Select the relevant country to find the subdivision codes.<br><br>[ISO Online Browsing Platform](https://www.iso.org/obp/ui/) |
| <field> is not a recognised ISO2A country value | For employee addresses in another country, enter the ISO code in the correct format.<br><br>Find the correct country code on the ISO Online Browsing Platform.<br><br>[ISO Online Browsing Platform](https://www.iso.org/obp/ui/) |
| Employee country code is required if no employee email, mobile phone number or daytime phone number is provided. | Add the employee’s country code.<br><br>Find the correct country code on the ISO Online Browsing Platform.<br><br>[ISO Online Browsing Platform](https://www.iso.org/obp/ui/) |
| EMP country <field> is too long. Maximum length is 3 | Check employee’s country code is correct.<br><br>Find the correct country code on the ISO Online Browsing Platform.<br><br>[ISO Online Browsing Platform](https://www.iso.org/obp/ui/) |

File errors

| Error | Solution |
| --- | --- |
| File extension is not allowed | Your file needs to be in either CSV (.csv) or TXT (.txt) format. If your software provides a file in a different format, you will need to change this before you can upload the file.<br><br>You can send us multiple CSV or TXT files at a time, using one of the following archive file extensions:<br><br>*   .gz<br>*   .gzip<br>*   .tar<br>*   .zip |
| A submission with the attachment has already been submitted | The file has already been uploaded. If you need to upload the file again, open the file with a text editor (such as notepad), add a space to the contact person and save. This changes the data and will allow a new submission. |
| Line is too long | There are more than 27 fields of information per employee line. Fields are separated by commas.<br><br>Generate the file again and upload without opening it in a spreadsheet editor (such as Excel). If you need to edit the file, use a text file editor (such as notepad).<br><br>Refer to the ‘File formats and fields’ lists for more information about the number and order of fields for each file type. |
| Invalid header record supplied in the uploaded file<br><br>* * *<br><br>Header record not found | The file must contain a valid header record for the file type being uploaded.<br><br>*   HEI2 for employee information (EI) files.<br>*   EIA2 for employment information amendments to EI returns filed on or after 1 April 2021.<br>*   EIA for employment information amendments to EI returns filed before 1 April 2021.<br>*   HED2 for employee detail (ED) files.<br><br>Refer to the ‘File formats and fields’ lists for more information about the number and order of fields for each file type. |
| There is an incorrect number of fields in the line | Check the following.<br><br>*   Make sure the file has a maximum of 27 fields. Generate the file again and upload without opening it using Excel. Refer to the ‘Employee information (EI) list of fields and example file’ under ‘File formats and fields’ for more information.<br>*   Look for a line record indicator with no employee details after it. Delete the line if no details to add or update the required information. |
| You have an empty line in your file. Please delete this line. | Your file should not have any lines with no details. Check your file and delete any blank lines.<br><br>**Example**<br><br>HEI2,042711462,20210604,N,N,,Bill…  <br>DEI,111111111,Brown John,M,…  <br><Delete this blank line>  <br>DEI,074444444,Cork Chelsea,M,… |
| You are missing columns. | Check you have the correct number of columns in the file.<br><br>Refer to the ‘File formats and fields’ lists for more information about the number and order of fields for each file type. |
| Invalid from version. Expecting ‘0001’ – Format: 9999<br><br>* * *<br><br><field> is an invalid form version. Expecting ‘0001’ | The version number must be 0001. |

Income exemption errors

| Error | Solution |
| --- | --- |
| <field> is not a valid income exemption<br><br>* * *<br><br>Employee exempt income <$> is too long, Maximum length is 6 | Enter a valid income exemption.<br><br>**Employee exempt income codes**<br><br>*   BLH - Provide board-lodging-use of a house or part house or equivalent allowance<br>*   HPT - Honoraria payments<br>*   OES - Overpayment of an amount of an employer’s superannuation cash contribution<br>*   RTA - Retiring allowance<br>*   TAO - Taxable allowances for accommodation and living costs overseas<br>*   VBS - Some payments under a voluntary bonding scheme and living costs overseas |

IRD number errors

| Error | Solution |
| --- | --- |
| The employer IRD number entered in the top line of the schedule is wrong<br><br>* * *<br><br>IRD number does not match employer IRD number. Format 999-999-999<br><br>* * *<br><br><IRD number> is not your IRD number<br><br>* * *<br><br>Employer IRD number does not match IRD for this account<br><br>* * *<br><br>Employer IRD does not associate to a valid EMP account<br><br>* * *<br><br>You have provided an incorrect IRD number in your file<br><br>* * *<br><br>The provided information was not specific enough to match with a single employment relationship | The employer IRD number in the file you’re uploading must match the IRD number of the myIR account your logged into. Either update the IRD number of the file or log into the correct myIR account. |
| <field> is not a valid PAYE intermediary IRD number. | Update a valid intermediary IRD number. |
| Not a valid IRD number – Format: 999-999-999<br><br>* * *<br><br><field> IRD number must be nine digits long<br><br>* * *<br><br>IRD number <field> is too long. Maximum length is 9<br><br>* * *<br><br><field> is not a valid IRD number | Enter a valid 9-digit IRD number for the required field |
| Incomplete – Format: 999-999-999<br><br>* * *<br><br>IRD number needs to be 9 digits | The employee’s IRD number is incomplete. Enter their 9-digit IRD number if you have it.<br><br>If the employee cannot give your their IRD number enter 000-000-000 in the employee’s IRD number field and update the employee’s tax code to ND (non-notified rate). |

KiwiSaver errors

| Error | Solution |
| --- | --- |
| You are not allowed to make KiwiSaver <field> with a WT tax code | WT tax code workers are treated as self-employed. Do not automatically enrol them for KiwiSaver or make KS deductions or employer contributions. |
| Employee opt out field must be “N” if employee eligibility is “EE” | Check you have the correct KiwiSaver eligibility code for this employee.<br><br>**KiwiSaver eligibility codes**<br><br>*   NE – New employee<br>*   EE – Existing employee<br>*   EA – Existing employee auto enrolled into KiwiSaver |
| <field> is not a valid KiwiSaver eligibility<br><br>* * *<br><br>Employee eligibility must be either "NE" or "EE" or "" | Enter a valid KiwiSaver eligibility code.<br><br>**KiwiSaver eligibility codes**<br><br>*   NE – New employee<br>*   EE – Existing employee<br>*   EA – Existing employee auto enrolled into KiwiSaver |
| KiwiSaver status is required for new employees<br><br>* * *<br><br><field> is not a valid KiwiSaver status value. | Enter a valid KiwiSaver status code.<br><br>**KiwiSaver status codes**<br><br>*   AK – Active KiwiSaver member<br>*   OK – Opting into KiwiSaver<br>*   NK – Not eligible for KiwiSaver<br>*   CT – Casual/temporary employee<br>*   AE – Auto-enrol |
| Emp KiwiSaver opt-out is too long. Maximum length is 1 | Opting out employees Y for yes.<br><br>Employees not opting out N (no). |
| Opt-out date is required to opt-out of KiwiSaver<br><br>* * *<br><br>The opt-out date of the employee must be provided if the opt-out indicator is ticked | Enter the date the opt-out form was signed by the employee. |
| Opt-out date must be blank | If the KiwiSaver opt-out indicator is N (no) date field must be blank. |
| Opt-out reason must be blank | If the KiwiSaver opt-out indicator is N (no) opt-out reason must be blank. |
| Opt-out reason is required when employee opted-out 56 days from employment<br><br>* * *<br><br><field> is not a valid opt-out reason | Enter a valid KiwiSaver late opt-out reason.<br><br>**KiwiSaver late opt-out reason codes**<br><br>*   INFO – Employer did not provide a KiwiSaver information pack within seven days of starting employment<br>*   IRIS – Inland Revenue did not send an investment statement upon allocation to a default scheme<br>*   ERIS – Employer did not provide an investment statement (for the employer chosen KiwiSaver scheme)<br>*   EVNT – Events outside of control meant the opt-out application was unable to be submitted within the eight-week time limit<br>*   CRIT – Did not meet the criteria to join KiwiSaver (refer to the Employee information pack (KS3) for criteria)<br>*   INER – Incorrectly enrolled under the age of 18<br>*   OTHR – Other reason (please explain) |
| An explanation is required when the opt out reason is ‘Other’ | You must include a late opt out reason if ‘Other’ has been selected. Please do not use commas as this will cause a structure error. |

Name errors

| Error | Solution |
| --- | --- |
| Payroll contact name: Required<br><br>* * *<br><br>Employer contact name is required<br><br>* * *<br><br>A contact name is required | Add a contact name.<br><br>Do not use commas or other special characters in the name field. Apostrophes are ok (for example, O‘Riley) |
| Contact name contains invalid characters | Do not use commas or other special characters in the name field. Apostrophes are ok (for example, O‘Riley) |
| Employer name <field> is too long. Maximum length is 20 | Employer name cannot exceed 20 characters. |
| Employee name is required<br><br>* * *<br><br>Employee name cannot be blank | Add employee’s name. Do not use commas in the name field. Apostrophes are ok (for example, O‘Riley) |
| Employee first name is required | Enter a first name |
| Employee last name is required | Enter a last name |
| Emp First Name <field> is too long. Maximum length is 50. | Employee first name cannot exceed 50 characters |
| Emp Last Name <field> is too long. Maximum length is 50. | Employee last name cannot exceed 50 characters |
| Employee name is too long. Max length is 255 | First last and middle names combined cannot exceed 255 characters |
| <field> is not an allowable title<br><br>* * *<br><br>Employee title must be one of “Mr, Mrs, Miss, Ms, Other” if provided | Enter a valid employee title.<br><br>**Employee titles**<br><br>*   Mx<br>*   Miss<br>*   Ms<br>*   Mrs<br>*   Master<br>*   Mr<br>*   Brigadier<br>*   Captain<br>*   Colonel<br>*   Dame<br>*   Doctor<br>*   Honourable<br>*   Honourable Doctor<br>*   Judge<br>*   Lady<br>*   Lord<br>*   Major<br>*   Professor<br>*   Reverend<br>*   Reverend Father<br>*   Reverend Mother<br>*   Right Honourable<br>*   Right Reverend<br>*   Sir<br>*   Sister<br>*   Wing Commander |

Nil return errors

| Error | Solution |
| --- | --- |
| A nil return should only be filed when you have no employee line items<br><br>* * *<br><br>A nil return should not have any line items | If the file contains employee amounts, it is not a nil return. Change the indicator to N (no). |

Pay frequency errors

| Error | Solution |
| --- | --- |
| Pay Frequency has too many characters<br><br>* * *<br><br>Pay frequency is required | Add a valid pay frequency.<br><br>*   WK - Weekly<br>*   4W - Four-weekly<br>*   FT - Fortnightly<br>*   MT - Monthly<br>*   DA - Daily<br>*   AH - Adhoc / irregular<br>*   HM - Half-monthly / twice a month |

  

Phone and mobile number errors

| Error | Solution |
| --- | --- |
| Invalid phone number<br><br>* * *<br><br><field> is not a valid phone number | This is a number only field. Do not include dashes, brackets or other characters. For local numbers including a contact for payroll, the number should be a maximum of 12 digits. Overseas numbers for employees can be a maximum of 30 digits. |
| Invalid mobile country code<br><br>* * *<br><br>Invalid daytime country code<br><br>* * *<br><br>Invalid employee country code | Enter a valid country code. The country code for New Zealand is NZL. If no number is provided, delete the country code.<br><br>[ISO Online Browsing Platform](https://www.iso.org/obp/ui/) |
| Employee’s mobile phone number was not provided | You must include a mobile number if a country code is added. If no number is provided, delete the country code. |
| Employee’s daytime phone number was not provided | You must include a daytime number if a country code is added. If no number is provided, delete the country code. |
| Employer mobile phone number is required<br><br>* * *<br><br>Payroll contact phone number: Required | Add the required payroll contact number |
| Payroll phone number <field> is too long<br><br>* * *<br><br>Employer mobile <field> is too long | Check the payroll contact number is correct |
| Mob phone number is too long<br><br>* * *<br><br>Employee mobile <field> is too long | Check the number is correct |
| Mob Ext is too long. Maximum length is 20. | Check the mobile extension number is correct |
| Mob Phone Country Code <field> is too long. Maximum length is 3. | Check the mobile country code is correct.<br><br>[ISO Online Browsing Platform](https://www.iso.org/obp/ui/) |
| Area code was not specified for employee daytime phone number | Enter an area code |
| Day phone number is too long. Maximum length is 30. | Check the daytime number is correct |
| Day extension is too long. Maximum length is 20 | Check the daytime extension number is correct |

Tax code errors

| Error | Solution |
| --- | --- |
| A tax code must be provided<br><br>* * *<br><br>Emp tax code <field> is too long. Maximum length is 10<br><br>* * *<br><br>Invalid tax code<br><br>* * *<br><br><field> is not a valid tax code<br><br>* * *<br><br>Tax code has too many characters | Add a valid tax code.<br><br>The Tax code declaration – IR330 lists all available tax codes.<br><br>[Complete my tax code declaration](/income-tax/income-tax-for-individuals/tax-codes-and-tax-rates-for-individuals/complete-my-tax-code-declaration) |
| Tax code appears more than once. May not have duplicate tax codes<br><br>* * *<br><br>The student loan tax code of M appears more than once for an employee on the EIS. There can be only one M deduction for one employee on each schedule. | An employee in the file appears more than once with the same tax code.<br><br>If the employee and tax code information is duplicated in error, delete the incorrect line.<br><br>If the employee should be included twice, the second job should use a valid secondary tax code.<br><br>The Tax code declaration – IR330 lists all available tax codes.<br><br>[Complete my tax code declaration](/income-tax/income-tax-for-individuals/tax-codes-and-tax-rates-for-individuals/complete-my-tax-code-declaration) |