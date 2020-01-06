# FreeIMU-GUI
FreeIMU GUI originally from Fabio Varesano - modified for Python 3.6 and PyQT5
https://code.launchpad.net/~fabio-varesano/freeimu/trunk

## FreeIMU library commands

| Command | Params         | Info                                                           |
|:-------:|:--------------:| -------------------------------------------------------------- |
| v       |                | Returns version information FreeIMU 					        |
| 1       |                | Initializes the FreeIMU library                                |
| 2       |                | Resets the FreeIMU library.                                    |
| g       |                | Initialize FreeIMU gyroscope(s).                               |
| t       |                | Set FreeIMU temperature calibration.                           |
| p       | int pressure   | Set the sea level pressure. Example: Set to 100 `p100`         |
| r       | int count      | Read *FreeIMU raw data* `count` times as printable data. `r1`  |
| b       | int count      | Read *FreeIMU raw data* `count` times as binary data. `b1`     |
| q       | int count      | Read *FreeIMU quaternions* `count` times. `q1`                 |
| z       | int count      | Read *FreeIMU quaternions + values* `count` times. `z1`        |
| a       | int count      | Read *FreeIMU kalman filtered quats + vals* `count` times. `a1`|
| C       |                | Read/Check calibration values. `C`                             |
| d       |                | Read FreeIMU debug outputs. `d`                                |
| D       |                | Read *FemtoBeacon data*. `D`                                   |
| SLEEP_SENSORS|           | Sleep IMU sensors                                              |
| WAKE_SENSORS |           | Wake IMU sensors                                               |

*FreeIMU raw data* - accel X, accel Y, accel Z, gyro X, gyro Y, gyro Z, mag X, mag Y, mag Z, temperature

*FreeIMU quaternions* (IMU orientation with respect to Earth) - quaternion 1, quaternion 2, quaternion 3, quaternion 4

*FreeIMU quaternion + values* (IMU orientation with respect to Earth). Values are rad/sec. - quaternion 1, quaternion 2, quaternion 3, quaternion 4, accel X, accel Y, accel Z, gyro X, gyro Y, gyro Z, mag X, mag Y, mag Z, temperature (from barometer), pressure, sample frequency, mag heading, estimated altitude, motion detect value.

*FreeIMU kalman filtered quats + vals* (IMU orientation with respect to Earth). Values are rad/sec. Quaternions are Kalman filtered. - quaternion 1, quaternion 2, quaternion 3, quaternion 4, accel X, accel Y, accel Z, gyro X, gyro Y, gyro Z, mag X, mag Y, mag Z, temperature (from barometer), pressure, sample frequency, mag heading, estimated altitude, motion detect value.

*FemtoBeacon data* (YPR is 180deg based. Euler angles are 360deg based.) - current MS, yaw, pitch, roll, euler angle 1, euler angle 2, euler angle 3, accel X, accel Y, accel Z.
