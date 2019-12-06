# SYSC3010_Programmable_Braille
The programmable braille board is an innovative device that can increase accessibility for the visually impaired.

#### Authors:  
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
  #### dependencies: Maven
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
     
# Setting up the Slave PI
  #### Installing and enabling dependencies:
  1. Enable I2C in Raspi-Config -> Interfacing Options -> Advanced
  2. Get I2C tools using the command “sudo apt-install i2c-tools”
  3. Allow the Slave Pi to use I2C by running the command “sudo adduser pi i2c” 
  4. Get Python smbus using the command “sudo apt-get install python-smbus”
  5. Install Flask using the command “pip install -U Flask”
  #### After you have all the dependencies sorted:
  1. Power on the Slave Pi and either connect to it via SSH (SSH pi@[I.P address]) to run it in headless mode, or using a   
     monitor, keyboard and mouse.
  2. Copy the folder SlavePi onto the Slave PI
  3. Ensure the Arduino is setup for I2C by typing the command “sudo i2cdetect -y 1”
  4. Cd into the SlavePi folder via the terminal and run the command “python SlavePiController.py”
# Setting up the Braille Board 
  1. Copy the file Text2Braille_ARDUINO.ino onto your computer
  2. Navigate to the location of Text2Braille_ARDUINO.ino
  3. Open it on the Arduino IDE
  4. Complete the steps in the “Circuit setup” section below
  5. Connect your Arduino via USB
  6. Upload the code onto the board
  7. Turn on the power supply
# Project Images
![Imgur](https://i.imgur.com/QQlkzxH.jpg)
![Imgur](https://i.imgur.com/98bZlTg.jpg)
![Imgur](https://i.imgur.com/fjRSM6v.jpg)

