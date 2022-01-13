# RMAP

The Rotating Motion Activated Pedestal

Based on [this Arduino project](https://create.arduino.cc/projecthub/lindsi8784/motion-following-motorized-camera-base-61afeb).

## Parts

### Arduino Uno

Controls the servo motor based on input from the PIR sensors.

<!-- [![Arduino Uno Rev 3](https://cdn.shopify.com/s/files/1/0506/1689/3647/products/A000066_03.front_970c6014-61ab-4226-a20f-14cc6d8d682c_1000x750.jpg?v=1629816078)](https://store.arduino.cc/products/arduino-uno-rev3/) -->

### TowerPro MG996R Servo

Moves the top of the pedestal to different positions. The [TowerPro MG996R 360° Servo](https://www.amazon.com/Tower-MG996R-Rotation-Robotic-Servo/dp/B081XC2BM4) I got did not work like a regular servo, but the [180° version](https://www.amazon.com/4-Pack-MG996R-Torque-Digital-Helicopter/dp/B07MFK266B) works fine.

### PIR Sensors

The motion sensors direct the servo to move to look toward the motion. [These PIR sensors](https://www.amazon.com/HC-SR501-Sensor-Infrared-Arduino-Raspberry/dp/B07KBWVJMP) worked fine, but they do have a one minute initialization time, so keep that in mind.

## Concept

The RMAP is a circular pedestal with 5 sensors at regular angles over a 180° arc. A servo in the center rotates a flat, circular top between 0 and 180° to point anything on top of it in the direction of the detected motion. The idea is to create a base that rotates to follow motion. With a camera or phone positioned on top, it would function similarly to the [Facebook Portal](https://www.amazon.com/Portal-Facebook-Hands-Free-Calling-Built/dp/B07HFWG8S4).

## Construction

To build the housing for the 5 PIR sensors, I created a two-piece base in Fusion 360. I had little experience using CAD software, so I encountered a lot of trouble.

The top piece of the pedestal is a simple column with small holes around its center that could be used to mount something. On the bottom, a small extension allows a .5 mm deep hole to be cut to attach the servo.

The bottom piece of the pedestal houses the 5 PIR sensors and holds the servo in place. I made circular holes to put the PIR sensors into. Rectangles would have been better because the sensors tend to fall out of their slots, although I rigged some tape to keep them in place. The stand in the center for the servo ended up too large, but, with some tape, the servo stays in place. The wiring is rather tight, so the whole pedestal should probably be a bit larger, especially if the goal is to fit the Arduino inside.

## Problems

- PIR sensors fall out of holes
  - make the holes rectangular to fit the sensors into
  - use duct tape
- not enough space
  - make the whole model larger
- servo does not function
  - not yet fixed

1/13/2022: I have not yet determined why the servo is no longer functioning. I tested the logic portion of the system before, and the servo and PIR sensors seemed to be working fine.
