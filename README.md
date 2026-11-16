# ECE 528/L - Robotics and Embedded Systems with Lab
**CSU Northridge**

**Department of Electrical and Computer Engineering**

## Line Follower Lab
The Line Follower lab interfaces with the following:

* User LEDs of the TI MSP432 LaunchPad
* Pololu Gearmotor with Encoder - [Product Link](https://www.pololu.com/product/3675)
* 8-Channel QTRX Sensor Array - [Product Link](https://www.pololu.com/product/3672)

## 1. Overview

This lab implements the concepts introduced in the two previous labs, motor control and reflectance sensor, to create a line follower robot that will drive along a line maze course. These concepts were used to display how a finite state machine, or FSM, can be used to allow the robot to explore the line maze in real-time.

## 2. Components Used

- 1 MSP432 Launchpad
- 1 USB-A to Micro-USB Cable
- 1 TI-RSLK MAX Chassis
- 1 8-Channel QTRX Sensor Array
- 1 Black Tape (1-inch or 3/4-inch)
- 1 Display Board

## 3. Pre-Lab Questions

Pre-lab assignment

1)
void Chassis_Board_LEDs_Init(){
    P8->SEL0 &= ~0xE1;
    P8->SEL1 &= ~0xE1;
    P8->DIR |= 0xE1;
    P8->OUT |= 0xE1;
}

2)
/** 
* @file print_tenth.c
* 
* @brief Main source code for Print Tenth program.
* 
* This file contains the main entry point and the implementation
* of the Print_Tenth function taht iterates from 10 to 51 and
* prints a message every 10th iteration (10, 20, 30, 40, 50)
* and a different message following the 10th iteration (11, 21,
* 31, 41, 51).
* 
* @author Steve Ortiz
*/
void Print_Tenth();

int main(){
    Print_Tenth();
    return 0;
}

void Print_Tenth(){
    //implementation goes here
     for (int i = 1; i<=52; i++){
        if ((i%10) == 0){
            printf("Index %d: Every 10th iteration.\n", i);
        }
        if ((i%10) == 1  && i != 1){
            printf("Index %d: Following the 10th iteration.\n", i);
        }
    }
}

## 4. Analysis and Results

The lab reinforced C programming concepts and practices through hands-on testing. During two unrecorded trials, the robot navigated the maze and returned to its starting point. The robot did not complete the same route during any recorded trial, as the video below shows its best recorded attempt.



## 5. Known Issues or Limitations

The main limitation surrounding the lab was an unfortunate series of unforeseen circumstances that led to the lack of several lab sessions where the code could be tested and tried.

## 6. References

1. ece528L_fall26_lab3_line_follower.pdf
2. MSP432P4xx SimpleLink Microcontrollers Technical Reference Manual
3. ece528L_fall26_lab2_reflectance_sensor.pdf
4. ece528L_fall26_lab1_motor_control.pdf
