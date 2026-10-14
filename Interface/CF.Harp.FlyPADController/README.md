## About

`CF.Harp.FlyPADController` provides an asynchronous API and reactive operators for data acquisition and control of [FlyPADController](https://fchampalimaud.github.io/hwsw_docs/docs/flypad-controller/overview) devices.

## How to Use

To use `CF.Harp.FlyPADController` for visual reactive programming, please install this package using the [Bonsai package manager](https://bonsai-rx.org/docs/articles/packages.html).

The package can also be used from any .NET application:
```c#
using CF.Harp.FlyPADController;

using var device = await Device.CreateAsync("COM3");
var whoAmI = await device.ReadWhoAmIAsync();
var deviceName = await device.ReadDeviceNameAsync();
var timestamp = await device.ReadTimestampSecondsAsync();
Console.WriteLine($"{deviceName} WhoAmI: {whoAmI} Timestamp (s): {timestamp}");
```

## Additional Documentation

For additional documentation and examples, refer to the [official FlyPADController documentation](https://fchampalimaud.github.io/hwsw_docs/docs/flypad-controller/overview).

## Feedback & Contributing

`CF.Harp.FlyPADController` is released as open-source under the [MIT license](https://licenses.nuget.org/MIT). Bug reports and contributions are welcome at [the GitHub repository](https://github.com/fchampalimaud/device.flypadcontroller).