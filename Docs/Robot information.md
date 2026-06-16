# Robot info
<img width="800" height="600" alt="ARC" src="https://github.com/user-attachments/assets/ebfba54b-69bd-4acb-864d-184d471ae257" />

**Name:** Arc

**Weight:** 0.66

**Size:** 251mm x 120mm with 180mm in height


> [!NOTE]
>Ever wonder why we chose the name Arc? It’s far more than just a name on a robot. For us, Arc is the continuous curve where our backgrounds meet, our team unites, and what we aim to do as a team.

# A short trivia!
The Meaning of "Arc"

​In mathematics, an arc is a continuous portion of a curved line or the smooth path along the circumference of a circle. It represents a fluid transition, a connection between distinct points, and the trajectory of continuous motion. It plays a vital role, it doesn’t just exist in space, but it makes movement adaptive, seamless, and perfectly directed.

​But over time, the meaning of the word “arc” has grown far beyond graphs and geometry. In modern usage, especially in engineering, storytelling, and life, an arc is:

​“A journey of transformation, a bridge connecting separate points, and a continuous momentum that drives growth forward.”

​In this context, an arc can be a path of development that elevates a team, a focal point that bridges different ideas, or a standard of adaptability that defines how challenges are overcome. An arc is something that spans gaps, maintains a powerful trajectory, and ensures dynamic progress, without needing to take the spotlight.

​So why did we name Our Robot Arc?

​First, it reflects our identity. ​Our team, TLGC Catalyst, proudly carries our heritage into the world of technology. In Filipino culture, we value deep connections, community, and the bridges we build to lift each other up. The name "Arc" was directly inspired by the mathematical concept because of how our robot sees and navigates: through a camera that sweeps in a half circle, a 180 degree field of vision. Naming our robot “Arc” connects our engineering journey to our local roots, reflecting the Filipino spirit of resilience, continuous growth, and a sweeping, upward path forward.

​Second, it reflects our mission.

​We began training in April 2026, just two months ago. In that short time, we’ve learned, built, and grown rapidly. Like a true arc which tracks a powerful narrative of progress from start to finish our robot symbolizes our rapid transformation, intelligent problem solving, and the ability to act as the bridge for transformation in ourselves, in our community, and in the world of robotics.

​Driven by Trajectory

​Arc is not just a machine. It is a symbol of connection, a driver of innovation, and a promoter of momentum. Just as a mathematical arc gives order and direction to a curve, our robot is designed to make systems smarter, transitions smoother, and ideas come to life.

​With Arc, we don’t just move we bridge.
We don’t just wander we drive the way forward.

# Mobility

## Drive System Used
Our EV3 autonomous car uses one Medium Motor to drive forward, powering the main wheels. This single-motor setup provides consistent speed for straight movement while allowing us to precisely control distance. By utilizing one Medium Motor instead of two Medium Motors, the car gains a more compact design and reduced weight, making it highly agile. Additionally, the built in rotation sensor in the motor helps us measure exactly how far the wheels rotate, allowing for precise tracking, smoother acceleration, and highly accurate autonomous navigation.

## Turning Strategy
Our EV3 robot uses a custom steering setup for the front wheels. Instead of a normal gear rack, we attached a half gear to a beam to make a simple rack. When the motor turns, this gear moves the beam sideways to turn the front wheels left or right. This setup makes the steering smooth and precise, which helps the robot turn well and stay steady. By keeping the design simple, we made it less complicated and made sure it works reliably during runs.

## Motors Used
### Medium Motor
<img width="333" height="333" alt="597100100-c9c5783b-2a71-4b0c-8473-82a2a08ac405" src="https://github.com/user-attachments/assets/958106c7-8fa5-4364-9379-6dc4a0f5b66d" />

## Why we chose this system
We used one Medium Motor to drive our robot because it is compact, lightweight, and provides plenty of power for our needs. This single motor setup efficiently drives the wheels to move the robot smoothly across the mat and ensure precise control. Choosing a single Medium Motor instead of two medium motors keeps the robot from becoming too heavy, bulky, or overly complex, while still offering incredible maneuverability during runs

# Power System
## Main Power Source
We’ve powered our self driving car using the EV3 rechargeable battery, which provides a stable energy supply to ensure smooth and consistent operation. This battery serves as the main power source for our robot
<img width="1335" height="1696" alt="465793506-5939e7b1-b03f-4d41-bfef-d27653e3c9d5" src="https://github.com/user-attachments/assets/1654a735-59d6-4868-95e6-60dd627a598f" />

## Voltage and Current Details
Our EV3 robot runs on a 7.2V rechargeable lithium-ion battery with a 2050 mAh capacity. While its actual operation time depends on the robot's real-time power draw, this battery is capable of supplying a steady 2.05 amps of current for one full hour. It seamlessly powers the EV3 brick, motors, and sensors all at once to ensure a consistent voltage for uniform performance. Much more practical and economical than standard disposable batteries, this rechargeable power pack is perfect for prolonged training runs and competitions.

## Power Safety & Management
To guarantee the reliability and safety of the EV3 robot, we followed strict insulation and power management protocols. Before every run, the rechargeable battery was fully charged, and we powered down the EV3 brick immediately after use to prevent overheating and conserve energy. We also applied insulating materials to critical connections, removing the risk of accidental contact with exposed wiring or short circuits. These proactive measures protected the team and the hardware alike, ensuring the robot stayed stable and ready for competition.

# Obstacle Avoidment

## Sensors Used for Detection
### Pixy Cam 2
<img width="645" height="634" alt="597102144-5753737b-6624-4d70-8d01-149ea59d3588" src="https://github.com/user-attachments/assets/eac6fe5b-9094-40a4-a8a5-aad087f6cca3" />

To improve our robot’s ability to detect visual markers and environmental cues, we mounted the Pixy Cam on top of the robot, connected to the medium motor steering with an axle. This elevated, dynamic position gives the camera a wider field of view, allowing it to actively turn with the steering to detect obstacles from a greater distance and with fewer blind spots. Placing the camera higher also prevents it from being blocked by parts of the robot’s frame, which improves both its accuracy and response time during object recognition.

For navigation, we mounted a single ultrasonic sensor in a fixed position, allowing the robot to actively monitor its surroundings straight ahead. This strategic configuration enables a single sensor to measure forward distances to nearby walls without the added weight of multiple sensors. As a result, the robot receives reliable and consistent environmental data, helping it stay centered in narrow paths or corridors. By constantly tracking these forward distance values, the robot can make precise steering adjustments to maintain a straight, balanced course critical for avoiding collisions and achieving consistent lap performance.
