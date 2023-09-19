## How to use Pigmaker Program

This program takes scanned images of breeding and farrowing records that resemble the following examples and generates reports.

<img width="634" alt="breeding_record_example" src="https://github.com/Jakeh766/pigmaker-program/assets/77121832/dc8cf357-f228-4e43-a0c5-cbfd774ebf9b">

Breeding record example

<img width="669" alt="farrowing_record_example" src="https://github.com/Jakeh766/pigmaker-program/assets/77121832/11554c01-f90e-48a3-9932-4edfa973bc21">

Farrowing record example

When first opening the program, this window will open.

<img width="367" alt="UI_Window" src="https://github.com/Jakeh766/pigmaker-program/assets/77121832/beb11c9a-d6be-45b5-9aef-3e2b6c1307e4">

Then the user should input the start and end dates for the breeding, farrowing, and weaning, and then the group number. Then the user can enter the breed and farrow files and then click the review breed button and this window will pop up. 

<img width="696" alt="Editor_example" src="https://github.com/Jakeh766/pigmaker-program/assets/77121832/9f910e0b-9d57-4781-8b30-bcb835d532b4">

The table cells highlighted in red are errors and the user must manually correct them. Likewise, the user will follow the same process for the farrowing records. 

Once all errors have been corrected. The user can click the generate report button and a pdf report that looks like this will be generated.

<img width="316" alt="Report_example" src="https://github.com/Jakeh766/pigmaker-program/assets/77121832/f243ce00-484d-4f3d-910e-93957efb3b8a">

<img width="310" alt="Report_example2" src="https://github.com/Jakeh766/pigmaker-program/assets/77121832/64854717-2bee-4594-857f-1132cb6d1cd9">

After reviewing the report, the user can choose to output the group's data to the excel database.

## How the program works
Using these scanned images, usually in PDF format, the program converts them to PNG files and sends them to AWS Textract API where it extracts the tabular data from the images. The program then converts this tabular data into Pandas Dataframes for data cleaning. It performs separate cleaning for the breeding and farrowing dataframes. Then the program has a check errors function that will check the dataframe for any values that are obviously wrong. For example, if there is a letter where there is supposed to be a number, the function will count that as an error and highlight it in red so the user can see it. Once the user has corrected all errors, the program merges the breeding and farrowing dataframes together and generates a report mostly by using the pandas Python library.  
