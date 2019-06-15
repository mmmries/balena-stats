> This project is based on [balena sense](https://github.com/balena-io-projects/balena-sense).

## Balena Stats

The goal of this project is to make it extremely simple to get a raspberry pi setup in your house that can receive sensors readings and provide graphs.

It uses InfluxDB to receive and store the sensor readings and Grafana to create graphs.
For detailed setup instructions you can follow [the balena-sense blog post](https://www.balena.io/blog/build-an-environment-and-air-quality-monitor-with-raspberry-pi/#settinguptheraspberrypi).
When you get to the step about cloning in balena-sense, just clone this repository instead and the rest of the instructions will work.

## Other Changes

This project turns on the InfluxDB UDP listener in order to get the simplest possible way of receiving sensor readings.
Your project can use the [UDP Protocol](https://docs.influxdata.com/influxdb/v1.7/supported_protocols/udp/) to send in sensor readings.
Just look at the balena dashboard to find the loal IP address of your PI and then have any of your other devices send UDP packets to port `8089`.
