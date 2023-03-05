# Sensor implementation information

## Accelerometer

### Android

- **ID:** [TYPE_ACCELEROMETER](https://developer.android.com/reference/android/hardware/Sensor#TYPE_ACCELEROMETER)
- **Values:** 3 elements, XYZ axes, each minus G
- **Unit:** m/s^2
- [source](https://developer.android.com/reference/android/hardware/SensorEvent#sensor.type_accelerometer:)

### iOS

- **Name:** Accelerometer
- **Data:** [CMAccelerometerData](https://developer.apple.com/documentation/coremotion/cmaccelerometerdata) object -> holds [CMAcceleration](https://developer.apple.com/documentation/coremotion/cmacceleration) object -> XYZ axes
- **Unit:** Gs

## Gyroscope

### Android

- **ID:** [TYPE_GYROSCOPE](https://developer.android.com/reference/android/hardware/Sensor#TYPE_GYROSCOPE)
- **Values:** 3 elements, XYZ axes, positive: counter-clockwise
- **Unit:** radians/second
- [source](https://developer.android.com/reference/android/hardware/SensorEvent#sensor.type_gyroscope:)

### iOS

- **Name:** Gyro
- **Data:** [CMGyroData](https://developer.apple.com/documentation/coremotion/cmgyrodata) object -> holds [CMRotationRate](https://developer.apple.com/documentation/coremotion/cmrotationrate) object -> XYZ axes
- **Unit:** radians/second

## Magnetometer

### Android

- **ID:** [TYPE_MAGNETIC_FIELD](https://developer.android.com/reference/android/hardware/Sensor#TYPE_MAGNETIC_FIELD)
- **Values:** 3 elements, XYZ axes
- **Unit:** uT (microteslas)
- [source](https://developer.android.com/reference/android/hardware/SensorEvent#sensor.type_magnetic_field:)

### iOS

- **Name:** Magnetometer
- **Data:** [CMMagnetometerData](https://developer.apple.com/documentation/coremotion/cmmagnetometerdata) object -> holds [CMMagneticField](https://developer.apple.com/documentation/coremotion/cmmagneticfield) object -> XYZ axes
- **Unit:** uT (microteslas)

## Heading

### Android

- **ID:** [TYPE_HEADING](https://developer.android.com/reference/android/hardware/Sensor#TYPE_HEADING)
- **Values:** 2 elements, 0: heading [0-360), 1: heading accuracy defined at 68% confidence
- **Unit:** both in degrees
- [source](https://developer.android.com/reference/android/hardware/SensorEvent#sensor.type_heading:)

### iOS

- **Name:** DeviceMotion (multiple sensors)
- **Data:** [CMDeviceMotion](https://developer.apple.com/documentation/coremotion/cmdevicemotion) object -> holds heading as Double [0-360]
- **Unit:** degrees

## Linear Acceleration

Same as [Accelerometer](#accelerometer) but without earth's gravity.

### Android

- **ID:** [TYPE_LINEAR_ACCELERATION](https://developer.android.com/reference/android/hardware/Sensor#TYPE_LINEAR_ACCELERATION)
- **Values:** 3 elements, XYZ axes
- **Unit:** m/s^2
- [source](https://developer.android.com/reference/android/hardware/SensorEvent#sensor.type_linear_acceleration:)

### iOS

- **Name:** DeviceMotion (multiple sensors)
- **Data:** [CMDeviceMotion](https://developer.apple.com/documentation/coremotion/cmdevicemotion) object -> holds [CMAcceleration](https://developer.apple.com/documentation/coremotion/cmacceleration) object -> XYZ axes
- **Unit:** Gs

## Barometer

### Android

- **ID:** [TYPE_PRESSURE](https://developer.android.com/reference/android/hardware/Sensor#TYPE_PRESSURE)
- **Values:** 1 element, atmospheric pressure
- **Unit:** hPa (hectopascal)
- [source](https://developer.android.com/reference/android/hardware/SensorEvent#sensor.type_pressure:)

### iOS

- **Name:** Ambient Pressure
- **Data:** [CMAmbientPressureData](https://developer.apple.com/documentation/coremotion/cmambientpressuredata) object -> holds [Measurement](https://developer.apple.com/documentation/foundation/measurement)<[UnitPressure](https://developer.apple.com/documentation/foundation/unitpressure)> object -> unit and value variable
- **Unit:** stored as variable

## Thermometer

### Android

- **ID:** [TYPE_AMBIENT_TEMPERATURE](https://developer.android.com/reference/android/hardware/Sensor#TYPE_AMBIENT_TEMPERATURE)
- **Values:** 1 element, ambient temperature
- **Unit:** degree celsius
- [source](https://developer.android.com/reference/android/hardware/SensorEvent#sensor.type_ambient_temperature:)

### iOS

- **Name:** Ambient Pressure ??
- **Data:** [CMAmbientPressureData](https://developer.apple.com/documentation/coremotion/cmambientpressuredata) object -> holds [Measurement](https://developer.apple.com/documentation/foundation/measurement)<[UnitTemperature](https://developer.apple.com/documentation/foundation/unittemperature)> object -> unit and value variable
- **Unit:** stored as variable
