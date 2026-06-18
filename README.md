Engineering materials
====

This repository contains engineering materials of a self-driven vehicle's model participating in the PRO Future Engineers competition in the season 2026

# Content
**docs**- Contains all documentation for the project, including robot architecture, programming flow, assembly instructions, improvement logs, and team information.

**hardware**- Contains EV3 hardware related files such as chassis designs, wiring layouts, and parts lists.

**media**- Contains visual assets such as robot photos, design diagrams, wiring schematics, and video recordings.

**software**-  Contains all Python source code for the EV3 robot. This includes the main control program developed using Visual Studio Code, which manages motor control and sensor input to perform tasks and navigate the environment.


> [!NOTE]
> This README.md doesn't contain all the information, some details are inside the folders

## Introduction
This document presents the technical specifications and design details of the TLGC Catalyst Future Engineer's Team B's autonomous vehicle robot for the 2026 Philippine Robotics Olympiad.

## TLGC Robotics Catalyst Team
Our team consists of two dedicated members who carefully manage the key aspects of our autonomous vehicle’s development. Representing Toplink Global College, the Future Engineers Team B is a passionate group committed to optimizing the essential electromechanical systems that drive our fully autonomous robot.


**Tymothy P. Dobla**

[![Facebook](https://img.shields.io/badge/Facebook-Follow-1877F2?style=flat&logo=facebook&logoColor=white)](https://www.facebook.com/iwwfyeiitahy)

**Zen Kobin N. Tevar**

[![Facebook](https://img.shields.io/badge/Facebook-Follow-1877F2?style=flat&logo=facebook&logoColor=white)](https://www.facebook.com/tevar.zenkobin)

> [!NOTE]
> The team information is at the docs folder
# Materials
Our autonomous self-driving car was developed using the LEGO Mindstorms EV3 Education Set (45544), the LEGO Mindstorms Education EV3 Expansion Set (45560), the LEGO Education Spike Prime Set (45678), and the LEGO Education Spike Prime Expansion Set (45681).

<img width="866" height="288" alt="Untitled_design__6_-removebg-preview" src="https://github.com/user-attachments/assets/0ea88ee8-386f-4312-9e13-1c93492f8049" />
<img width="866" height="288" alt="Untitled_design__7_-removebg-preview" src="https://github.com/user-attachments/assets/cb51d87a-07d0-4948-b8ef-754658cd8483" />

> [!NOTE]
> The list of the materials used in our robot is inside the hardware folder

# Chassis

## Selection Of Wheel
<img width="4096" height="3072" alt="1" src="https://github.com/user-attachments/assets/bb22fd77-4024-455b-adb9-6293aaf76dae" />

We selected the Wheel 39367 at the front and the Wheel 49295 at the rear to optimize our robot’s performance on a mat field. The front wheels are lightweight and have a low friction, narrow profile, which allows for quick, smooth turns with minimal resistance perfect for precise navigation on a smooth surface. Their design supports agile repositioning during autonomous routines where accuracy and responsiveness are critical. This configuration delivers an ideal balance of maneuverability at the front and powerful drive at the back, allowing the robot to move efficiently, accurately, and reliably on a mat based competition field

## Execution of Motors And Its Engineering Factor

### Motor Used For Steering
<img width="4096" height="3072" alt="2" src="https://github.com/user-attachments/assets/2ae7c269-d4cf-4a52-9c45-5ccee5994e14" />

The medium motor is small and fast, which makes it perfect for turning the front wheels quickly and smoothly. This helps the robot steer accurately when changing direction or making turns on the mat.

### Motor Used For Power
<img width="4096" height="3072" alt="3" src="https://github.com/user-attachments/assets/987bab28-7492-47af-92b6-1cea302fe0a4" />

The medium motor at the back gives the robot its main driving power. It provides strong and steady movement, allowing the robot to move with good speed and stability. This setup steering in the front and power in the back keeps the robot balanced and allows it to move smoothly, turn precisely, and stay in control on the mat field during the competition.

## Engineering Principle

Based on the simple engineering principle "use the right tool for the job," steering doesn’t need a lot of power instead it needs to be quick and light. That’s why we chose a medium motor it’s smaller, faster, and helps the robot turn smoothly without slowing down. Driving the robot forward, on the other hand, requires speed and stability. While we used a medium motor here as well, we geared it for more force to give the robot the power it needs to move across the mat with steady speed and control. Placing the drive motors at the back also helps the robot stay balanced and keeps the rear wheels from slipping.

This setup follows the principle of separating movement and control by using one light motor for turning and another for moving. This configuration makes the robot easier to steer, stronger when driving, and overall more reliable during the competition.

## Execution Of Steering
<img width="4096" height="3072" alt="4" src="https://github.com/user-attachments/assets/e3b5a4df-8430-4675-a292-00523f9adf81" />

Our robot uses a front steering mechanism inspired by the rack and pinion system to control its direction. Instead of a full gear rack, we used a half gear piece connected to a beam. When the gear rotates, it pushes the beam side to side, which turns the front wheels left or right. This setup allows the robot to steer smoothly and accurately, making it easier to change direction on the mat. The system provides controlled and stable movement during turns, helping the robot navigate the field more consistently during competitions.

# Energy and Sensor Management
This section covers the power source of the self driving car and the sensors used to provide it with the necessary information to navigate various challenges. It explains the reasoning behind the selection of each sensor and how they are integrated into the car, along with details on power consumption. A wiring diagram is also included for reference.

## Energy Source
We’ve powered our self-driving car using the EV3 rechargeable battery, which provides a stable energy supply to ensure smooth and consistent operation. This battery serves as the main power source for our robot.

<img width="1335" height="1696" alt="Battery Source" src="https://github.com/user-attachments/assets/5939e7b1-b03f-4d41-bfef-d27653e3c9d5" />

### Ultrasonic Sensor
Our robot utilizes an ultrasonic sensor to determine its distance from the field wall. The sensor emits sound waves and measures the time it takes for the echo to return, calculating the exact distance based on that delay.

<img width="4096" height="3072" alt="5" src="https://github.com/user-attachments/assets/caeafd40-795d-46e8-b68f-4dcf80592b1c" />

Originally, our robot relied on two ultrasonic sensors and a PID controller to know when to turn. If a distance change was detected, the robot would turn in that direction accordingly. This method worked at the start, but it proved unreliable at times, making turns hard to execute. To make the system more stable, we switched to using a single ultrasonic sensor to guide the robot using the wall. This sensor measures how close the robot is to the side of the field. By maintaining a set distance from the wall, the robot stays perfectly on track. If it gets too close or too far, it gently turns to correct itself. This wall following method made the robot significantly more accurate, allowing it to turn smoothly without needing multiple sensors at all.

## Gyro Sensor
<img width="4096" height="3072" alt="7" src="https://github.com/user-attachments/assets/a522c1d7-b2fd-4519-b60e-4f7b45f8ba33" />

A gyro sensor is attached to help the robot track how many full turns or laps it has completed. Because one full spin equals 360 degrees, the sensor continuously adds up the total angle as the robot rotates. We programmed the robot to stop once it hits 1100 degrees, which is slightly more than three full laps. This allows the robot to spin around smoothly and finish up close to its original starting point. As soon as it reaches that specific angle, it stops, ensuring it doesn’t over-rotate or drift off track.

## Pixy Camera
<img width="4096" height="3072" alt="6" src="https://github.com/user-attachments/assets/91b93e8e-60b3-4f5e-9ec4-d627574eb2b7" />

Our robot uses a Pixy2 camera to detect colored objects in front of it. In this setup, it looks for two specific colors, green and red, which tell the robot which way to go when it encounters an obstacle. If the Pixy2 sees a green object, the robot knows to turn left, and if it sees a red object, it turns right. This helps the robot make quick decisions during the run and choose the correct path based on the color it detects ahead.

## Color Sensor
<img width="4096" height="3072" alt="8" src="https://github.com/user-attachments/assets/5eff91c4-64ba-40b7-9d6f-d4ca0b37592c" />

A color sensor is attached, helping the robot count laps by tracking colored lines on the track. As it drives, the sensor looks down at the floor to detect when the surface color changes. We programmed the robot to recognize the blue and orange lines, adding a lap to its counter each time it crosses them. This allows the robot to keep an accurate tally of its progress automatically. Once it reaches the target number of laps, it stops right on cue, ensuring it finishes its run precisely where it's supposed to.

## Code & Control Used
<img width="1127" height="578" alt="62a79050e42d729d928b1756" src="https://github.com/user-attachments/assets/d2981cff-b953-4dc6-96d0-b0aa0891b07b" />

We used Python in Visual Studio Code to program our EV3 robot, managing motor control and sensor input to perform tasks and navigate its environment.

# Code Management
## Open challenge
<img width="1478" height="913" alt="Open" src="https://github.com/user-attachments/assets/d27397c0-d830-46f2-9e16-9f51a0442c73" />

> [!NOTE]
> The code starts from the top to bottom

To maintain our robot's direction and precision, we placed a gyroscope and a forward-facing ultrasonic sensor on the robot to continuously measure its heading and the distance to any obstacle ahead. The key idea is to calculate the difference between the gyro angle and the target heading, treating this deviation as the system’s error. We feed this error into an LQR-augmented Stanley controller that automatically adjusts the steering based on the robot's current speed. For example, if the robot drifts past the target angle, it steers in the opposite direction to correct itself, while an integrated memory term actively eliminates any slow drift on straightaways. This feedback loop allows the robot to constantly make small, fluid adjustments to stay on track, while automatically initiating a sharp, 90-degree turn whenever the ultrasonic sensor detects a wall ahead.

## Obstacle challenge
<img width="1476" height="915" alt="Obstacle" src="https://github.com/user-attachments/assets/d26f020d-9aa0-4d57-a468-3aacb3af4a9b" />

> [!NOTE]
> The code starts from the top to bottom

Our robot is built for fully autonomous navigation, combining a Gyro sensor, a front ultrasonic sensor, and a Pixy Cam to master complex courses and avoid colored pillars. The Gyro sensor serves as the robot's internal compass, continuously tracking the driving angle to ensure it stays centered. Utilizing a proportional control method, the system automatically corrects its trajectory based on tracking error, meaning the farther the robot drifts from the center, the sharper it steers to get back on track.

However, staying centered is only half the challenge when facing sharp corners. To manage these, the front ultrasonic sensor constantly measures the distance to oncoming walls, automatically triggering a precise mechanical turn sequence whenever a boundary gets too close. Immediately after a turn, the Pixy Cam takes charge to scan for traffic pillars. Because the camera is connected to the steering mechanism, it can move a full 180 degrees to easily detect obstacles positioned on the sides. It is trained to recognize specific colors: encountering a red pillar directs the robot to steer right, while green dictates a turn to the left. During these encounters, the robot temporarily overrides its path sensors to prioritize these visual cues, safely bypassing the obstacle before seamlessly switching back to gyroscopic stability for a reliable, adaptable run.

# Engineering Factor
We wanted our LEGO EV3 robot to have vision so it could follow lines, detect colors, and respond to objects. To do this, we used a PixyCam2 smart camera equipped with specialized LEGO firmware.

Because the EV3 uses proprietary ports that aren't natively compatible with the PixyCam's standard interface, we built a custom cable by cutting one end off a regular LEGO sensor cable to expose and splice the internal wires. We then coded the robot in Python, which allowed the EV3 brick to communicate with the PixyCam2 seamlessly, treating it just like any other standard LEGO sensor.

<img width="420" height="594" alt="595108374-e59a5707-6b38-432d-afe1-8f324c9f6016" src="https://github.com/user-attachments/assets/2993db83-a94a-44c1-bcc8-29cafa5f192b" />

Next, we attached those wires to jumper wires compatible with the PixyCam2's small pin port. Referencing the Pixy LEGO firmware documentation, we matched the corresponding power, ground, and data lines, enabling the EV3 to recognize the PixyCam2 as a standard LEGO color or ultrasonic sensor. To prevent short circuits, we insulated the connections using electrical tape or heat-shrink tubing. Because both systems operate on a shared 5V power level, we did not need additional voltage conversion or protective circuitry.

<img width="433" height="577" alt="595111388-99acb471-f484-4434-b546-ef1eebb13a45" src="https://github.com/user-attachments/assets/2b11fe1e-415c-4d78-99eb-525341a02dce" />

Once everything was connected, our Python script established immediate communication between the EV3 brick and the PixyCam2. The camera continuously streamed real-time data such as object locations and color signatures which our Python code processed to dynamically control the robot's motors and actions. With this software driven integration, our robot was able to follow lines, detect specific color targets, and track moving objects, delivering the high-performance responsiveness of an advanced machine using just a smart camera and LEGO parts.

To physically support this setup, we mounted the PixyCam2 using the small, L-shaped metal bracket that comes with the camera. By fastening it through the built-in screw holes, we were able to lower the camera's point of view, allowing it to focus sharply on the area directly in front of the robot. We manually adjusted the tilt before tightening the screws to lock it into position; even though this mounting setup wasn't motorized, it kept the camera perfectly stable during operation without requiring any extra parts.

# Improvements

We upgraded the robot by switching from two medium motors down to just one medium motor for driving, which allowed for a more compact and streamlined design. We also reduced our sensor setup from two ultrasonic sensors to just one ultrasonic sensor, freeing up enough physical space to integrate both a color sensor and a gyro sensor for much better navigation.

Regarding the vision system, we moved the camera from the top of the robot to the front, positioning it right above the steering motor for a clearer view. Lastly, we changed our steering setup, while our first robot used small wheels for steering, we have now upgraded to slightly bigger steering wheels while keeping the larger rear wheels, giving the robot improved turning precision, better traction, and smoother overall movement on the mat.

# 1

<img width="1920" height="957" alt="1" src="https://github.com/user-attachments/assets/74a09851-1681-48d9-83a9-6d009160ead9" />
<img width="1920" height="957" alt="2" src="https://github.com/user-attachments/assets/73a21e8e-a449-432d-89e1-bcc35e51a817" />
<img width="1920" height="957" alt="3" src="https://github.com/user-attachments/assets/9d5a0afc-e4a0-44b0-a906-02c0f47724e1" />
<img width="1920" height="957" alt="4" src="https://github.com/user-attachments/assets/236fa3a2-372c-426b-8cf3-4c5b3474a08c" />
<img width="1920" height="957" alt="5" src="https://github.com/user-attachments/assets/bc0c3472-2f30-4924-99c7-b77c20a2038c" />
<img width="1920" height="957" alt="6" src="https://github.com/user-attachments/assets/f4a51b66-668c-48d6-b97b-b3c7b8385107" />

# 1.1

<img width="1920" height="957" alt="7" src="https://github.com/user-attachments/assets/8053415a-9663-4840-9c07-4e7452576175" />
<img width="1920" height="957" alt="8" src="https://github.com/user-attachments/assets/469b1bb7-872b-4104-b216-dc78a3d09123" />
<img width="1920" height="957" alt="9" src="https://github.com/user-attachments/assets/5c7d24f3-1293-4c8a-bbc4-61010473bfd2" />
<img width="1920" height="957" alt="10" src="https://github.com/user-attachments/assets/ddc7a0c2-00c1-4b68-adce-5ae0431f2c71" />
<img width="1920" height="957" alt="11" src="https://github.com/user-attachments/assets/a22aa35e-bd4c-43d1-8f64-84b726561f9b" />
<img width="1920" height="957" alt="12" src="https://github.com/user-attachments/assets/44260112-6be4-4185-8e1a-71e5a5feed31" />

# 2

<img width="1920" height="957" alt="1" src="https://github.com/user-attachments/assets/58e31112-e8d1-4d8b-99c2-a2956c1555c8" />
<img width="1920" height="957" alt="2" src="https://github.com/user-attachments/assets/dc969be1-ecdb-442b-92b9-17187fe9e01d" />
<img width="1920" height="957" alt="3" src="https://github.com/user-attachments/assets/dc8256e9-8b89-4dd9-8353-83e7d68503dd" />
<img width="1920" height="957" alt="4" src="https://github.com/user-attachments/assets/3e166ff1-7859-4e45-b188-f79f6e558314" />
<img width="1920" height="957" alt="5" src="https://github.com/user-attachments/assets/be946220-667f-4390-a73c-7b0fe597ebf4" />
<img width="1920" height="957" alt="6" src="https://github.com/user-attachments/assets/21329e05-fe68-4522-aa03-2af42d4d5a34" />

# Credits
We are deeply proud to represent our school, Toplink Global College Inc., which constantly supports our passion for innovation and robotics. We also want to extend our heartfelt thanks to our beloved coach, your patience, guidance, and continuous encouragement truly inspired us throughout this journey. Finally, we express our sincere appreciation to LEGO Mindstorms; the high-quality components and flexible design of the EV3 kit provided the hands-on experience that allowed us to explore, build, and bring this project to life.

