---
title: 'Husarion add-ons'
platform: 'CORE2'
autotoc: true
layout: layout.hbs
order: 4
page: 'Manuals'
onepager: true
---

# CORE2block extension kit #

Adapter which connects CORE2 or CORE2-ROS with Makeblock system. 

<div class="thumb center h350">
![](/assets/img/external-modules/core2block.png)
</div>

The main part are adapters for sensors and motors. Electrical interface of Makeblock sensors is similar to CORE2 hSensor, but some pin-swapping is needed. These adapters do the job.

Set contains:

 * 6 cables and adapters for connecting Makeblock sensors to the Husarion CORE2 controller (6x 15cm)
 * 4 cables for connecting Makeblock DC motors (with encoder) to the Husarion CORE2 controller (4x 30cm)
 * 2 cables for connecting Makeblock DC motors (without encoder) to the Husarion CORE2 controller (2x 30cm)
 * hBatteryPack - a battery pack for 3x18650 Li-Ion batteries (batteries not included)
 * 2 acrylic plates + set of screws, that link CORE2 and hBatteryPack with Makeblock mechanical parts
 
## Sensor adapter ##

Sensor adapters consist of:
 * 6 PCB's which connects to CORE2 from one side, and to the Makeblock sensors from the other side. 
 * 6 ribbon cables to connect CORE2 hSensors with adapter PCBs.

The connectors used with CORE2 are shrouded box headers: 2×3-Pin, 0.1" (2.54 mm), male, mating with IDC 0.50" pitch ribbon cables. We use Amphenol T821106A1S100CEU or compatible. On the "Makeblock side" a 6P6C sockets are used to work with 6P6C crimped connectors, similar to the telephone jacks. In the Makeblock documentation they are called "RJ25". We use Molex 95501-2661 or compatible.

Adapter PCBs that can be separated by breaking them off, if you like. The connections on each adapter are explained on the circuit diagram below:

<div class="thumb center h350">
![](/assets/img/external-modules/core2block-schematic.png)
</div>

Important: the Makeblock documentation shows a different, non-standard pin order for 6P6C (RJ25) connector. We follow the order used by Molex and FCI connector manufacturers, and also by LEGO® in their Mindstorms kits.

On the bottom side of PCB you can find jumpers for configuring the adapter connections. They are needed for interfacing CORE2 with different Makeblock sensors. The photo below shows the jumper position on PCB:

<div class="thumb center h350">
![](/assets/img/external-modules/jumpers.jpg)
</div>

And this table should be helpful for you:

<table>
    <tr>
       <th>Makeblock sensor name</th>
       <th>Main interface</th>
	   <th>CORE2 hSens port no</th>
       <th>JP1-JP3 position</th>
    </tr>
    <tr>
        <td>Me Compass</td>
        <td>I2C</td>
        <td>1 or 2</td>
        <td>B</td>
    </tr>
    <tr>
        <td>Me Ultrasonic Sensor</td>
        <td>digital/interrupt</td>
        <td>1-6</td>
        <td>B</td>
    </tr>
    <tr>
        <td>Me 3-Axis Accelerometer and Gyro Sensor</td>
        <td>I2C</td>
        <td>1 or 2</td>
        <td>B</td>
    </tr>
    <tr>
        <td>Me 7-Segment Serial Display</td>
        <td>2-wire serial</td>
        <td>3-4</td>
        <td>A</td>
    </tr>
    <tr>
        <td>Me Bluetooth Module(Dual Mode)</td>
        <td>UART</td>
        <td>3 or 4</td>
        <td>A</td>
    </tr>
    <tr>
        <td>Me Flame Sensor</td>
        <td>digital</td>
        <td>1-6</td>
        <td>A or B</td>
    </tr>
    <tr>
        <td>Me Line Follower</td>
        <td>digital</td>
        <td>1-6</td>
        <td>B</td>
    </tr>
    <tr>
        <td>Me Light Sensor</td>
        <td>analog</td>
        <td>1-6</td>
        <td>B</td>
    </tr>
    <tr>
        <td>Me Infrared Receiver Decode</td>
        <td>I2C</td>
        <td>1-6</td>
        <td>A or B</td>
    </tr>
    <tr>
        <td>Me PM2.5 Sensor</td>
        <td>UART</td>
        <td>3 or 4</td>
        <td>A</td>
    </tr>
    <tr>
        <td>Me Potentiometer</td>
        <td>analog</td>
        <td>1-6</td>
        <td>B</td>
    </tr>
    <tr>
        <td>Me PIR Motion Sensor</td>
        <td>digital/interrupt</td>
        <td>1-6</td>
        <td>B</td>
    </tr>
	<tr>
        <td>Me RGB LED</td>
        <td>serial</td>
        <td>3 or 4</td>
        <td>A or B</td>
    </tr>
	<tr>
        <td>Me-Shutter</td>
        <td>digital</td>
        <td>1-6</td>
        <td>A or B</td>
    </tr>
    <tr>
        <td>Me Slide Potentiometer</td>
        <td>analog</td>
        <td>1-6</td>
        <td>B</td>
    </tr>
	<tr>
        <td>Me USB Host</td>
        <td>serial</td>
        <td>3 or 4</td>
        <td>A</td>
    </tr>
	<tr>
        <td>Me Touch Sensor</td>
        <td>digital</td>
        <td>1-6</td>
        <td>A or B</td>
    </tr>
	<tr>
        <td>Me Temperature and Humidity Sensor</td>
        <td>digital</td>
        <td>1-6</td>
        <td>A or B</td>
    </tr>
	<tr>
        <td>Me Sound Sensor</td>
        <td>analog</td>
        <td>1-6</td>
        <td>B</td>
    </tr>
	<tr>
        <td>Me TFT LCD Screen – 2.2 Inch</td>
        <td>UART</td>
        <td>3 or 4</td>
        <td>A</td>
    </tr>
	<tr>
        <td>Me Line Follower Array</td>
        <td>UART</td>
        <td>1-6</td>
        <td>B</td>
    </tr>
	<tr>
        <td>Me Sound Sensor</td>
        <td>analog</td>
        <td>1-6</td>
        <td>B</td>
    </tr>
</table>

## Motor adapter ##

A simple, 6-wire cable with different connectors on both sides:
 * On the CORE2 side, there is a **black**, 6-pin, female, wire-to-board connector with 2.54mm pitch.
 * On the Makeblock motor side, there is a similar connector, but **white**, with 2mm pitch and polarization keys.

**Black** connectors:
 * Harwin M20-1060600 housing with Harwin M20-1160046 crimp contacts
 * Molex 50-57-9006 (70066-0005) housing with Molex 0016020xxx 70058 crimp contacts
 * Amphenol (former FCI) 65039-031LF housing with 47649-000LF or 47565-002LF crimp contacts
 * TE connectivity 104439-5 housing with 181270-1 crimp contacts
And many other manufacturers. These connectors are commonly known as "Dupont".
 
**White** connectors:
 * JST PHR-6 housing with SPH-001T-P0.5S crimp contacts
There are also other manufacturers.
 
Caution! The cable doesn't have any polarization key on the 2.54 (black) connector. Please make sure that you connect it in correct orientation.

The motor adapter allows to use the following Makeblock motors:
 * DC Motor-25 9V/700RPM
 * DC Motor-37 12V/200RPM
 * DC Motor-37 12V/50RPM
 * 36 DC Geared Motor 12V 240RPM
 * Mini Metal Gear Motor – N20 DC 12V
 * DC Encoder Motor – 25 6V/185RPM
 * 180 Optical Encoder Motor
 * Optical Encoder Motor-25 9V/185RPM
 * Optical Encoder Motor-25 9V/86RPM
Of course, if you can deal with soldering custom connectors, you will be able to use other motors as well.

## hBatteryPack ##

The same which is used in Telepresence robot, ROSbot and CORE2brick kit. Full description here: [hBatteryPack](https://husarion.com/core2/manuals/external-modules/#external-modules-hbatterypack "hBatteryPack")

## Acrylic plates and screws ##

There are 2 transparent, PMMA plates with holes. The hole spacing is 8mm to make them compatible with LEGO® Mindstorms and Makeblock mechanics. 

The bigger board is prepared for assembling with CORE2, using M3x6 standoffs, M3x10 screws to connect standoffs with PMMA board and M3x4 screws to attach CORE2.

The smaller board is prepared for assembling with hBatteryPack, using M3x6 standoffs, M3x10 screws to connect standoffs with PMMA board and M3x4 screws to attach hBatteryPack.

***

# Servo controller for CORE2 #

Allows to connect 12 additional servos to CORE2.

Communicates with CORE2 via hSensor interface. Up to four servo controllers can work on one hSensor port thanks to 2-bit addressing. The step down DC/DC converter with software-controlled output voltage is available on board to simplify power connections - you can supply the servo controller and CORE2 from the same power source.

Servo controller can deliver up to 3A average current to the servos.

The picture below describes the pinout of the Servo driver.

<div class="thumb center h350">
![](/assets/img/external-modules/servo_driver.png)
</div>

## First run ##

Connect the Vin voltage (+6V...+16V) and servos that you need. Connect the UART interface to hSens3 or hSens4 on CORE2 using the flat IDC cable. 
Build your program for CORE2 following the example available on https://husarion.com/core2/examples/
Library for ServoDriver is available on GitHub:
https://github.com/husarion/modules

## Specification ##

 * Integrated DC/DC converter
 * Output voltage (+V servo) selectable by software: 5V / 6V / 7.4V / 8.6V
 * 12 PWM outputs, 3.3V logic level, compatible with most analog and digital RC servos
 * 3A nominal output current
 * 5A peak output current
 * Input voltage range (Vin): 6...16V
 * Logic supply voltage: +5V typical, +4...+10V is acceptable.
 * Overcurrent and short-circuit protection

## Address selection ##

You can connect up to four servo controllers to one UART interface (hSens3 or hSens4 port of CORE2) in parallel. The IDC flat cable allows to crimp additional connectors anywhere along the cable. 
Each command sent by CORE2 to servo controller contains an address from 0 to 3. Each servo controller will execute only the commands that match the local address, configured with jumper. The default address is 0 (without jumper).

## LED behavior ##

In the current firmware, the LED is turned on if both power supplies (+5V and +Vin) are connected. LED is blinking when servo controller receives commands.