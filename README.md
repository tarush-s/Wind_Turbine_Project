# ESE 5160-WIND CHEATERS

## Team Members 
Tarush Sharma & Pratyush Mallick 

## Video 

[![Watch the video](https://github.com/ese5160/a14-final-submission-group-wind_cheaters/blob/main/ProjectPic.jpg)](https://drive.google.com/drive/folders/1qCl4C_BRDAGmtREUxvwGxH0i9VQtbXF5)

## Pictures 
<p align="center">
<img src="https://github.com/ese5160/a14-final-submission-group-wind_cheaters/blob/main/PCB Layout 3-D.png" width="18%"></img> 
<img src="https://github.com/ese5160/a14-final-submission-group-wind_cheaters/blob/main/PCB Layout 2-D.png" width="18%"></img> 
<img src="https://github.com/ese5160/a14-final-submission-group-wind_cheaters/blob/main/PCB_Top.jpg" width="15%"></img>
<img src="https://github.com/ese5160/a14-final-submission-group-wind_cheaters/blob/main/PCB_Back.jpg" width="15%"></img>
<img src="https://github.com/ese5160/a14-final-submission-group-wind_cheaters/blob/main/ThermalCamera.jpg" width="15%"></img>

<p align="center">
<img src="https://github.com/ese5160/a14-final-submission-group-wind_cheaters/blob/main/Backend.png" width="25%"></img> 
<img src="https://github.com/ese5160/a14-final-submission-group-wind_cheaters/blob/main/NodeRedGUI.png" width="25%"></img>
<img src="https://github.com/ese5160/a14-final-submission-group-wind_cheaters/blob/main/ProjectPic.jpg" width="20%"></img>
<img src="https://github.com/ese5160/a14-final-submission-group-wind_cheaters/blob/main/ProjectPic2.jpg" width="20%"></img>

## Project Summary 

### Device Description
<p>The apparatus serves the purpose of overseeing the operational condition of wind turbine monitoring systems, concurrently aligning it in the optimal direction for enhanced efficiency. It possesses the capability to monitor various parameters, including temperature, humidity, vibrations, and pressure within the mechanical chamber of a wind turbine. These recorded data points are instrumental in facilitating predictive maintenance practices and enabling the proficient control of wind turbines. A tailored Graphical User Interface (GUI) has been implemented to present health-related statistics and facilitate the user in positioning the turbine according to their specified preference.</p>

### Inspiration
<p> The inspiration for conceptualizing this product arises from the imperative to implement efficient energy harvesting techniques. Wind energy harvesting presently constitutes 10% of the nation's electricity production and is on a trajectory of growth. Consequently, the imperative to harvest energy with optimal efficiency becomes indispensable for the sustained efficacy of the solution over the long term.
</p>

### Device Functionality

The apparatus has been meticulously designed to be seamlessly integrated with any operational wind turbine. It provides a high degree of adaptability in the placement of the air velocity sensor. Onboard, a suite of sensors, actuators, and integrated circuits (ICs) is incorporated, comprising:

1. **BME680 (Bosch Environmental Sensor):** This sensor furnishes data on the ambient pressure, temperature, and humidity in the proximity of the device. Its inclusion is imperative as it affords insights into the heating constraints of the PCB. The sensor utilizes the I2C communication channel to talk with the Microcontroller Unit..

2. **LSM6DS0 Accelerometer:** Tasked with measuring vibrations within the gearbox, this accelerometer is configured to initiate an alarm should vibrations exceed predefined safety limits. Utilizing the SPI communication interface to engage in communication with the main Microcontroller Unit.

3. **A4988 Stepper Motor Driver:** Strategically placed on the board, this driver facilitates the control of a Nema17 stepper motor. Capable of driving high-current bipolar stepper motors, it can supply up to 2A of current, enabling precise and torque-driven movements.

4. **SD Card Reader:** The integrated SD card reader serves the purpose of storing backup firmware images or facilitating Over-The-Air updates for the acquisition of new firmware. The SD card reader communicates with the Microcontroller Unit using SPI protocol.  

### Project Links
<p>The link to our node-red instance is given below. </p>

[NODE-RED](http://172.178.45.14:1880/ui/#!/1?socketid=f3atLysdu5UjvYGdAAAB)

<p>The link to our custom PCBA is given below. </p>

[PCBA](https://upenn-eselabs.365.altium.com/designs/142BF039-9CF6-45FC-A34A-C023821C1D9D?variant=[No+Variations]&activeDocumentId=Main.SchDoc(1)&activeView=SCH&location=[1,97.86,12.59,26.06]#design)

### Challenges

During the prototyping phase of our product development, we encountered several challenges, which we have categorized into software and hardware issues:
1. **Software Challenges:**
   - In the sensor interfacing stage of the design process, it became apparent that the SPI sensor operates effectively only at a baud rate below 1 MHz.
   - Another software-related issue arose with the FTDI chip utilized for our USB connection; it exhibited heightened sensitivity to noise, necessitating proper coupling for optimal performance.

2. **Hardware Challenges:**
   - A manufacturing oversight resulted in the placement of 4 Ohm pull-up resistors instead of the intended 4.7K Ohms, causing a short between the SDA and SCL lines.
   - Further investigation revealed that the motor driver IC could supply a full 2 Amps of current only when equipped with a heatsink attached to it.

<p>
Overall, these insights contribute to enhancing the robustness and efficiency of future product development processes by addressing and mitigating potential challenges proactively.
</p>

### Next Steps 
Additional enhancements that can be incorporated into the project include:

1. **Gear-Box:** Introducing an supplementary coupling gear-box to the design would facilitate the isolated rotation of the sensor. This adjustment enables the collection of air velocity data from various directions before coupling with the wind turbine gear to position it accordingly.

2. **Sensor Suite:** Further refinement of the sensor suite is conceivable, with the addition of sensors capable of monitoring detailed data points such as oil levels in the gear box. Additionally, the inclusion of a meter to quantify the electricity generated by the turbine would contribute to a more comprehensive sensing capability.

