>If you have any questions, please contact fischertechnik-technik@fischer.de

# TXT 4.0 Controller - I2C
The fischertechnik [TXT 4.0 controller](https://www.fischertechnik.de/en/toys/e-learning/txt-4-0-controller) has 2 connections labeled EXT1 and EXT2 (see 07 in the picture). Both connections are connected to the internal I2C bus, see [RX Controller Operating Instructions](https://www.fischertechnik.de/-/media/fischertechnik/fite/service/elearning/lehren/txt40controller/fischertechnik-txt-operating-manual_en.pdf).

| TXT 4.0 Controller | 6-pin Assigment |
| --- | --- |
|<img src="https://github.com/user-attachments/assets/258e930e-3d88-402c-94c4-a39d4877b59c" width="400">|<img src="https://github.com/user-attachments/assets/9121a6af-6fb6-44de-b255-afbd045acae8" width="400">|

> [!WARNING]
> * Power supply for I2C is **3.3V**

## Python Code
TXT 4.0 controller uses Python3. The basic functions for I2C are listed [here](https://pypi.org/project/smbus2/).

### I2C Imports
```python
```

### I2C Scan
```python
```

### I2C Write Buffer
```python
```

### I2C Read Buffer
```python
```

### I2C Write Read Buffer
```python
```

### Examples External I2C Modules
Some examples of external I2c modules already exist. These examples can be imported with the [ROBO Pro Coding](https://www.fischertechnik.de/en/apps-and-software#apps) app.

| sensor chip |  ROBO Pro Coding program name |
| ---         | ---                           |
| APDS9960    | *APDS9960_smbus* |

## fischertechnik I2C Sensors
Some I2C addresses are already reserved, see e.g. [here](https://i2cdevices.org/addresses) or [www.i2c-bus.org](https://www.i2c-bus.org/). All fischertechnik I2C sensors are listed in the table below.

| Sensor                     | Item Number  | I2C Address | sensor chip          | RX Controller           | TXT 4.0 Controller      | TXT Controller |
| ---                        | ---          | ---         | ---                  | ---                     | ---                     | ---            |
|Environmental sensor 6-pin	 |182974     	|0x76	      |BME680                | Yes                     | Yes                     |                |
|Environmental sensor 10-pin |167358	    |0x76	      |BME680                | Yes, I2C-Adapter 186150 | Yes, I2C-Adapter 186150 | Yes (C/C++)    |
|RGB gesture sensor 6-pin	 |183267	    |0x39	      |APDS9960              | Yes                     | Yes                     |                |
|RGB gesture sensor 10-pin   |186705	    |0x39	      |APDS9960              | Yes, I2C-Adapter 186150 | Yes, I2C-Adapter 186150 | Yes            |
|Kombisensor 6-pin           |201257	    |0x68	      |ICM42670 (GYRO + ACC) | Yes (FW>=0.26.2)        | Yes                     |                |
|                            |              |0x30 	      |MMC5603 (MAG)         | ...                     | ...                     |                |
|Kombisensor 10-pin	         |158402	    |0x10	      |BMX055 (MAG)          | Yes, I2C-Adapter 186150 | Yes                     |                |
|                            |              |0x18         |BMX055 (ACC)          | ...                     | ...                     |                |
|                            |              |0x68	      |BMX055 (GYRO)         | ...                     | ...                     |                |
|RGB color sensor	         |213965	    |0x14	      |Knobloch              |                         | Yes (txtapi>=6.4.0)     |                |
|NFC module	                 |-	            |0x24	      |PN532 NFC RFID Module |                         | Yes                     | Yes (C/C++)    |
|AGV charging module	     |-	            |0x26	      |Knobloch              |                         | Yes                     |                |
|RESERVED                    |              |0x8          |                      | RESERVED                |                         |                |

## Connector I2C - 10-pin  (Deprecated)
> [!WARNING]
> * Power supply for I2C is 3.3V
> * No separate power supply at the plug 

<img src="https://github.com/user-attachments/assets/2004514b-5a98-4904-ba74-0bb5a3d93dd0" width="400">
