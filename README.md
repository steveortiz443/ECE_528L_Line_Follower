# ECE 528/L - Robotics and Embedded Systems with Lab
**CSU Northridge**

**Department of Electrical and Computer Engineering**

## Line Follower Lab
The Line Follower lab interfaces with the following:

* User LEDs of the TI MSP432 LaunchPad
* Pololu Gearmotor with Encoder - [Product Link](https://www.pololu.com/product/3675)
* 8-Channel QTRX Sensor Array - [Product Link](https://www.pololu.com/product/3672)

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
    for (int i = 1; i>=52; i++){
        converted = ((value_to_convert >> i) & 1);
        if ((i%10) == 1){
            printf("Index %d: Every 10th iteration.\n", i);
        }
        if ((i%11) == 1){
            printf("Index %d: Following the 10th iteration.\n", i);
        }
    }
}

