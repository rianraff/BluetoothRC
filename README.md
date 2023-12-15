# <div style="text-align: center"> BluetoothRC </div>

### Group B6
- Aldrian Raffi Wicaksono       `2106653256`
- Ivan Indrastata Ramadhan		`2106706981`
- Naufal Febriyanto     		`2106702674`
- Raden Bagus S. K. R. G. R.    `2106702610`

## <div style="text-align: center"> Introduction </div>
<div style="text-align: justify">

**Problem**

In today's modern workspace, the lack of playfulness and engagement has become apparent, contributing to monotony and isolation. Traditional desktop accessories often prioritize functionality over interaction, leaving users with a sense of routine. The Bluetooth RC (BRC) project addresses this by introducing a miniature robot designed to bring joy and interaction to the workspace.

The BRC tackles key issues such as the absence of playfulness, the monotony of the workplace, and limited functionality in existing miniature robots. By incorporating playful movements, animated expressions, and interactive features, the BRC aims to create a dynamic and lively workspace experience.

**Solution**

The BRC offers a solution by infusing playfulness and enhanced functionality into the modern workspace. With interactive movements, animated expressions, and playful sound effects, the BRC serves as a companion that responds to user presence, breaking the monotony of daily routines. Equipped with sensors for user interaction and wireless communication for remote control, the BRC introduces a new dimension of engagement.

Powered by the ESP32 microcontroller and the FreeRTOS operating system, the BRC ensures robust processing capabilities, enabling real-time multitasking and advanced functionalities. Its open-source nature encourages a community of creators and enthusiasts to contribute to its development, promising continuous innovation.

The Bluetooth RC's playful nature and interactive capabilities aim to transform the workspace, fostering creativity, reducing stress, and enhancing overall well-being. Join us in creating a more vibrant and enjoyable work environment with the BRC

</div>

## <div style="text-align: center"> Implementation </div>
<div style="text-align: justify">

**Hardware Design and Schematic**

The BRC is engineered with a robust hardware design centered around the ESP32 microcontroller, chosen for its processing power and versatile connectivity options.

| Core Component | Detail |
| :-: | :-: |
| ESP32 Microcontroller | The brain of the BRC, handling processing, sensor readings, motor control, and wireless communication. |
| Motor Drivers | Two drivers translating signals from the ESP32 to motor commands for precise movement |
| Motors |  Two small DC motors providing driving force for forward, backward, and turning motions. |
| Sensors | Ultrasonic sensors act as the robot's eyes, detecting obstacles in its path |
| OLED Display | Displays animated expressions and information to enhance user interaction |
| Battery | Powered by a rechargeable battery, ensuring convenience and portability |

<div style="text-align: center"> 

**Schematic**

</div>
<p align="center">
<img src=Circuit_diagram.jpg>
</p>

**Software Development**

Core functionalities:

1. Motor control
    - Receive user or internal logic commands.
    - Translate commands into signals for motor drivers.
    - Implement motor control algorithms for smooth and coordinated movement.

2. Sensor data interpretation
    - Continuously read data from sensors (accelerometer, gyroscope, proximity sensor, light sensor).
    - Process data to trigger appropriate responses (e.g., change movement based on accelerometer data).

3. User interaction and communication
    - Enable user interaction through a user interface on the robot or remotely via mobile app/web interface.
    - Utilize Wi-Fi and Bluetooth capabilities for communication with external devices.

The FreeRTOS operating system facilitates multitasking for concurrent handling of motor control, sensor data interpretation, and user interaction. FreeRTOS tasks are implemented for independent execution of specific functionalities with varied priorities.

Code structure and workflow:

1. Modular structure for readability, maintainability, and reusability.
2. Initialization phase sets up ESP32, initializes peripherals, and loads configuration data.
3. Main loop continuously:
    - Reads sensor data.
    - Processes user input and commands.
    - Updates motor commands based on sensor data, user input, and internal logic.
    - Drives motors according to updated commands.
Updates OLED display with animations and information.
Handles communication with external devices.

The Interrupt Service Routines (IRS) handle high-priority events (e.g., sensor triggers, button presses) and perform minimal processing and signal the main loop for further action.

<div style="text-align: center"> 

**Sequence Diagram**

 </div>
<p align="center">
<img src=Sequence_diagram.png>
</p>

</div>

## <div style="text-align: center"> Test and Evaluation </div>
<div style="text-align: justify">

**Testing**

While hardware testing has not been conducted on the system yet, the code has been successfully uploaded to the ESP32 board without errors, ensuring syntactic validity and compatibility. The upcoming step involves comprehensive testing using the Android app developed with Android Studio. This testing phase will involve sending commands through the app to observe the robot's behavior and response. Key metrics to be measured include battery life, Wi-Fi range, and communication latency. Results and any encountered issues will be meticulously documented, with the aim of demonstrating the robot's functionality and performance.

**Evaluation**

1. Quantitative methods
    - Measure accuracy, speed, and reliability of robot movements and expressions.
    - Evaluate app usability and functionality.

2. Qualitative methods
    - Conduct surveys and interviews with potential users and stakeholders.
    - Gather opinions and suggestions on the robot and app.

3. Comparison and analysis
    - Compare results with project objectives and requirements.
    - Identify strengths and weaknesses of the system.

4. Documentation
    - Present findings and conclusions in a clear and concise manner.
    - Use tables, graphs, and charts to illustrate data.

5. Future development
    - Discuss limitations and challenges of the evaluation process.
    - Propose future directions for system development and testing.

</div>

## <div style="text-align: center"> Conclusion </div>
<div style="text-align: justify">

In the culmination of this project, we've crafted a miniature desktop robot with expressive facial features, wirelessly controlled via an ESP32 board and freeRTOS. Leveraging tools like 3D printing, Arduino, and Android Studio, we've embarked on a journey marked by innovation and creativity.

While unforeseen circumstances impacted our ability to conduct timely hardware testing, we acknowledge this limitation. The project timeline has not been met, and as a result, we cannot assert the complete achievement of our objectives and requirements.

However, a robust plan for testing and evaluation is in place, involving the Android app's command transmission to the robot, observation of behavior, and measurement of critical metrics such as battery life, Wi-Fi range, and communication latency. Documentation of results and user feedback through surveys and interviews will form a crucial aspect of our evaluation strategy.

Despite facing challenges, this project has been a rich learning experience, enhancing our skills in robotics, Arduino, and Android development. We appreciate the support and feedback received from our supervisor and peers. Looking forward, we are enthusiastic about completing the testing and evaluation phases, demonstrating the robot's functionality, and unveiling the potential for future development and innovation.

</div>
