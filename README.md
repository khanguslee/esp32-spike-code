# ESP32 Spike Code

Random ESP32 code to test things out.

## Contents

### Last Will and Testament

Tests out how the Last Will and Testament feature works. 

On connection to the broker, the ESP32 device will publish to a `sensor/1/status` topic with the message `Online`. If the ESP32 disconnects from the broker, the broker will send a last will message to all subscribers to this topic. This last will message is set so that it updates the `sensor/1/status` topic with an `Offline` message. When the ESP32 client is online, it will send the message `Hello World` every 5 seconds to the topic `sensor/1/data`.

#### Requirements

Needs to have the `PubSubClient` library installed. This can be added using the Arduino Library Manager.
