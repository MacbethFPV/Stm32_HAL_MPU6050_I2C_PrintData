# Simple_MPU6050_I2C_Printout
Basic MPU6050 I2C Driver used to get Accelerometer and Gyroscope print outs over UART using an STM32F411RET6U Nucleo Dev Board

Original Author - Controller's Tech
Original Author's Website - https://controllerstech.com/how-to-interface-mpu6050-gy-521-with-stm32/
Modified by - Mac
Purpose - Base for future project
=========================================

Some guidance to use the above:
  - Firstly check out Controller Tech's Youtube Video to learn how the code goes together
  - Ensure STM32CubeIDE is Installed
  - Start an STM32 Project
  - Select Board, (I used the STM32F411RET6U Nucleo board)
  - Under Connectivity, choose to enable an I2C port. 
        (I used I2C1 and chose pins PB6 (I2C1_SCL) and PB7 (I2C1_SDA)
  - Under Connectivity, choose to enable a USART port. 
        (I used USART1 and chose pins PA9 (USART1_TX) and PA10 (USART1_RX)
  - After saving my project and letting the code auto generate, I added the .h and .c file to my project 
        <PROJECT_FOLDER>/Core/Inc/MPU6050.h
        <PROJECT_FOLDER>/Core/Src/MPU6050.c
        I would not advise copy and pasting main to your project, I like to pick it apart and manually 
          insert the portions that were not auto-generated by STM32CubeIde
  - I hooked up the CP2102 using CP2102 GND -> Nucleo GND
                                 CP2102 RXD -> Nucleo TX (PA9)
                                 CP2102 TXD -> Nucleo RX (PA10)
                                 (May differ for your setup depending on your HW and Pin configuration)  

Hardware used:
  - STM32F411RET6U Nucleo Board
  - MPU6050 6-axis IMU
  - CP2102 USB to TTL Adapter 
  - Qty 4: 1.25mm Dupont Female to Female Connectors

