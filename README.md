# Introduction
This engineering documentation presents the technical details and design specifications of the autonomous vehicle robot developed by the TLGC Catalyst Future Engineer's Team for the Philippine Robotics Olympiad 2025

# Content
**docs**- Contains all documentation for the project, including robot architecture, programming flow, assembly instructions, improvement logs, and team information.

**hardware**- Contains EV3 hardware related files such as chassis designs, wiring layouts, and parts lists.

**media**- Contains visual assets such as robot photos, design diagrams, wiring schematics, and video recordings.

**software**-  Contains all source code for the EV3 robot. This includes the main control program developed using LEGO Mindstorms, which manages motor control and sensor input to perform tasks and navigate the environment.

> [!NOTE]
> This README.md doesn't contain all the information, some details are inside the folders

# TLGC Robotics Catalyst Team
Our team consists of three dedicated members who carefully manage the key aspects of our autonomous vehicle’s development. Representing Toplink Global College, the Future Engineers Team is a passionate group committed to optimizing the essential electromechanical systems that drive our fully autonomous robot.

![Future Engineers Team Photo](https://github.com/user-attachments/assets/275cc0c6-ded0-43f2-af96-ff63b8f0492a)

**Marc Vincent B. Cortez**(Right)                                                                                                                              

**Andrei Jerome M. Manalansan**(Left)                                                                                                                         

**Yasser M. Lapaz**(Middle)                                                                                                                                    

> [!NOTE]
> The team information is at the docs folder
# Materials
Our autonomous self driving car was developed using the LEGO Mindstorms EV3 Education Set (45544) and LEGO Mindstorms Education EV3 Expansion Set (45544)

![45544-1-0-removebg-preview](https://github.com/user-attachments/assets/7b6e5ab7-0c0d-43d3-89e1-20ac8d9be258)
<img width="500" height="500" alt="Lego Mindstrom Expansion Set " src="https://github.com/user-attachments/assets/54831924-3041-4191-8ca0-946f1caf6f2f" />


> [!NOTE]
> The list of the materials used in our robot is inside the hardware folder

# Chassis

## Selection Of Wheel

![Wheels & Rims](https://github.com/user-attachments/assets/5b4b30df-26f0-4f54-bbd8-d0d5175c212c)

We selected the Wheel 41897 with Rim 56098 at the front and the Wheel 15038 with Rim 44771 at the rear to optimize our robot’s performance on a mat field. The front wheels are lightweight and have a low friction, narrow profile, which allows for quick, smooth turns with minimal resistance perfect for precise navigation on a smooth surface. Their design supports agile repositioning during autonomous routines where accuracy and responsiveness are critical. This configuration delivers an ideal balance of maneuverability at the front and powerful drive at the back, allowing the robot to move efficiently, accurately, and reliably on a mat based competition field.

## Execution of Motors And Its Engineering Factor

### Motor Used For Steering
![Medium Motor](https://github.com/user-attachments/assets/dfa347a3-80a1-4128-9860-92bd51b8464b)

The medium motor is small and fast, which makes it perfect for turning the front wheels quickly and smoothly. This helps the robot steer accurately when changing direction or making turns on the mat.

### Motor Used For Power
![Large Motor](https://github.com/user-attachments/assets/74ad7641-d676-41ee-bb67-968e484f1934)

The large motor at the back gives the robot its main driving power. It provides strong and steady movement, allowing the robot to move with good speed and stability. This setup steering in the front and power in the back keeps the robot balanced and allows it to move smoothly, turn precisely, and stay in control on the mat field during the competition.

## Engineering Principle

Based on a simple engineering principle "Use the right tool for the right job". Steering doesn’t need a lot of power instead it needs to be quick and light. That’s why we chose the medium motor. It’s smaller, faster, and helps the robot turn smoothly without slowing it down. Driving the robot forward, on the other hand, needs strength and stability. That’s where the large motor comes in. It’s more powerful and gives the robot the force it needs to move across the mat with steady speed and control. Putting it at the back also helps the robot stay balanced and keeps the rear wheels from slipping.

This setup follows the principle of separating movement and control we use a light motor for turning and a strong motor for moving. It makes the robot easier to steer, stronger when driving, and overall more reliable during the competition.

## Execution Of Steering

![Steering (1)](https://github.com/user-attachments/assets/cf54a7b6-2063-4345-b599-76eb8488704c)

Our robot uses a front steering mechanism inspired by the rack and pinion system to control its direction. Instead of a full gear rack, we used a half gear piece connected to a beam. When the gear rotates, it pushes the beam side to side, which turns the front wheels left or right. This setup allows the robot to steer smoothly and accurately, making it easier to change direction on the mat. The system provides controlled and stable movement during turns, helping the robot navigate the field more consistently during competitions.

# Energy and Sensor Management
This section covers the power source of the self driving car and the sensors used to provide it with the necessary information to navigate various challenges. It explains the reasoning behind the selection of each sensor and how they are integrated into the car, along with details on power consumption. A wiring diagram is also included for reference.

## Energy Source
We’ve powered our self-driving car using the EV3 rechargeable battery, which provides a stable energy supply to ensure smooth and consistent operation. This battery serves as the main power source for our robot.
<img width="1335" height="1696" alt="Battery Source" src="https://github.com/user-attachments/assets/5939e7b1-b03f-4d41-bfef-d27653e3c9d5" />

## Sensors
Our self driving car is equipped with two ultrasonic sensors, a gyro sensor, and one Pixy 2 camera. These smart sensors help it detect nearby objects, stay balanced, and recognize signs or colored markers. Working together, they allow the car to drive smoothly, avoid obstacles, and react to its surroundings. This setup enables the vehicle to handle both open areas and challenging obstacle courses.

### Ultrasonic Sensor
Our robot uses two ultrasonic sensors to measure how close it is to the walls on each side of the field. These sensors send out sound waves and wait for them to bounce back. The time it takes tells the robot how far away something is.

**Right Side**

<img width="645" height="410" alt="Ultrasonic Sensor Right Side" src="https://github.com/user-attachments/assets/240ad9aa-f7c5-4d63-92dd-4d4c02cc6567" />

**Left Side**

<img width="648" height="408" alt="Ultrasonic Sensor Left Side" src="https://github.com/user-attachments/assets/ffe279bf-b7bd-43b0-a794-f540f283c56c" />

At first, our robot used color sensor which detects colors on the sides of the field to know when to turn. If it detects a color, it would turn in that direction according to the color detected. This method worked at the start, but it wasn’t always reliable sometimes the colors were hard to detect due to lighting or faded markings. To make things more stable, we switched to using the ultrasonic sensors to guide the robot using the walls. These sensors measure how close the robot is to each side of the field. When both sides show the same distance, the robot stays centered. If one side gets too close to the wall, it gently turns to correct itself. This wall following method made the robot more accurate and allowed it to turn smoothly without needing color lines at all.

### Gyro Sensor
<img width="645" height="1057" alt="Gyro Sensor" src="https://github.com/user-attachments/assets/b28e924f-d0b5-4c19-860f-85fb9f4d8a80" />

A gyro sensor is attached, It helps the robot measure how many full turns or laps it has made. One full spin is 360 degrees, so the sensor keeps adding up the angle as the robot rotates. We programmed the robot to stop when it reaches 1100 degrees, which is just a little more than three full laps. This lets the robot turn around smoothly and return close to its starting point. Once it reaches that point, it stops, making sure it doesn’t over rotate or get off track.

### Pixy Camera 2
<img width="704" height="493" alt="Pixy Camera" src="https://github.com/user-attachments/assets/553b70ca-4ca0-49f2-ba05-81333d3b9074" />

Our robot uses a pixy2 camera helps the robot detect colored objects in front of it. In our setup, it looks for two specific colors: green and red. These colors tell the robot which way to go when it sees an obstacle. If the Pixy2 sees a green object, the robot knows it should turn left. If it sees a red object, the robot will turn right. This helps the robot make quick decisions during the run and choose the correct path based on what color it detects ahead.

# Code & Control Used
![334160](https://github.com/user-attachments/assets/144978b0-b2e9-43ba-a676-fe390cc9cb60)

We used LEGO Mindstorms to program our EV3 robot, managing motor control and sensor input to perform tasks and navigate its environment.

# Code Management

## Open Challenge

## Obstacle Challenge
<img width="1879" height="705" alt="Obstacle Challenge (1)" src="https://github.com/user-attachments/assets/42b72463-3bb3-44de-b486-76440f4b252c" />
<img width="1895" height="702" alt="Obstacle Challenge (5)" src="https://github.com/user-attachments/assets/b599681f-d853-4086-9c5a-091cbaa361a9" />
<img width="1876" height="709" alt="Obstacle Challenge (4)" src="https://github.com/user-attachments/assets/5e46fec1-446e-4796-930a-37df1af20d40" />
<img width="1906" height="690" alt="Obstacle Challenge (3)" src="https://github.com/user-attachments/assets/7132e59a-4c38-4035-8f16-efc3354c0f5f" />
<img width="1884" height="653" alt="Obstacle Challenge (2)" src="https://github.com/user-attachments/assets/c3c631c5-5c37-44fe-a147-b4150a1af4c1" />
<img width="1884" height="653" alt="Obstacle Challenge (2)" src="https://github.com/user-attachments/assets/c3c631c5-5c37-44fe-a147-b4150a1af4c1" />

In the field of autonomous robotics, achieving smooth and intelligent navigation is one of the key challenges. A common task is to design a robot car that can steer itself while staying centered between obstacles or walls, and avoid objects based on visual detection. One effective solution combines ultrasonic sensors for real-time distance measurement with proportional control (P-gain) for steering, and a Pixy Cam to recognize colored obstacles and determine direction. Together, these components create a responsive and adaptable navigation system suitable for various robotics applications.

To maintain the robot's position at the center of a corridor or path, two ultrasonic sensors are placed on the left and right sides of the car. These sensors continuously measure the distance to the nearest  wall on each side. The key idea is to compute the difference between the left and right distances, which serves as the system’s error signal. This error is then multiplied by a proportional gain constant (Kp) to determine the amount of steering adjustment needed. This method, known as proportional control, allows the robot to steer left or right depending on how far it has drifted from the center. If the left distance is greater than the right, the car is too close to the right wall and must steer left to correct its course, and vice versa. This feedback loop ensures the robot continuously makes small adjustments to remain in the center.

While the ultrasonic sensors handle basic centering, the robot also needs to detect and avoid obstacles that may appear directly in its path. This is where the Pixy Cam plays a crucial role. The Pixy Cam is a color based vision sensor capable of recognizing and tracking objects by their color signatures. For this setup, the Pixy Cam is programmed to detect two specific colors: green and red. These colors represent directional commands green signals the car to turn left, while red instructs it to turn right.

When the Pixy Cam detects a green object in the robot’s path, it overrides the normal centering behavior. The robot temporarily shifts control from the ultrasonic sensors to the Pixy Cam’s input, initiating a left turn maneuver to avoid the green obstacle. Similarly, when a red object is detected, the robot turns right. This override mechanism ensures that color-based visual input has priority in urgent navigation situations, such as avoiding an object directly ahead. Once the obstacle is no longer in view, the robot resumes its original path correction using the ultrasonic sensors and proportional steering.

In conclusion, combining two ultrasonic sensors with proportional gain allows a robot car to effectively stay centered between boundaries, providing stability and accuracy. Integrating a Pixy Cam introduces the ability to detect and respond to colored obstacles intelligently. This hybrid approach of sensor fusion using both distance and vision data creates a robust navigation system that is both reactive and adaptive, which is essential in autonomous robotics.

# Engineering Factor

We wanted our LEGO EV3 robot to have vision so it could follow lines, detect colors, and respond to objects. To do that, we used a PixyCam2 smart camera with a special LEGO firmware that lets it work directly with the EV3 brick, just like any other LEGO sensor.

Normally, PixyCam2 connects to things like Arduino or Raspberry Pi, using standard electronic signals. But the EV3 uses special LEGO ports that aren’t directly compatible. To make them work together, we built a custom cable. We took a regular LEGO sensor cable like the kind used for a touch or ultrasonic sensor and cut one end off to expose the wires inside.

Next, we connected those wires to jumper wires, which could plug into the small pins on the PixyCam2’s port. Then we matched the correct wires for power, ground, and data, based on the Pixy LEGO firmware documentation. This allowed the EV3 to recognize the PixyCam2 just like it would a LEGO color or ultrasonic sensor.

We made sure the connections were clean and well insulated, using electrical tape or heat shrink tubing to prevent any short circuits. Since both devices use the same 5V power level, we didn’t need any extra electronics to make it safe.

Once everything was connected, the EV3 was able to communicate with the PixyCam2 right away. The camera sent information about what it could see like object locations and colors and the EV3 used that data to control the robot’s actions. With this setup, our robot could follow lines, detect certain colors, and respond to moving objects just like a more advanced machine, but using only LEGO parts and a smart camera.

In our project, we used the PixyCam2 smart camera with a LEGO Mindstorms EV3 robot, and to mount the camera, we used the metal bracket that comes with the PixyCam2. This small L shaped bracket has screw holes, so it was easy to attach the camera securely to our robot. We mainly used it to lower the camera’s point of view, helping the PixyCam2 better focus on the area directly in front of the robot. We adjusted the tilt by hand before tightening the screws to hold it in place. Even though the bracket isn’t motorized, it kept the camera steady during operation. This simple setup gave us a reliable and flexible way to position the camera without needing any extra parts.

# Improvements
We improved the robot by replacing the color sensor with a gyro sensor, since the color sensor was often unreliable due to poor lighting and being too dependent on surface color. The gyro sensor provides more accurate and consistent turning. We also enhanced the walling system so it rotates more smoothly and better protects the robot when it gets close to walls, especially shielding the Pixy camera from direct contact. To improve space and wiring, we moved the Pixy camera to the top of the robot, as placing it beside the medium motor made the area too crowded and hard to manage wires. Lastly, we upgraded the rear wheels to a larger size, which gave the robot better traction, more stability, and smoother forward movement on the mat.

## 3
![Improvement 3](https://github.com/user-attachments/assets/502308c7-651a-43df-99d6-5a48a1d06814)
<img width="3048" height="1297" alt="Improvement(3 1)" src="https://github.com/user-attachments/assets/f1327b43-0fcf-4032-a2d0-a96ad33585b4" />

## 3.1
<img width="3048" height="4064" alt="Improvement(4)" src="https://github.com/user-attachments/assets/968ec2e9-6dba-4fb6-ac80-c1a62b39e640" />
<img width="3048" height="1328" alt="Improvement(4 1)" src="https://github.com/user-attachments/assets/d3c9dfb7-37f5-47b2-bacd-c943ffc5719e" />

## 3.2
![Improvement 3 2(1)](https://github.com/user-attachments/assets/85c2ae1a-bbd4-44c5-976d-38954a6f7837)
![Improvement 3 2(1 1)](https://github.com/user-attachments/assets/6dfa9d75-57b3-456e-af80-f41d7e5564f7)


> [!NOTE]
> The other improvements is inside the docs folder
> 
# Credits 
