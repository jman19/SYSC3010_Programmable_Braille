# SYSC3010_Programmable_Braille
The programmable braille board is an innovative device that can increase accessibility for the visually impaired.

Authors:  
  MasterPI: Jason  
  MasterPIButton: Jason  
  SlavePI: Jason (Restful Interface), Sam (rest of the code)  
  Arduino: Sam  
  Android App: Omar  
# How to get all the code/update SubModules
  1. clone the project
  2. cd into project
  3. git submodule update --init
# Setting up Master PI
  1. Copy the folder MasterPi onto the masterPi 
  2. Cd into the MasterPi folder on the masterPi run the command “mvn spring-boot:run” this will start the server 
  3. (optional) there are configurable settings located in “src/main/resources/application.properties” these settings allow you to
      specify things such as text parse size and the IP and port of the slave PI note you must restart the server for new settings 
      to apply
  4. (optional) to run the automated test run the command “mvn test”
# Setting up the MasterPi Button controller
  1. Copy the folder MasterPiButton onto the masterPi
  2. Cd into the MasterPiButton folder on the masterPi run the command “python MasterPiButton.py”
  3. (optional) if one wishes to simply verify that the hardware of the buttons are functions run the command “python 
     DriverTestButton” this will launch an application to print on the console to indicate that a specific button was pressed
# Project Images
![Imgur](https://i.imgur.com/QQlkzxH.jpg)
![Imgur](https://i.imgur.com/98bZlTg.jpg)
![Imgur](https://i.imgur.com/fjRSM6v.jpg)

