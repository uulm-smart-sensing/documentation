# Sensors

## Guideline on how to add support for a new sensor

When adding a new sensor to our `sensing_plugin` the following steps should be followed. It's best to do all of the steps in the [Flutter](#flutter) section first.

### Flutter

1. Add a new value to the `SensorId` enum in [api_sensor_manager.dart](https://gitlab.uni-ulm.de/se-anwendungsprojekt-22-23/sensing-plugin/-/blob/main/pigeons/api_sensor_manager.dart).

    ```dart
    enum SensorId {
        ...
        newSensor,
    }
    ```

2. If the unit of the values that the sensor produces is not already present, add the unit to the `Unit` enum in [api_sensor_manager.dart](https://gitlab.uni-ulm.de/se-anwendungsprojekt-22-23/sensing-plugin/-/blob/main/pigeons/api_sensor_manager.dart).

    ```dart
    enum Unit {
        ...
        // New unit category
        newUnit,
    }
    ```

3. Consider adding units from the same category to which the values can be converted to.
4. If a new unit is added, an according conversion method must be added in [unit_converter.dart](https://gitlab.uni-ulm.de/se-anwendungsprojekt-22-23/sensing-plugin/-/blob/main/lib/src/preprocessing/unit_converter.dart).

    ```dart
    final unitConversionMethods = <Unit, double Function(double, Unit, Unit)>{
        ...
        Unit.newUnit: _convertNewUnitCategory,
    };

    ...

    double _convertNewUnitCategory(
        double value,
        Unit sourceUnit,
        Unit targetUnit,
    ) {
        ...
    }
    ```

5. The best way to convert units within a category is to convert each source unit to a single unit and then convert that unit to the target unit.
6. Don't forget to add conversion tests in [unit_converter_test.dart](https://gitlab.uni-ulm.de/se-anwendungsprojekt-22-23/sensing-plugin/-/blob/main/test/preprocessing/unit_converter_test.dart).
7. Now you are all set up to implement the sensors on Android and iOS.

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
