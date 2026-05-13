Pin Definitions:
Motor driver pins (enA, in1, in2, in3, in4, enB) control two DC motors.
Flame sensors (ir_R, ir_F, ir_L) detect fire from right, front, and left.
Servo (A4) positions the nozzle.
Pump (A5) activates water spraying.

Setup Function:
Initializes serial communication for monitoring.
Configures sensor pins as inputs and motor/servo/pump pins as outputs.
Sweeps the servo motor to calibrate nozzle movement.
Sets motor speed using PWM (Speed = 160).

Loop Function:
Continuously reads flame sensor values (s1, s2, s3).
Prints sensor readings for debugging.
If fire is detected (sensor values below threshold), robot stops, activates pump, and sweeps servo to spray water.
If no fire but sensors detect intermediate values, robot navigates (forward, backward, turn left/right).
If no condition matches, robot stops and pump is off.

Servo Control:
servoPulse() generates PWM signals to rotate servo to specific angles.
Used for aiming nozzle during firefighting.

Motor Control Functions:
forword(), backword(), turnRight(), turnLeft(), Stop() define robot’s movement.
Each function sets motor driver pins to achieve desired motion.

Overall Behavior:
Robot autonomously detects fire direction.
Moves toward fire, stops, sprays water using pump + servo sweep.
Navigates around when no fire is detected.
Simple threshold-based decision-making ensures quick response.
