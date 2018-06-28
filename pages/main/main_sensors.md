---
title: Sensors
keywords: electronics, sensors
summary: "Sensors are what allow your robot to interact with the physical world."
sidebar: main_sidebar
permalink: main_sensors.html
folder: main
---

## Preface

Without sensors and feedback that utilizes them, your robot is basically an overengineered RC car.

*Seriously, in a demo event I remember one parent asked, "What makes this a robot and not just a RC car?" It was difficult to answer that question.*

Let's take a look at the sensors we use in our FRC robots.

## Sensors

### 1. Encoders and Potentiometers

Encoders and pots are both examples of rotary sensors - they measure rotation. They are they most commonly used sensors in our FRC robots. We can use encoders to measure the position of a rotating arm, flywheel speed, how much an elevator has been raised, and more.

Read [this article](http://frc-pdr.readthedocs.io/en/latest/motors/encoders.html) to learn the difference between absolute and relative (incremental) encoders.

{% include image.html file="main/quadrature.jpg" caption="Visual graph" max-width="400" %}

You might see the term quadrature encoder tossed in around a lot. All that means is that the encoder can tell you the speed and rotation of a shaft bidirectionally (both forwards and backwards). This is possible because they output two channels, A and B, which are out of phase by 90 degrees and the phase difference is what determines the directionallity.

Pulses per revolution (PPR) is a measure of the resolution of an incremental encoder, with one revolution being 360 degrees. Encoders will slowly accumulate error. For example an arm observed at 0 degrees might read 0 pulses and after moving it a bit, at 0 degrees again the encoder will read 340 pulses. To account for error, a limit switch can be used at a point of the arm's movement to zero out the encoder. Better yet if possible, use an absolute encoder.

For continuously turning systems, you can pair an encoder with a 360 pot measuring the same output shaft so you can program the encoder to always be "zeroed" at start up. 1678 has done this with their robots and you can research on them to learn more.

{% include image.html file="main/srxmagencoder.jpg" caption="SRX Mag Encoder" max-width="200" %}

4159 recommends the use of the [SRX Mag Encoders](http://www.ctr-electronics.com/srx-magnetic-encoder.html). They are easily wired to Talon SRX's and easily programmable using CTRE's libraries.

Read about pots in this article [here](http://www.resistorguide.com/potentiometer/). Although we don't use pots very often in our robots, they may prove useful in future competitions.

{% include image.html file="main/pot.jpg" caption="Pot" max-width="200" %}

There's a [Chief Delphi thread](https://www.chiefdelphi.com/forums/showthread.php?t=100332) discussing about pots vs encoders.

### 3. IMUs

Learn about the differences between accelerometers, gyroscopes, and IMU's in this [Sparkfun guide](https://www.sparkfun.com/pages/accel_gyro_guide).

These sensors can be used to keep the robot's drivetrain orientation, prevent it from tipping over, and more.

{% include image.html file="main/navx.jpg" caption="navX" max-width="400" %}

We most commonly use the [navX-MXP by Kauai Labs](https://www.kauailabs.com/store/index.php?route=product/product&product_id=56). It plugs in the the RoboRio's MXP port or you can use their omnimount, and is easy to program using their provided libraries.

Other IMUs teams use include the Pigeon IMU (which is easily integrated with Talon SRX's), ADIS16448 by Analog Devices, and Spartan Board by 971.

### 4. Limit Switches

{% include image.html file="main/limitswitch.jpg" caption="Limit switch" max-width="250" %}

Read [this article](http://frc-pdr.readthedocs.io/en/latest/motors/limitswitch.html) to learn what limit switches are, how to wire them, and how to program them. WPILib also has an [article](http://wpilib.screenstepslive.com/s/currentCS/m/java/l/599744-using-limit-switches-to-control-behavior) on programming limit switches. When using a limit switch, keep in mind if it's normally open or normally closed.

Hall effect sensors can be used as a contactless limit switch. We recommend [this sensor](https://www.andymark.com/Electrical-p/am-3313.htm) intended for use on the DART actuator. If you'd like, you can learn about how hall effect sensors work [here](https://www.electronics-tutorials.ws/electromagnetism/hall-effect.html).

{% include image.html file="main/halleffect.gif" caption="Hall effect" max-width="400" %}

### 5. Other Not So Common Ones But Maybe Useful

Being worked on...

- Reed switches
- IR sensors
- Break beam sensor
- LIDAR
- Cameras in the Vision section

## Programming Sensors

Being worked on...

## Further Learning

1678 has done multiple workshops on "RoboRio and Sensors". You should watch one of these videos to supplement our notes above.
- [Fall 2017](https://www.youtube.com/watch?v=tKSH2k5lTLs)
- [Fall 2016](https://www.youtube.com/watch?v=vhjChjfEvhM)