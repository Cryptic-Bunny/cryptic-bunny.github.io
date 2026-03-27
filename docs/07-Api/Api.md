---
title: Indvidual Api
---

# Message type 1 - Set motor Command

|  | Byte 1 | Byte 2-3 | Byte 4-5 |
|---|---|---|---|
| Variable Name | Message type | Direction | Speed |
| Variable Type | Uint8_t | Uint16_t | Uint16_t |
| Min Value | 0 | 0 | -100 |
| Max Value | 12 | 360 | 100 |
| Example | 1 | 180 | 50 |

# Message type 2 - Motor status

|  | Byte 1 | Byte 2 | Byte 3-4 |
|---|---|---|---|
| Variable Name | Message type | Motor state | Speed |
| Variable Type | Uint8_t | Uint8_t | Uint16_t |
| Min Value | 0 | 0 | -100 |
| Max Value | 12 | 1 | 100 |
| Example | 2 | 1 | 50 |

## Message type 3 - Distance from any objects

|  | Byte 1 | Byte 2-3 |
|---|---|---|
| Variable Name | Message type | Distance |
| Variable Type | Uint8_t | Uin8_t |
| Min Value | 0 | 0 |
| Max Value | 12 | 100 |
| Example | 3 | 46 |

# Message type 4 - Hall effect sensor value

|  | Byte 1 | Byte 3 |
|---|---|---|
| Variable Name | Message type | Hall Value |
| Variable Type | Uint8_t | Uint16_t |
| Min Value | 0 | 0 |
| Max Value | 12 | 360 |
| Example | 4 | 180 |

# Message type 5 - Pressure

|  | Byte 1 | Byte 2 |
|---|---|---|
| Variable Name | Message type | Pressure |
| Variable Type | Uint8_t | Uint8_t |
| Min Value | 0 | 30 |
| Max Value | 12 | 110 |
| Example | 5 | 104 |

# Message type 6 - Temperature

|  | Byte 1 | Byte 2-3 |
|---|---|---|
| Variable Name | Message type | Temprature |
| Variable Type | Uint8_t | Uint16_t |
| Min Value | 0 | 0 |
| Max Value | 12 | 300 |
| Example | 6 | 80 |

# Message types 7 and 8

These two message types, for the most part, will just be ignored by my subsystem as they have
no bearing on the pressure sensor, and the people who need them will get the messages before
my subsystem.

## Message type 9 - Status request

|  | Byte 1 |
|---|---|
| Variable Name | Message type |
| Variable Type | Uint8_t |
| Min Value | 0 |
| Max Value | 12 |
| Example | 9 |

## Message type 10 - Status response

|  | Byte 1 | Byte 2 |
|---|---|---|
| Variable Name | Message type | Status code |
| Variable Type | Uint8_t | Uint8_t |
| Min Value | 0 | 0 |
| Max Value | 12 | 1 |
| Example | 10 | 1 |

## Message type 11 - Error code

|  | Byte 1 | Byte 2 |
|---|---|---|
| Variable Name | Message type | Error Code |
| Variable Type | Uint8_t | Uint8_t |
| Min Value | 0 | 0 |
| Max Value | 12 | 1 |
| Example | 11 | 1 |

## Message type 12 - Emergency stop

|  | Byte 1 |
|---|---|
| Variable Name | Message type |
| Variable Type | Uint8_t |
| Min Value | 0 |
| Max Value | 12 |
| Example | 12 |
