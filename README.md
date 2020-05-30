## GUI, API Test Automation Sample

![Image of Yaktocat](https://github.com/MamdouhMansour/mml_89-yahoo.com/blob/master/test-automation.jpg)

#### *Getting Started*

- Within your IDE import this project by clone the project url, before that you need to signin with GitHub.
- IntelliJ: first fork the project to you repositories (File >> New >> Project from Version Control >> GitHub (Login) >> Select the project >> Clone )
- Eclipse: (File >> import >> Git >> Projects from Git >> Clone URI >> Copy the URI >> Next >> Next >> Check "Clone submodules" >> Next >> Next >> Finish)
- Each package has package-info.java class to identify the purpose of each .
- Code is documented.

#### *Prerequisites*

- JDK 13.
- Lastest Eclipse or IntelliJ IDE.
- Lastest Chrome WebDriver.
- Latest Chrome Browser.

#### *Test Data*

- Test data for google search task externalized from "/Gui_Api_Automation_Task/src/test/resources/TestDataFiles/GoogleTestData.properties".
- Test data for herokuapp task externalized from "/Gui_Api_Automation_Task/src/test/resources/TestDataFiles/HerokuappTestData.properties".
- Properties file of herokuapp includes the absolute path for the image file to upload, after cloning the projec to your local maching change the path in "HerokuappTestData.properties" by change the value of "File_Path" to your file absolute path.
- Data can be externalized using ExcelFileManager.
- Last update done by deleting properties files, getTestData class and externalize test data using ExcelFileManager.

#### *Running Tests*

- Tests can be run within the test class, sampleTestSuite.xml, or via terminal "mvn test".
- Tests can be scaled using docker-zalenium, by installing Docker-Desktop then open the terminal in your IDE and run the commands wrote in "docker-compose_zalenium.yml" attached with the project to build your images, in "execution.properties" you need to change the execution address as following--> executionAddress=localhost:4444.
- In sampleTestSuite.xml within test tags you need to add the following--> <test thread-count="2" name="GUI Test" parallel="classes">, to manage the thread tests need and make execution parallel.
- As advantage of Zalenium no need to reconfigure the images created as Zalenium automatically creates images if needed.  

#### *Reporting*

- Allure report is generated with gif of each test, logs, and assertion result.
- This report can be run from the project folder by running the "generate_allure_report" executable file.
- Automatic host of allure reports on local run of automated tests can be done by assign "openAllureReportAfterExecution" to be true in "execution.properties".
- API response body of random Cat-Fact is attached to the log of the test in allure report.
- You can configure allure reprot multiple options through "execution.properties".

#### *Built With*

- Java
- SHAFT_ENGINE
- Maven
- TestNG

#### *Further Release* 

- Running from cloud testing.
- Scaling with Dockers.
- Automatically host reports with Jenkins.
- BDD.

