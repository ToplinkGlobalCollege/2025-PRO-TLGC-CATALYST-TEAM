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
Our autonomous self-driving car was developed using the LEGO Mindstorms EV3 Education Set (45544)
![45544-1-0-removebg-preview](https://github.com/user-attachments/assets/7b6e5ab7-0c0d-43d3-89e1-20ac8d9be258)

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

