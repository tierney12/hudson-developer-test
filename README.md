# hudson developer test
This is my proposed solution for the hudson developer test.

To run in eclipse:

Open a workspace and select to import a project.
In the import options: first select 'General, Existing project into workspace.' https://i.imgur.com/YI1h09d.png
Then choose 'select archive file,' and select the .zip from this repository. Then select 'Finish.' https://i.imgur.com/IwfcxZ7.png

Select the 'Parser.java' class in the package explorer, and select run configurations https://i.imgur.com/QdXUa0S.png
Select to run as a Java Application, under arguments enter the target website url, and an optional filename for the JSON output. https://i.imgur.com/WfFIdqH.png
Select 'apply' and 'run'

Output is default to "output.json"

When testing the application I decided to do inline testing with helper functions for printing variable values to the console rather than use an automated testing module e.g. JUnit.
I decided to do this because the application simply parses data and exports it using two well documented and tested modules. I designed the application with extensibility and testability in mind, creating different helper functions to separate the concerns so that with extension the code would not have to be redesigned in order to test individual functions, such as querying the list of products  to check prices, stock etc. 