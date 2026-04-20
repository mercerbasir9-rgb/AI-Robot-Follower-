# **Team Name**
SeyTech

---

# **Project Title**
AI Robot Follower

---

## **Project Description**
An autonomous person-following robot powered by a Raspberry Pi 5 and Arduino Uno, using the YOLOv11 computer vision model and Pi Camera Module 3 to detect and track a designated owner in real time.

---

## **About the Project**
This project is meant to be a demonstration of a system that can be applied to real-world tasks and industries such as construction, industrial, medical, and beyond.

For the hardware setup, we used an aluminum robot chassis as the base of our system. When designing this system, we wanted it to be just as safe as it was efficient, so we made sure to integrate a power source with a built-in Battery Management System (BMS) to prevent short-circuit, overdischarge, and overheating.

We used a 5V switching voltage regulator rated at 6A to safely deliver the required 5V and 5A to the Raspberry Pi voltage pin. We included a L293D expansion board to control 4 TT DC motors from the Arduino due to its limited PWM output pins. Once connected, we sent information between the Arduino and Raspberry Pi via serial communication at 9600 Baud.

---

## **How Did the Idea Come About?**
During the last competition, Sey used computer vision in his project and wanted to use it again — this time applying it to a mobile system that can track and follow the device owner. He brought the idea to the team and we agreed to collaborate, with one member focusing on hardware setup while Sey focused on programming. This project is meant to be a demonstration of a system that can be applied to real-world tasks and industries such as construction, industrial, and military.

---

## **Challenges We Faced**

- **Camera Boundary Calibration** — One of our major challenges was setting the bounds for the camera and establishing the correct x-coordinate thresholds to tell the robot when it needed to go left or right.

- **Serial Communication** — Establishing reliable
