# Micromouse code

*A maze-solving micromouse implemented on STM32F446RE*

This mouse design has two DC motors driven by a TI DRV8833, and 4 IR sensors, two looking forward at an outward angle and two looking sideways, again at an angle.
Odometry is provided by a hall effect quadrature encoder on each motor.
Provision is made for a TDK ICM-42688 IMU, or a TDK ICM-45688 if and when that becomes available.
A forward-facing VL53L4CD time-of-flight ranging sensor is used for look-ahead

## Pin Descriptions

| Pin number | Configuration | Function | Description |
|------------|---------------|----------|-------------|
| | PWM Output | LMotor_A | Left motor PWM signal 1 |
| | PWM Output | LMotor_B | Left motor PWM signal 2 |
| | PWM Output | RMotor_A | Right motor PWM signal 1 |
| | PWM Output | RMotor_B | Right motor PWM signal 2 |
| | GPIO Output | IR_Front_L_Pulse | Front left IR emitter pulse enable |
| | GPIO Output | IR_Front_R_Pulse | Front right IR emitter pulse enable |
| | GPIO Output | IR_L_Pulse | Left IR emitter pulse enable |
| | GPIO Output | IR_R_Pulse | Right IR emitter pulse enable |
| | ADC | IR_Front_L | Front Left IR Sensor |
| | ADC | IR_Front_R | Front Right IR Sensor |
| | ADC | IR_L | Left IR Sensor |
| | ADC | IR_R | Right IR Sensor |
| | Interrupt Input | L_ENC_A | Left encoder channel A |
| | Interrupt Input | L_ENC_B | Left encoder channel B |
| | Interrupt Input | R_ENC_A | Right encoder channel A |
| | Interrupt Input | R_ENC_B | Right encoder channel B |
| | I2C SDA | VL53L4CD_SDA | I2C bus data for VL53L4CD |
| | I2C SCL | VL53L4CD_SCL | I2C bus clock for VL53L4CD |
| | Interrupt Input | VL53L4CD_INT | Interrupt from VL53L4CD |
| | GPIO Output | VL53L4CD_EN | Enable for VL53L4CD |
| | SPI SCK | ICM-42688_SCK | SPI Clock for ICM-42688 |
| | SPI MISO | ICM-42688_MISO | SPI MISO for ICM-42688 |
| | SPI MOSI | ICM-42688_MOSI | SPI MOSI for ICM-42688 |
| | SPI CS or GPIO Output | ICM-42688_CS | Chip select, active low, for ICM-42688 |
| | GPIO Interrupt | ICM-42688_INT1 | Interrupt 1 from ICM-42688 |
| | GPIO Interrupt | ICM-42688_INT2 | Interrupt 2 from ICM-42688 |
| | GPIO Input or Interrupt | SW1 | Switch 1, momentary push-button input |
| | GPIO Input or Interrupt | SW2 | Switch 2, momentary push-button input |
| | GPIO Output | LED1 | LED 1 Output |
| | GPIO Output | LED2 | LED 2 Output |
| | ADC | VBATT | Battery voltage input |

