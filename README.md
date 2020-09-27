`gen.py`:- 
This program output a csv of n rows specified via the `rows` argument, the header specified in the `column` option via the column_name. Generating different random data for each columns and rows of type integer (eg: 1,2,3000, …) or string (alpha characters of size 1 to 10 maximum)

This program take three arguments:- 
rows :- it is optional and have default value 50. This reflect the number of rows we will output in the csv file

output_path:- it is optional. This is to specify where we want the file to be saved and if not specified than default path will be current directory.

column:- It is not optional and form of the agrument  are - column_name, column_type. Type can be integer and string only.

To run only this file, example:- "python3 gen.py -r 100 -c name,str"

`api.py`:- It is a REST Api which is developed in Flask.
It is using two HTTP methods:- POST and GET
POST: push data to a file, which we doing in chunks as in I don’t have to push all of the file at once. We can push more than one file if we want to.

Still in process- push a file in multiple parallels call.

GET: retrieve a file that has been uploaded. It will be in the same order as the original file that has been pushed to the API. 

To run only this file, example:- "python3 api.py"

`auto.sh`:- wrote a bash script to automate above two files.

- generating a file of 100 rows using the first python script you have written (gen.py)

- Upload that file in chunks.

- Retrieve the file which has been uploaded via the GET and saving into current directory.

- Getting Diff of original file and  retrieved file from API.

In process:-  Uploading a file in chunks of 10,which will upload in parallel.

To run only this file, example:- "./auto/sh"

`Note`- These three code still in process and in debugging mode. Working on it and trying to implement more features into it. It is my current practice code.

