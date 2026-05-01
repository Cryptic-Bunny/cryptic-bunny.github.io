---
title: Indvidual Api
---
Team 307's message protocol is as follows. The first and second bytes of every message sent through the UART will be 'AZ'. Followed by a third byte, the sender ID, which is just the sender's capitalized initial. The fourth is the receiver ID, the receiver's capitalized initial. The following bytes contain data defined by the types in the section below. Then the end of the message will be two bytes that write out 'YB'. Additionally, no messages will exceed 64 bytes.

An example of a message I will send out is "AZEAHelloYB".

The list of sender/receiver IDs is "A, D, E, G, J, and Z." With being my specific Sender ID.

# Message type 6 - Pressure

Message type 6 as specificed in the team data sheet will be the only message I send. 

| Byte 1–2 | Byte 3 | Byte 4 | Byte 5-62| Last 2 Bytes |
|---------------------|------------------|----------------------|-----------|-----------|
| AZ | E | A | Depth and pressure | YB |

The depth and pressure byte itself will have specific minimums and maximums associated to them. Pressure will have a minimum value of 30000 Kilopascals to 110000 Kilopascals. Depth meanwhile will have a value minimum of 0 meters to a maximum of 40000 meters.

# Other message types

My subsystem is able to recieve other message types from across the group and pass them along. It does nothing with the data outside of copying it and sending the copy.
