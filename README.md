# LendsqrQA_Task2_Solution
This task requires creating automated test scripts for at least 2 APIs per API module, excluding the Oraculi Mobile SDK (Beta) module. Furthermore, it provides detailed steps on how to set up and run test scripts in Postman for Task 2 of the assessment and optionally, how to run the exported/downloaded collections in the command line.

# Detailed Steps On How To Set Up and Run Test Scripts in Postman

Step 1: Set up Postman
Download and install Postman from https://www.postman.com/downloads/

Download the API collection tested from the list in this repository based on the test (Positive, Negative or Edge Cases).

Launch Postman and import the Adjutor API collection by clicking on import button in Postman. 

Step 2: Import environment variables (Make sure to have downloaded the environment based on the test; Positive, Negative or Edge case)

Click on Environment tab

Click on import button follow the prompt and upload from where the environment was downloaded into

The collection and environment imported comes with all the endpoints and request and test scripts

Step 3: Run the collection in Postman

From the collection imported, click "..." (more options tab)

Locate and click on "Run collection" to open the collection runner.

Select the environment that was downloaded and imported

Click "Run [collection/Folder Name]"

Step 4: Analyze results

After the run, Postman will display test results

Review passed and failed tests

Check the response time for performance analysis

# Alternatively:

You can run the collection(s) using Newman runner in the command line.

Here are detailed steps to set up and run the Postman collections using Newman in the command line.

Newman is Postman's command-line collection runner, which allows you to run and test your API collections directly from the terminal.

Step 1: Install Node.js and npm

Download and install Node.js from https://nodejs.org/

This installation will include npm (Node Package Manager)

Verify installation by opening a terminal and running:

node --version

npm --version

Step 2: Install Newman

Open a terminal or command prompt

Run the following command to install Newman globally:

npm install -g newman

Step 3: Verify installation by running:

Copynewman --version

Step 4: Prepare Your Working Directory

Create a new directory for your Newman tests

Move your exported/downloaded collection (the ones downloaded from this repository) and environment JSON files into this directory

Step 5: Run the Collection with Newman

Open a terminal and navigate to your working directory using the command: cd path/to/your/working/directory

Run the following command:

newman run YourCollection.json -e YourEnvironment.json

Replace YourCollection.json and YourEnvironment.json with your actual filenames

Step 6: Analyze the Results

Newman will run your collection and display the results in the terminal, showing:

Total number of requests

Failed tests

Total run duration

Test results for each request

# Step 7: Generate HTML Reports (Optional)

Install the Newman HTML reporter:

npm install -g newman-reporter-htmlextra

Run your collection with the HTML reporter:

newman run YourCollection.json -e YourEnvironment.json -r htmlextra

This will generate an HTML report in your current directory which can be opened on your preferred web browser.




