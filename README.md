# hello-world
Sample repository
ROS navigation stack drives the robot by publishing velocity commands to /cmd_vel topic using geometry/Twist messages. The base controller on the Teensy board receives the twist messages through rosserial_python and translates the velocites to motor commands. A PID controller maintains the robot's speed by calculating how much PWM signal must be generated to spin each motor based from the total error over time. Errors are derived by comparing the actual motor's speed to the desired speed sent by navigation stack. This section will show you how to tune the PID controller with lino_pid, wire up the components, and upload the base controller's code on the Teensy board.
