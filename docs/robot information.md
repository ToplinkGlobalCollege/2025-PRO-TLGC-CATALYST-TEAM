# Robot Info
![TLGC Catalyst Robot](https://github.com/user-attachments/assets/9eab7df2-d8ef-4700-9e72-295631cccf4a)
**Name:** Katalista
                                                                                                                                                                   
**Weight:** 0.8 kg
                                                                                                                                                                   
**Size:** 270mm x 170mm with 150mm in height

> [!NOTE]
> Did you know why we named our robot katalista?
> Well katalista is more than just a name. It represents who we are, where we come from, and what we aim to do as a team.

# A short trivia!
The word "Katalista" is the Tagalog equivalent of the English word "Catalyst." In science, a catalyst is a substance that speeds up a chemical reaction without being consumed or changed in the process. It plays a vital role—it doesn’t cause the reaction itself, but it makes it happen faster, easier, and with less energy.

But over time, the meaning of the word “catalyst” has grown far beyond chemistry. In modern usage, especially in engineering, business, technology, and life, a catalyst is:

“A person, idea, event, or thing that causes or accelerates change.”

In this context, a catalyst can be someone who inspires innovation, an event that sparks transformation, or a tool that changes how things are done. A catalyst is something that helps progress begin, speeds it up, or shifts its direction for the better, without needing to take the spotlight.

So why did we name our robot Katalista?

First, it reflects our identity. Our team—TLGC Catalyst—is proudly based in the Philippines, and using Tagalog for the name honors our language, culture, and local roots. Naming our robot “Katalista” connects our engineering journey to who we are as Filipinos.

Second, it reflects our mission. We began training in May 2025, just three months ago. In that short time, we’ve learned, built, and grown rapidly. Like a true catalyst, our robot symbolizes rapid progress, intelligent problem-solving, and the ability to spark change—in ourselves, in our community, and in the world of robotics.

Katalista is not just a machine. It is a symbol of transformation, a driver of innovation, and a promoter of change. Just as a chemical catalyst makes reactions more efficient, our robot is designed to make systems smarter, processes faster, and ideas come to life.

With Katalista, we don’t just participate—we initiate.
We don’t just follow change—we drive it.                                                                                                                             
# Mobility

## Drive System Used
Our EV3 autonomous car uses a single LEGO Large Motor to drive forward. The motor is connected to the main wheels, providing consistent power and speed for straight movement. Because we only used one motor. The Large Motor’s built in rotation sensor helps us measure how far the car moves, making it easier to control and program. This simple setup keeps the robot lightweight, efficient, and ideal for straightforward autonomous driving.

## Turning Strategy
Our EV3 autonomous robot employs a custom front wheel steering mechanism based on the principles of a rack and pinion system. Instead of using a traditional gear rack, the design incorporates a half gear element attached to a beam that functions as a simplified rack. As the gear rotates driven by a motor or manually pre set it translates the beam laterally, causing the front wheels to pivot left or right. This mechanical linkage enables smooth and proportional steering control. The configuration allows for stable directional changes and improves maneuverability on the field, especially during precise turns and alignment tasks. The simplicity of this setup also reduces mechanical complexity while maintaining reliable performance during competition runs.

## Motors Used
### Large Motor
<img width="567" height="440" alt="45502-1-removebg-preview" src="https://github.com/user-attachments/assets/6717787f-a92a-45a7-a58c-52b32eb69805" />

### Medium Motor
<img width="333" height="333" alt="ar-ev3-medium-servo-motor-1139-removebg-preview" src="https://github.com/user-attachments/assets/b7e79cc4-5961-4763-a34b-bb36f2e45b51" />

## Why we chose this system
We used the Large Motor to drive our robot forward because it’s strong and can handle the weight of the robot. It gives enough power to move smoothly across the mat and works well for straight driving. The Medium Motor is smaller and quicker, so we used it for steering. It’s just the right size for turning the front wheels without making the robot too heavy or bulky. This combination of one strong motor for driving and one small motor for steering helped make our robot both powerful and easy to control.

# Power System
## Main Power Source
We’ve powered our self-driving car using the EV3 rechargeable battery, which provides a stable energy supply to ensure smooth and consistent operation. This battery serves as the main power source for our robot.
<img width="1335" height="1696" alt="Battery Source" src="https://github.com/user-attachments/assets/5939e7b1-b03f-4d41-bfef-d27653e3c9d5" />

## Voltage and Current Details
Our EV3 robot uses a rechargeable lithium ion battery that provides a voltage of 7.2 volts and a capacity of 2050 mAh. This means the battery can supply 2.05 amps of current for one hour before needing a recharge, depending on how much power the robot uses. The battery is powerful enough to run the EV3 brick, motors, and sensors all at once. It also keeps the power stable, which helps the robot perform consistently. Since it’s rechargeable, it’s more convenient and cost effective than using disposable batteries, especially for long practices and competitions.

## Power Safety & Management
To keep our EV3 robot safe and reliable, we followed good power safety and management practices. We made sure the rechargeable battery was always fully charged before each run, and we turned off the EV3 brick after use to save power and prevent overheating. To avoid short circuits or accidental contact between exposed wires or metal parts, we also applied insulating materials around key connections. This helped protect both the robot and the people handling it. By managing power carefully and using insulation, we made sure the robot stayed safe, stable, and ready for every test and competition round.
# Obstacle Avoidment

## Sensors Used for Detection
### Pixy Cam 2
<img width="378" height="480" alt="PIXY2-Camera-378x480-removebg-preview" src="https://github.com/user-attachments/assets/91683fe7-6888-4859-9258-9e515214c627" />

## Strategy
To improve our robot’s ability to detect visual markers and environmental cues, we mounted the Pixy Cam on top of the robot. This elevated position gives the camera a wider field of view, allowing it to detect obstacles from a greater distance and with fewer blind spots. Placing the camera higher also prevents it from being blocked by parts of the robot’s frame, which improves both its accuracy and response time during object recognition.

For navigation, we angled the ultrasonic sensors at 45 degrees on each side of the robot. This strategic placement enables the sensors to measure both forward and side distances to nearby walls. As a result, the robot receives more reliable and consistent distance data, helping it stay centered in narrow paths or corridors. By continuously comparing the left and right sensor values, the robot can make precise steering adjustments to maintain a straight and balanced course critical for avoiding collisions and achieving consistent lap performance.

Additionally, as part of our walling strategy, we installed a free rolling wheel on the side of the robot to serve as a stabilizer. This wheel gently rolls along the walls surface without causing friction or drag. It helps the robot stay aligned by allowing slight contact with the wall, effectively “hugging” it without scraping or stopping, which results in smoother and more stable navigation.
