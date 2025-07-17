> [!TIP]
> We recommend using dark mode when reading this repository
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
[![Facebook](https://img.shields.io/badge/Facebook-Page-1877F2?style=flat&logo=facebook&logoColor=white)][(https://facebook.com/yourusername](https://www.facebook.com/share/16bncUjy9o/   ))                                                                                                               
https://www.instagram.com/beezlebobbb?igsh=aDJhdGhrMmpxZzFn

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
<img width="1724" height="189" alt="Screenshot 2025-07-17 150729" src="https://github.com/user-attachments/assets/02fc3278-f444-4d90-a65b-86cbf910a10c" />
<img width="1849" height="269" alt="Screenshot 2025-07-17 150752" src="https://github.com/user-attachments/assets/b3a832b6-4d12-4b35-bd53-028e5075961b" />
<img width="1621" height="233" alt="Screenshot 2025-07-17 150808" src="https://github.com/user-attachments/assets/15b256b6-7da4-4d13-9375-b8e09984ce1b" />

> [!NOTE]
> The code starts from the top to bottom 

To maintain our robot's position at the center of a corridor or path, we placed two ultrasonic sensors on the left and right sides of the chassis. These sensors continuously measure the distance to the nearest wall on each side. The key idea is to calculate the difference between the left and right distances this difference is treated as the system’s error. We multiply this error by a proportional gain constant to determine how much the robot should steer. This method, called proportional control, lets our robot automatically adjust its direction depending on how far it has drifted from the center. For example, if the left distance is greater than the right, the robot is too close to the right wall and needs to steer left to correct itself, and vice versa. This feedback system allows the robot to constantly make small adjustments to stay centered.

## Obstacle Challenge
<img width="1815" height="704" alt="Screenshot 2025-07-17 145845" src="https://github.com/user-attachments/assets/e561b8e3-3959-4bf5-8ebd-f3238a258bfb" />
<img width="1144" height="458" alt="Screenshot 2025-07-17 145955" src="https://github.com/user-attachments/assets/d209d8fa-bd4e-4f5b-a84b-98e651823204" />
<img width="1082" height="227" alt="Screenshot 2025-07-17 150017" src="https://github.com/user-attachments/assets/dc8bb6aa-6b2f-46f3-8302-d2df28e588a5" />
<img width="1200" height="448" alt="Screenshot 2025-07-17 150042" src="https://github.com/user-attachments/assets/984bcb9a-e719-4ac4-8ae9-12be06834efb" />
<img width="1752" height="466" alt="Screenshot 2025-07-17 150108" src="https://github.com/user-attachments/assets/eeb88ce5-848e-4b8e-8636-afbda827438d" />
<img width="1886" height="444" alt="Screenshot 2025-07-17 150135" src="https://github.com/user-attachments/assets/924e5265-7e6e-44f1-8d47-b8b5cb50b74a" />
<img width="1050" height="429" alt="Screenshot 2025-07-17 150352" src="https://github.com/user-attachments/assets/752be521-fa7b-4db4-9e98-e4ea5730cd8d" />

> [!NOTE]
> The code starts from the top to bottom

Our robot was designed to move by itself, stay centered between walls, and avoid obstacles in its path. To do this, we combined two types of sensors: ultrasonic sensors and a color detecting Pixy Cam. The ultrasonic sensors are placed on the left and right sides of the robot. These sensors act like the robot’s ears, constantly measuring the distance from each wall. If the robot gets too close to one side, it automatically steers back toward the center. This is done using a method called proportional control, where the robot adjusts its steering based on how off center it is the farther it is from the middle, the more it turns to correct its path.

But staying centered isn’t enough. The robot also needs to avoid obstacles that might appear directly in front of it. That’s where the Pixy Cam comes in. The camera is trained to recognize specific colors: green means turn left, and red means turn right. When the Pixy Cam sees a green or red object, the robot temporarily stops using the side sensors and instead follows the camera’s command to avoid the obstacle. Once the object is no longer in sight, the robot switches back to using the ultrasonic sensors to stay centered.

By combining distance sensors and visual detection, our robot can smoothly and intelligently navigate its environment. It knows when to stay centered and when to react quickly to objects in its way, making it reliable and adaptable for autonomous tasks.

# Engineering Factor

We wanted our LEGO EV3 robot to have vision so it could follow lines, detect colors, and respond to objects. To do that, we used a PixyCam2 smart camera with a special LEGO firmware that lets it work directly with the EV3 brick, just like any other LEGO sensor.

Normally, PixyCam2 connects to things like Arduino or Raspberry Pi, using standard electronic signals. But the EV3 uses special LEGO ports that aren’t directly compatible. To make them work together, we built a custom cable. We took a regular LEGO sensor cable like the kind used for a touch or ultrasonic sensor and cut one end off to expose the wires inside.

<img width="420" height="594" alt="Untitled_design-removebg-preview" src="https://github.com/user-attachments/assets/b59880e3-d8ba-442a-bb2c-79cf9c450bc4" />

Next, we connected those wires to jumper wires, which could plug into the small pins on the PixyCam2’s port. Then we matched the correct wires for power, ground, and data, based on the Pixy LEGO firmware documentation. This allowed the EV3 to recognize the PixyCam2 just like it would a LEGO color or ultrasonic sensor.

We made sure the connections were clean and well insulated, using electrical tape or heat shrink tubing to prevent any short circuits. Since both devices use the same 5V power level, we didn’t need any extra electronics to make it safe.

<img width="433" height="577" alt="IMG_20250717_152335_773-removebg-preview" src="https://github.com/user-attachments/assets/da56e3f1-6093-4f0d-b7e6-b483c668475c" />

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
# Credits 
We would like to express our heartfelt appreciation to LEGO Mindstorms for providing the robotics set that made this project possible. The high quality components and flexible design of the EV3 kit allowed us to explore, build, and learn through hands on experience. We are also deeply thankful to our beloved coach, whose patience, guidance, and encouragement inspired us throughout this journey. Finally, we are proud to represent our school, which continues to support our passion for robotics and innovation.


