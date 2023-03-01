<h1 align="center">Checkpoint 2 Presentation - Team 304 - Portable Weather Station & Portable Personal Fan</h1>

&nbsp;

## Checkpoint 1 Presentation
[![Checkpoint 1 Presentation](./images/design-ideation-images/Checkpoint1PresentationThumbnail.JPG "Checkpoint 1 Presentation Thumbnail")](https://www.youtube.com/watch?v=TLzWeIzh0lc&ab_channel=CaymanPreston "Checkpoint 1 Presentation")

&nbsp;

## Selected Design

![Selected Design](./images/design-ideation-images/Selected_Design_Drawing.svg "Selected Design")

<!--- Write a description here about what's going on in the design.-->

![Design Enclosure 1](./images/design-ideation-images/Enclosure(Isometric1).jpg "Enclosure (Isometric) 1")

![Design Enclosure 2](./images/design-ideation-images/Enclosure(Isometric2).jpg "Enclosure (Isometric) 2")

<!--- Add an included description for these images.-->

![Design User Needs](./images/design-ideation-images/Selected_Design_User_Needs_Table.JPG "Selected Design User Needs")

<!--- Consider adding a little description here.-->

&nbsp;

## Block Diagram

Once we developed out final project design concept, we then developed a block diagram to identify the individual subsystems needed to fulfil the project requirements and develop our project. We separted our design into four main subsystems: Power Supply subsystem, Microcontroller and OLED subsystem, Temperature Sensor subsystem, Humidity Sensor subsystem, and Motor Controller subsystem.

![Block Diagram](./images/design-ideation-images/Team_304_Block_Diagram_(New)_SVG.svg "Team 304 Block Diagram")

The Power Subystem uses a switching voltage regulator to output 3.3V to supply power to the microcontroller, temperature sensor, and humidity sensor. The Microcontrooler is an 8-bit microcontroller with MQTT, UART, PWM, SPI and I2C which fulfills project requirements. The Temperature sensor and Humidity sensor run on I2C protocol which fulfills one of the communication protocol requirements. The Motor Controller subsystem drives the motor using SPI communication protocol which fulfills project requirements. All components are surface-mount components and each pinout is labeled on the microcontroller block with their specific communication protocols.

&nbsp;

## Component Selection

[Component Selection.pdf](https://github.com/EGR314-Team-304/EGR314-Team-304.github.io/files/10863817/Component.Selection.pdf)

### 5V Voltage Regulator

![image](https://user-images.githubusercontent.com/122584348/222214879-eef7bc81-d864-4548-812d-55aa9cb1cfb7.png)

This IC is not much more expensive than the cheapest option, and is a big step up in the reputability of the manufacturer. We were initially going to go with option 1 because we are familiar with this chip as we used it in one of our ICC’s (the 3.3V version) but it was out of stock. We went with this alternative option because of its large stock.

### 3V Voltage Regulator

![image](https://user-images.githubusercontent.com/122584348/222215442-e1992483-ec26-4a95-8989-41be0ceb9bd6.png)

This IC is the cheapest option, and is a very reputable manufacturer. We also are familiar with this chip as we used it in one of our ICC’s (the 3.3V version). Worst case scenario we have to substitute it with the slightly more expensive and larger TI version.

### Humidity Sensor

![image](https://user-images.githubusercontent.com/122584348/222215996-7b30da86-b69e-4d1c-a3c9-103d8f6a54ed.png)

Product was found on a reputable source and manufacturer. The price is the most competitive out of the other options and has the best sensor accuracy. The sensor runs on I2C protocol which will fulfill one of the communication protocol requirements as well.

### Temperature Sensor

![image](https://user-images.githubusercontent.com/122584348/222216164-d7e42745-26c6-4a6c-911b-20abcc371094.png)

Product was found on a reputable source and manufacturer. It is accurate and has a wide temperature-sensing range. It is the cheapest option and the benefits match the other more expensive sensors. The sensor runs on I2C protocol which will fulfill one of the communication protocol requirements as well. 

### Motor Driver

![image](https://user-images.githubusercontent.com/122584348/222216362-ba5fe039-a115-42be-9db5-4c8bc66f6ae2.png)

It is the only part that was able to be found that would actually suffice for this project, as finding surface mount motor driver parts that are readily available and have serial communication capabilities are not easy to find online. This part was initially given out to the class, which will help in getting acquainted with the part’s behavior and obtaining help with getting the part to work. This part also comes with a datasheet for further information. This part will require an additional power rail but will serve our project’s purpose, nonetheless.

### Fan

![image](https://user-images.githubusercontent.com/122584348/222216521-b2b4859b-c870-4332-a3e9-49038f1e7e48.png)

The pricing for this device is the best out of all the options here, allowing for a couple more being available to order for spares. The listing for this product is also more reputable than some of the other options. This fan comes included with a datasheet and mounting screws, although the datasheet is not as detailed as Option 1’s. This product runs with 5V, and while it is larger than the other options with no RPM listed, it serves as a more efficient cooling fan that would best serve our project’s needs.

### Power Source

![image](https://user-images.githubusercontent.com/122584348/222216729-c5ab52b4-0c13-49b6-a715-3be7b8f345a2.png)

The reason we went with the 3.7V batteries is because this would remove the need for a 5V switching regulator for our project. The 3.7V would be sufficient to run our motor driver and motor and then would be stepped down to 3.3V for our microcontroller and other components. We deemed this the best option and most cost effective taking into consideration the money we’ll save from cutting out the 5V switching regulator.

### OLED Display

![image](https://user-images.githubusercontent.com/122584348/222216881-797f8d0d-70f1-4c0c-840f-29c408f03614.png)

The reason we went with option 1 was because of the price and the I2C protocol. We’ve been informed that the I2C protocol is easiest when coding an LCD screen. We also determined that our final product will be relatively small so the small size of the OLED will be perfect for our device.

## Power Budget

<!--- Add screenshots of the Power Budget and add it here with a small description to explain what's going on in it.-->

&nbsp;

## Microcontroller Selection

 ![PIC18LF27K40 Microcontroller](./images/design-ideation-images/PIC18LF27K40.png "PIC18LF27K40")

<!--- Rearrange some of the wording on the existing report to flow with this section. (Look at section of text just above the image on the report)-->

&nbsp;

## Hardware Proposal

<!--- Include PDF of the complete schematic, ensure it's able to be clicked on and include a little description noting the ability to click on it to zoom in.-->

<!--- Include a description to go over the different components in a general sense.-->

## Software Proposal

In order to model and lay out the overall framework and architecture of the code required to run our product, our team created an activity diagram. The goal of the diagram was not necessarily to write any functional code, but to establish the overall functionality of our software. We did so by creating a UML state chart mapping the intended flow of our program. 

&nbsp;

### Software Proposal UML Activity Diagram
![Team 304 Software Proposal UML Diagram](./images/design-ideation-images/304SoftwareProposal_02_24.jpg "Software Proposal UML Activity Diagram")

### Functionality

Our program will begin with the initialization of necessary peripherals, including EUSART, I²C, and SPI. The initialization functions will run only once, at the beginning of the program. Next, we will enter the main loop of the program.

Within the main loop of the program, the PIC MCU will repeatedly execute a set of instructions. First, it will utilize the I2C protocol to acquire data from the temperature and humidity sensors. Next, it will analyze the data gathered from the sensors and make a determination as to what speed the fan should operate at. This decision is based on the temperature and humidity readings. After deciding on the appropriate fan speed, the PIC MCU will transmit this information over the SPI protocol to the motor, which controls the fan's rotational speed. Finally, the PIC MCU will take into account the current menu setting and utilize the USART protocol to send the appropriate data to the LED screen. The data displayed on the LED screen is based on the settings that have been selected by the user. This entire process is continuously repeated in a loop, allowing for the system to consistently monitor and adjust the temperature and humidity levels as necessary.

If, at any point during the main loop, the menu button is pressed, an interrupt is triggered and the program enters the menu subloop. The menu index is incremented, which determines the current mode of operation within the menu subloop. The menu subloop has been designed to provide the user with various options for interacting with the system.

In mode 1, the program simply displays the current temperature and humidity values. This allows the user to monitor the current state of the system without making any changes.

In mode 2, the program displays the maximum temperature and humidity recorded in the current session. This requires the program to keep track of the highest temperature and humidity readings received since the session started. To accomplish this, the program continuously compares the highest recorded temperature and humidity values with the current readings and updates the maximum values as necessary.

In mode 3, the user can calibrate the system by entering known temperature and humidity values. The program then calculates the difference between the measured and input values and saves this difference as an offset to be applied to all future readings. This allows the system to be adjusted to account for any discrepancies in the sensors or other environmental factors. 

By providing these different modes of operation, the program allows for greater flexibility and customization of the system. Additionally, the use of interrupts and menu indexing provides a user-friendly interface that allows for easy navigation and control of the system.

### Rationale

Our team carefully considered the suite of features that our hardware could theoretically be used for and aimed to provide as many features as possible with a simple and understandable user interface. The main loop of the program was designed to continuously read data from the temperature and humidity sensors, process that data to adjust the fan's speed, output data over SPI to the motor, and transmit selected data over USART to the LED screen. This was done to ensure that the system was constantly monitoring and adjusting to changes in temperature and humidity, and that users could easily see the current readings on the LED screen. The menu subloop was implemented to provide users with a way to access and customize different settings on the product, so as to increase the product's flexibility and user-friendliness. The three different modes of the menu system were designed to provide users with different options based on their needs, such as viewing current or historical weather data. Calibration of the device was deemed a necessary option to ensure that users could trust the data provided by the system and make informed decisions based on that data. We also wanted the user interface to be simple, intuitive, and responsive. To make the product more user-friendly and accessible to a wider range of users, we wanted the menu system to be easy to navigate and understand.

[< Back to home](./index.md)
