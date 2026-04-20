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

The robot's brain is split into four Python files — one handles the camera, one runs the YOLOv11 detection model, one manages the serial connection to the Arduino, and one ties it all together. Every frame, it checks where the detected person is relative to the center of the camera view, and whether they're close or far based on how big their bounding box is. From that, it sends a simple one-word command — like F, L, R, or STOP — over serial to the Arduino, which then drives the motors accordingly.
<img width="1920" height="1080" alt="Your paragraph text" src="https://github.com/user-attachments/assets/ed5d591d-0d0c-49bb-92e0-6d8212606a01" />
<img width="655" height="873" alt="image" src="https://github.com/user-attachments/assets/46b4686a-42f0-4237-ad08-f70f5b7af735" />
<img width="654" height="873" alt="image" src="https://github.com/user-attachments/assets/7bba7066-6fe5-45e2-9b78-8a1101698c4d" />



---

## **How Did the Idea Come About?**
During the last competition, Sey used computer vision in his project and wanted to use it again — this time applying it to a mobile system that can track and follow the device owner. He brought the idea to the team and we agreed to collaborate, with one member focusing on hardware setup while Sey focused on programming. This project is meant to be a demonstration of a system that can be applied to real-world tasks and industries such as construction, industrial, and military.

---

## **Challenges We Faced**

One of our major challenges was setting the bounds for the camera and establishing the correct x-coordinate thresholds to tell the robot when it needed to go left or right. Another major challenge was establishing serial communication between the Raspberry Pi and the Arduino.The last challenge we experienced is losing sight of the owner while moving forward due to difference of resolution between the Raspberry Pi and camera module. Our Raspberry Pi board got fried in the process of testing, so we improvised and placed the laptop on top of the robot chassis. This improved the camera resolution and program operation so it was beneficial. 
