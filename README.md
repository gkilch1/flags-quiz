# flags-quiz

This app was created to demonstrate my understanding of connecting a PostgreSQL database to a full-functioning web application. 

The criteria you will need to run this application locally: 
1. PostgreSQL and pgAdmin
2. A code editor

Steps to running locally: 
1. Make sure PostgresSQL and PgAmin are downloaded to your computer
   
    - If they are not, use the below links to  begin the download:
      > Mac - https://sbp.enterprisedb.com/getfile.jsp?fileid=1258653 
        - Mac Users: If a pop-up asks permission to run the installer, select Open. You might need to enter your Mac password to allow the installer to run.
      > Windows - https://sbp.enterprisedb.com/getfile.jsp?fileid=1258649
        - Windows Users: If prompted to run the installer, select YES.
    - Click 'Next' until you see the screen that asks you to check all the packages you want installed.
      > For Mac and Windows users, you want to make sure all boxes are checked
        - PostgreSQL Server
        - pgAdmin
        - Stack Builder
        - Command Line Tools
    - Keep clicking on the 'Next' button until you come across a prompt asking you to enter a username and password.
      > The username will be 'postgres' and you will need to create a password. It is EXTREMELY important to write this password down for later use.
    - Continue until you click 'Finish'
    - A prompt for Stack Builder may appear after installation, but you can close it.
    
2. Once PostgreSQL is successfully installed, you will need to build out your database.
    - To begin, launch pgAdmin. Once pgAdmin is open, navigate to the PostgreSQL server.
      > Here you will be prompted to enter the password you created earlier.
    - After logging in, go to the 'Databases' section and create a new database. To do this, right-click on 'Databases' and select 'Create', followed by 'Database...'. A pop-up menu will appear where you should enter the name 'World' as the database name. Leave all the default settings unchanged and click 'Save'. Next, click on the newly created database and look for the 'Start Query' button on the top left corner. Click on it to run a new query.
      
      > ![Screenshot (352)](https://github.com/gkilch1/flags-quiz/assets/113639024/bfc8b284-38b6-4279-ac5d-d59b787ee571)
      
    - In the query editor, you will want to run the below command to create the table we will use:
      > CREATE TABLE flags ( id SERIAL PRIMARY KEY, name VARCHAR(45), flag TEXT );
    - If you have created the flags table correctly, you can find it under the 'World' database. To locate it, navigate to 'Schemas' and then to 'Tables'. After refreshing the 'Tables', the flags table should appear. You can easily view and edit data by right-clicking on the 'flags' table. As of now, there are no records available.
    - To insert the data, you will first need to download the 'flags.csv'. After this is downloaded, right-click on 'flags' table again, but this time select 'import/export data'. Go ahead and add only that 'flags.csv' file. Make sure 'Import' is selected and the file format is 'csv'. Scroll over to the options tab and turn on 'Header'. After that click OK.
      > Refresh 'Tables' and then right-click on 'flags' --> 'View Data'.
    - If the db was set up correctly, this should be the output in pgAdmin.
      
      > ![Screenshot (353)](https://github.com/gkilch1/flags-quiz/assets/113639024/630979ed-48ee-4d9b-9213-0528ab75ed89)

3. Now move to the code editor you will be using
   - You will want to download or clone this repo. Once you have successfully opened this project in the code editor of your choice, you will need to start up your terminal. In your terminal cd over to where you are storing the project and run 'npm i' or 'npm install' to download all of the packages required for this application.
   - Toggle back over to your code editor and open up the 'index.js' file. Here you will want to insert the password you created for PostgreSQL.
     
     > ![Screenshot (354)](https://github.com/gkilch1/flags-quiz/assets/113639024/9b7c0843-9bb0-453e-bf01-e218a7594b8d)
     
   - Once you have made the changes to the 'index.js' file, save them and return to your terminal. Run the command 'nodemon index.js' to launch the app on 'localhost:3000'. Open your browser and go to 'localhost'. You can then start the flags quiz.
     > For Windows users to view the flags properly, you will need to use Firefox and not Chrome.
   - Here is the end result:

     > ![Screenshot (355)](https://github.com/gkilch1/flags-quiz/assets/113639024/78dbe6dc-1c66-4541-96e9-c126a6940f6c)






Additional resources: 
> Node.js and npm install - https://docs.npmjs.com/downloading-and-installing-node-js-and-npm 



