# App_Parser Project : This project is used to extract the builds created using the different operating systems present in the Artifactory (JFrog). Also to parse the applications present in those builds and store the required details in the database accordingly.

Procedure to run the project :-
1. Install pip for python3 using : sudo apt install python3-pip

2. Now setup the virtual environment :-

   a. Activate the venv with this command : source env/bin/activate
   
   b. (If required)To deactivate the environment use this : deactivate

Note : If the activate command does not work, install virtual environment in the system using this command : python3 -m pip install --user virtualenv

3. Now setup the Django : pip install django

Note : To check if Django installed properly use this command : django-admin --version

4. Setup the pymongo : pip install pymongo

5. Setup the dnspython : pip install dnspython

6. Setup the Rest framework for Django : pip install djangorestframework

7. Install the pytz module to use the standard date and time of our timezone : pip install pytz

8. Install some modules for the image extractor (bash file) to run :-
   
   i) pip install bsdiff4
   
   ii) pip install google
   
   iii) pip install protobuf==3.20.0

9. Now being in the project folder run the manage.py file using this command : python3 manage.py runserver

10. After running the server, go to the postman application (Download it if not present).

   a. In that paste the server URL and add this to the url /fetch. This readAndFetch is the API url included in the project for the API call.
   
   b. After this change the API call to GET.
   
   c. Click on Send.
   
This will read and fetch the data of Builds in the below preview box.

                                 OR

   a. In that paste the server URL and add this to the url /parse. This readAnd Fetch is the API url included in the project for the API call.
   
   b. After this change the API call to POST.
   
   c. Then, just below it click on body and then click on raw.
   
   d. Paste the path name in double quotes " ".
   
This path is from the local disk where the CSV and ZIP files are present.

Note : Always give the absolute path.

   e. Now click Send.

11. [When POST API is called] The code will run successfully.

And after the execution, we will get the status of the data in database in the below preview box.

Detailed status of the extraction in the terminal.

And required folders will be created in the path provided due to mounting of images.

12. If another path of file needs to be processed, repeat step from 10.
