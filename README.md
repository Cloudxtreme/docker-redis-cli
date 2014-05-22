Mosquitto
=========

A Docker image for the Mosquitto MQTT Broker based on [crux][].

Usage
-----

    docker run -d -p 1883:1883 -p 8883:8883 prologic/mosquitto

You can also use this image/container as a MQTT (mosquitto) client.

    docker run -i -t prologic/mosquitto mosquitto_sub -h <host> -t <topic>

Where:

-   \<host\> is the Docker host where `prologic/mosquitto` is being run.
-   \<topic\> is the topic you wish to subscribe to.

Configuration
-------------

To configure Mosquitto, change certificates or add users, please modify the files found in `etc/mosquitto` in this repository to suit your needs. Then run with:

    docker run -d -p 1883:1883 -p 8883:8883 -v $(pwd)/etc/mosquitto:/etc/mosquitto prologic/mosquitto

  [crux]: https://index.docker.io/u/_/crux
