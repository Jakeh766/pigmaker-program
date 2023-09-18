# pigmaker-program

This program takes scanned images of breeding and farrowing records that look like the following examples.

<img width="634" alt="breeding_record_example" src="https://github.com/Jakeh766/pigmaker-program/assets/77121832/dc8cf357-f228-4e43-a0c5-cbfd774ebf9b">

Breeding record example

<img width="669" alt="farrowing_record_example" src="https://github.com/Jakeh766/pigmaker-program/assets/77121832/11554c01-f90e-48a3-9932-4edfa973bc21">

Farrowing record example

Using these scanned images, usually in PDF format, the program converts them to PNG files and sends them to AWS Textract API where it extracts the tabluar data from the images. The program then converts this tabular data into Pandas Dataframes for data cleaning. 
