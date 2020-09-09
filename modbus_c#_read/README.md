# Requirements

Using Modbus TCP protocol, connect to a PLC controller. IP address, port number and slave address will be provided in a separate email.
All three parameters (ip address, port number and slave address) should be configurable.

Once connected to the PLC controller start reading temperature and humidity values at every X seconds. Again this should be a configurable option, which default to 3 seconds.

Temperature and humidity addresses are listed in the table below:

| value       | startAddress | numberOfPoints | data type |
|-------------|--------------|----------------|-----------|
| Temperature | 2412         | 2              | float     |
| Humidity    | 2414         | 2              | float     |

New temperature and humidity values, which are different from the previously read values, should be sent via web socket to the client. Simulate socket communication with empty method or console.writeline, or comment in the code. Just make it clear where actual socket channel call will occur.

Finally, write current temperature and humidity values in Sqlite database at every 60 seconds interval.

## Technologies and Solution

Using .NET Core and C#.
Send us a link to a github repository with the solution.

## Hints

1. For modbus communication you can use [NModbus](https://www.nuget.org/packages/NModbus/) or research and use a library of your choice.
   1. Check github repository for samples how to use the library. More specific, see *ModbusTcpMasterReadInputs* example, which is the closest provided code for your needs.
   2. Described registers in the previous section are “holding” registers, so you can use corresponding methods for reading.
2. Convert ushort to float - [check this solution](https://stackoverflow.com/a/9130551/536196)

## Bonus

Add unit and/or integration tests.
