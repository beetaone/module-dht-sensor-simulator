# DHT sensor simulator

|         |                                                                               |
| ------- | ----------------------------------------------------------------------------- |
| name    | DHT sensor simulator                                                          |
| version | v1.0.1                                                                        |
| GitHub  | [dht-sensor-simulator](https://github.com/beetaone/module-dht-sensor-simulator) |
| authors | Paul Gaiduk                                                                   |

---

## Table of Content

-   [DHT sensor simulator](#dht-sensor-simulator)
    -   [Table of Content](#table-of-content)
    -   [Description](#description)
    -   [Features](#features)
    -   [Environment Variables](#environment-variables)
        -   [Module Specific](#module-specific)
        -   [Set by the beetaone Agent on the edge-node](#set-by-the-beetaone-agent-on-the-edge-node)
    -   [Dependencies](#dependencies)

---

## Description

DHT sensor simulator module emits temperature (in °C) and humidity (in %) data periodically as if they would be comming from a sensor.

## Features

-   Emits realistic temperature and humidity data in JSON format.

## Environment Variables

### Module Specific

The following module configurations can be provided in a data service designer section on beetaone platform:

| Name               | Environment Variables | Type    | Description                               |
| ------------------ | --------------------- | ------- | ----------------------------------------- |
| Temperature label  | TEMP_LABEL            | string  | Label for the temperature data.           |
| Humidity label     | HUMIDITY_LABEL        | string  | Label for the humidity data.              |
| Data send interval | SLEEP_INTERVAL        | integer | Time interval (sec) between the messages. |

Other features required for establishing the inter-container communication between modules in a data service are set by beetaone agent.

### Set by the beetaone Agent on the edge-node

| Environment Variables | type   | Description                            |
| --------------------- | ------ | -------------------------------------- |
| EGRESS_URLS           | string | HTTP ReST endpoint for the next module |
| MODULE_NAME           | string | Name of the module                     |

## Dependencies

The following are module dependencies:

-   requests