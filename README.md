# Introduction
This engineering documentation presents the technical details and design specifications of the autonomous vehicle robot developed by the TLGC Catalyst Future Engineer's Team for the Philippine Robotics Olympiad 2025

# Content
**docs**- Contains all documentation for the project, including robot architecture, programming flow, assembly instructions, improvement logs, and team information.

**hardware**- Contains EV3 hardware-related files such as chassis designs, wiring layouts, and parts lists.

**media**- Contains visual assets such as robot photos, design diagrams, wiring schematics, and video recordings.

**software**-  Contains all source code for the EV3 robot. This includes the main control program developed using LEGO Mindstorms, which manages motor control and sensor input to perform tasks and navigate the environment.

> [!NOTE]
> This README.md doesn't contain all the information, some details are inside the folders

# TLGC Robotics Catalyst Team
Our team consists of three dedicated members who carefully manage the key aspects of our autonomous vehicle’s development. Representing Toplink Global College, the Future Engineers Team is a passionate group committed to optimizing the essential electromechanical systems that drive our fully autonomous robot.

**Marc Vincent B. Cortez**    
**Team Captain/Coder**

**Andrei Jerome M. Manalansan**                                                                                                                                
**Team Builder/Placer**                    
**Age:17**          
Andrei is a grade 12 student at Toplink Global College Inc. He enjoys working with robots, mainly for school projects and competitions. He likes solving problems and figuring out how to make robots move through different challenges. When He's not working on robots, watches movies like Stranger Things, He also loves playing video games.


**Yasser M. Lapaz**           
**Team Placer/Coder**

# Materials
Our autonomous self-driving car was developed using the LEGO Mindstorms EV3 Education Set (45544) and LEGO Mindstorms Education EV3 Expansion Set (45544)
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

![Steering](https://github.com/user-attachments/assets/b5ffc7ad-a860-4c00-b7b5-96ffdd53739f)

Our robot uses a rack-and-pinion steering system at the front to control its direction. This setup works by turning a gear that moves a bar side to side, which makes the front wheels turn left or right. It allows the robot to steer smoothly and accurately, making it easy to change direction on the mat. With this type of steering, the robot can move in a controlled and stable way, especially during turns. The system helps ensure that movement stays smooth and consistent, which is important for navigating around the field during the competition.

# Energy and Sensor Management
This section covers the power source of the self-driving car and the sensors used to provide it with the necessary information to navigate various challenges. It explains the reasoning behind the selection of each sensor and how they are integrated into the car, along with details on power consumption. A wiring diagram is also included for reference.

## Energy Source
We’ve powered our self-driving car using the EV3 rechargeable battery, which provides a stable energy supply to ensure smooth and consistent operation. This battery serves as the main power source for our robot.
<img width="1335" height="1696" alt="Battery Source" src="https://github.com/user-attachments/assets/5939e7b1-b03f-4d41-bfef-d27653e3c9d5" />

## Sensors
Our self-driving car is equipped with two ultrasonic sensors, a gyro sensor, and one Pixy 2 camera. These smart sensors help it detect nearby objects, stay balanced, and recognize signs or colored markers. Working together, they allow the car to drive smoothly, avoid obstacles, and react to its surroundings. This setup enables the vehicle to handle both open areas and challenging obstacle courses.

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
