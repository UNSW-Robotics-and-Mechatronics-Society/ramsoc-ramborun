# Welcome to the RamboRun Coding Section!

Whether you're encountering errors during code upload or simply exploring the available functions, this guide has got you covered.

I will go over setting up the Arduino IDE and uploading the code and modifying your OttoBot behaviour.

# 1. Setting up the IDE 
Once you have downloaded the [Arduino IDE](https://www.arduino.cc/en/software), open the ramboRun.ino file.

Now go to library manager (Sketch > Include Library > Manage Libraries) and download **Adafruit SSD1306** and **Adafruit GFX Library** by Adafruit. Or you can click the library icon on the left of the window. 

To confirm that you have downloaded it, compile the sketch using the 'tick' icon on the top left of the IDE

The code should compile without any errors.

# 2. Downloading code from Github
After downloading the IDE you should download this repository. 

To do so click on the green button in the top right hand corner that says ` <> code` after doing so a drop down menu will appear. The last option listed should be `Download ZIP` select this option and once downloaded extract the files in your designated location.

# 3. Uploading to the nano
Once you have completed step 2, connect the devices Arduino nano to your computer and select the board. The port selection is located at the top of the IDE: 

<img src="images/Port.png" width="500px" height="auto">

The IDE might pickup your bluetooth ports like mine has. Usually, the names have "usbserial", "COM2" or similar in it. A trick I use is to disconnect the Arduino, observe which ports are listed, reconnect it, and then identify which new port appears in the list. 

Once you have selected the port and Arduino Nano board, upload the code to the Arduino nano: 

## Upload Errors
**If you have no errors, you are in luck!**

It's always a mission uploading code using the IDE, here's a fix to a common error that occurs:


* Run the old bootlegger. Go to Tools > Processor > Atmega328P(Old bootlegger):


  Now try uploading again, it should work!

* If the same or similar error still persists, ensure the right board and port is selected, press the reset button on the arduino or restart your IDE.

# 4. Serial Monitor
Open the serial monitor to view outputs from ramoRun. Go to Tools > Serial Monitor to open the monitor. 


# 5. Its ALIVE
If you have assembled the RamboRun correctly, the hardware is functional, the wires aren't faulty and the stars align, then your device should display the start screen of RamboRun with wave over the ultrasonic to initiate the game.

# 6. Modifying RamboRun
`ramboRun.ino` contains some initial `const` terms you can chance to adjust to your liking you can also explore the other functions and test out changing the parameters or variables provided to see how 


# 7. Troubleshooting
I've listed some common issues that may aid in the debugging process:
* Ensure the component (servo, US) is connected to the correct pin defined in the code. For example, `#define TRIG_PIN 8` means that the trig pin from your ultrasonic sensor should be connected to pin 8 in the Arduino Nano.
* If the code uploads but the device has slow or no movements, try replacing the wire.
* If you are using Windows and have issues uploading the code to the nano, search for **CH340 driver download** on your browser and follow the prompts. Since we use arduino nano clones, the necessary drivers might not be installed.

# 8. Conclusion

I hope you found this tutorial useful, please reach out (workshops@ramsocunsw.org) if you have any issues you need help with!



