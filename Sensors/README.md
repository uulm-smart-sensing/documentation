# Sensors

<!-- TODO: Add description how to add a sensor on each platform -->

## Guideline on how to add support for a new sensor

### Flutter

### Android

### iOS

To support a new sensor on the iOS platform, first check whether it is possible to access this data and what permissions and swift packages are necessary. 
> For example the `Gyroscope` sensor can provide data (= `CMGyroData`) when using the class `CMMotionManager` resp. package `CoreMotion` in general.
If it is possible to access the sensor or access at least collected sensor data, do the following steps: 
1. create a new class for the sensor and inherit the `IStreamHandler` protocol. 
2. if the class, which provide access to the sensor should only be instantiated once: register the class in the `ManagerCollection` by creating a `get<name of the manager>Manager()` method, which returns a singleton instance
3. collect all necessary information about the sensor and use this information (e. g. accuracy, if known) to fill the related methods (e. g. `getSensorInfo()`) 
4. implement the protocol methods from the `IStreamHandler` by accessing the manager methods and format the retrieved data (c. f. `GyroscopeHandler` for a basic example, how the implementation could look like)
5. register the stream handler in the `init` method of the `SensorManager` by placing an instance in the corresponding map
6. document everything by adding comments (possible warnings, addional information, ...) and checking, whether the information already (completely) exist in the [sensor_information.md](sensor_information.md) file

## Sensor implementation information

See [sensor_information.md](sensor_information.md) for information about how the sensors work and how to implement them.
