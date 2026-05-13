COMPONENTS USED:
At the heart of the robot lies the Arduino Uno, a versatile microcontroller that acts as the brain of the system, coordinating all sensors and actuators. 
To detect fire, a flame sensor is mounted on the robot, continuously scanning its surroundings for infrared signatures of flames. 
For navigation and obstacle avoidance, the HC-SR04 ultrasonic sensor measures distances by sending sound pulses and listening for echoes, ensuring the robot doesn’t collide with walls or objects.
Motion is provided by DC motors with wheels, driven through the L298N motor driver, which allows precise control of speed and direction.
A servo motor is used to position the water nozzle, enabling the robot to aim at the detected fire.
The extinguishing mechanism is powered by a mini water pump, which sprays water directly onto the flame.
All of these are powered by a rechargeable battery (7.4V–12V), making the robot portable and independent of external power sources.

WORKING CONNECTIONS:
The hardware components are carefully interconnected to ensure smooth operation. 
The flame sensor is connected to one of the Arduino’s analog pins, allowing it to send continuous fire detection signals. The ultrasonic sensor uses two digital pins—one for the trigger pulse and another for the echo response—to measure distances. 
The motor driver is wired to multiple digital pins, enabling the Arduino to control the left and right motors independently for forward, backward, and turning movements. 
The servo motor is connected to a PWM pin, which allows fine angular control for aiming the nozzle. 
The water pump is controlled through a relay or driver module, ensuring safe switching of higher current loads. 
Together, these connections form a responsive system where sensors feed data to the Arduino, and actuators respond instantly to commands.

POWER SUPPLY:
The robot is powered by a 7.4V–12V battery pack, which provides sufficient energy to drive the motors and water pump. 
Since the Arduino and sensors require a stable 5V supply, a voltage regulator is included to step down and stabilize the voltage. This ensures that sensitive components like the flame sensor and ultrasonic sensor receive clean, regulated power without fluctuations that could cause false readings. 
The separation of motor/pump power and regulated sensor power prevents electrical noise from interfering with detection accuracy. This thoughtful power distribution makes the robot reliable even during extended operation.

NOTE:
The hardware design emphasizes simplicity, affordability, and replicability. By using widely available components like the Arduino Uno, HC-SR04 ultrasonic sensor, and L298N motor driver, the robot can be built at low cost without sacrificing functionality. Its compact layout makes it suitable for classroom demonstrations, robotics competitions, or DIY projects. The modular approach also means students can easily replace or upgrade parts—for example, swapping the flame sensor with a more advanced IR module or replacing the water pump with a CO₂ extinguisher system. This balance of practicality and innovation makes the robot not just a fire-fighting prototype, but also a valuable educational tool for learning embedded systems, automation, and robotics.
