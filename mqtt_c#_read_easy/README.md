# Requirements

Using MQTT protocol, connect to a MQTT broker. IP address, port number and credentials will be provided in a separate email.

Subscribe to the topic "ondo/measuring_box" where you will recieve messages about temperature and humidity measured by a measuring box sensor every 5 seconds.
Data will be published in Json format in the following schema:

```json
{
  "temperature": 10.5,
  "humidity": 65.5
}
```

Where temperature and humidity are floating point numbers.
You need to parse the received message and dump the received data in the console.
If measured temperature is equal to 20.8, print message "Target temperature reached" again in the console.

## Technologies and Solution

Using .NET Core and C#.
Send us a link to a github repository with the solution.

## Hints

1. For mqtt communication you can use [MQTTnet](https://github.com/dotnet/MQTTnet) or research and use a library of your choice.
    1. Check github repository for samples how to use the library.

## Bonus

Add unit and/or integration tests.
