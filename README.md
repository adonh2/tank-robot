Mini Tank Robot 🤖🚜
A two-drive tracked robot I built using an Arduino-compatible platform. No welding involved, just solid, beginner-friendly hardware powered by two 18650 batteries, with infrared remote control and an 8x16 LED display for visual feedback.
Features

Infrared remote control: drive the tank forward, backward, left, and right using an IR remote
Servo-mounted "head": the tank can look left and right on command
8x16 LED matrix display: shows animations and status indicators for each movement (forward, back, left, right, stop)
Personalised nameplate: pressing a dedicated button on the IR remote displays my name ("ADON") on the LED panel
Dual-motor tank drive: independent PWM control of left and right motors for precise movement

Hardware
ComponentPinLeft motor directionD13Left motor PWMD11Right motor directionD12Right motor PWMD3ServoD9IR receiverA0LED matrix SDAA4LED matrix SCLA5
You'll also need: 2x 18650 batteries (not included in most kits).
Remote Control Mapping
Button (Hex)Action0xFF629DMove forward0xFFA857Move backward0xFF22DDTurn left0xFFC23DTurn right0xFF02FDStop0xFF30CFRotate anticlockwise0xFF7A85Rotate clockwise0xFF9867Display my name ("ADON") on the LED panel0xFF6897Look left (servo)0xFFB04FLook right (servo)
Getting Started

Install the IRremoteTank library in the Arduino IDE.
Wire up the motors, servo, IR receiver, and LED matrix according to the pin table above.
Upload the sketch to your Arduino.
Insert two charged 18650 batteries and power on.
Point your IR remote at the receiver and start driving!

How It Works
The sketch listens for IR signals in the main loop and matches decoded hex values to movement commands. Each movement triggers both a motor action and a corresponding animation on the LED matrix (driven over a bit-banged I2C-style protocol on A4/A5). There's also a dedicated button that scrolls my name across the display, a little personal touch I added to make the tank mine. The servo lets the tank pan its "head" left or right for a bit of extra personality.
Why I Built It
A hands-on project to dig into robotics, motor control, and embedded electronics, and a fun way to watch code translate directly into physical movement.
