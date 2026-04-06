# Compare and contrast MQTT with other communication protocols

## Instructions

This lesson covered MQTT as a communication protocols. There are others, including AMQP and HTTP/HTTPS.

Research these both and compare/contract them with MQTT. Think about power usage, security, and message persistence if connections are lost.

## Rubric

| Criteria | Exemplary | Adequate | Needs Improvement |
| -------- | --------- | -------- | ----------------- |
| Compare AMQP to MQTT | Is able to compare and contrast AMQP to MQTT and covers power, security, and message persistance. | Is partly able to compare and contrast AMQP to MQTT and covers two of power, security, and message persistance. | Is partly able to compare and contrast AMQP to MQTT and covers one of power, security, and message persistance. |
| Compare HTTP/HTTPS to MQTT | Is able to compare and contrast HTTP/HTTPS to MQTT and covers power, security, and message persistance. | Is partly able to compare and contrast HTTP/HTTPS to MQTT and covers two of power, security, and message persistance. | Is partly able to compare and contrast HTTP/HTTPS to MQTT and covers one of power, security, and message persistance. |


Submission: Comparison of MQTT, AMQP, and HTTP/HTTPS
Feature	MQTT	AMQP	HTTP / HTTPS
Communication Model	Publish/Subscribe	Queue-based (Message broker)	Request/Response
Power Usage	Very low (lightweight)	Medium	High
Bandwidth Usage	Low	Medium	High
Ideal Use Case	IoT devices, sensors	Enterprise messaging systems	Web communication, APIs
Connection Type	Persistent connection	Persistent connection	Stateless (new request each time)
MQTT vs AMQP
Power Usage

MQTT is designed to be lightweight, so it uses very little power. This makes it ideal for small IoT devices running on batteries.
AMQP is heavier and requires more processing, so it consumes more power and is less suitable for low-power devices.

Security

Both MQTT and AMQP support secure communication (e.g., TLS encryption).
However, AMQP has more advanced built-in security features, such as authentication and access control mechanisms, making it stronger for enterprise systems.

Message Persistence (when connection is lost)

MQTT supports Quality of Service (QoS) levels:

QoS 0: no guarantee
QoS 1: at least once
QoS 2: exactly once

This allows some level of message reliability.

AMQP has stronger message persistence:

Messages can be stored in queues
Guaranteed delivery even if systems go offline

👉 Conclusion:
MQTT is better for simple, low-power IoT communication, while AMQP is better for reliable, enterprise-grade messaging systems.

MQTT vs HTTP/HTTPS
Power Usage

MQTT uses a persistent connection and minimal data packets, so it consumes very little power.
HTTP/HTTPS requires a new request-response cycle each time, which increases power consumption and is inefficient for IoT devices.

Security

HTTP becomes HTTPS when using TLS encryption, which provides strong security.
MQTT can also use TLS, but security depends more on implementation.

👉 In practice: HTTPS is more standardized and widely used for secure communication.

Message Persistence (when connection is lost)

MQTT supports message delivery through QoS and can store messages temporarily on the broker.
HTTP/HTTPS does not support persistence:

If the connection fails, the request is lost
The client must resend the request manually

👉 Conclusion:
MQTT is much better for continuous data streaming and unreliable networks, while HTTP/HTTPS is better for web services and one-time requests.

Final Summary
MQTT: best for low-power, real-time IoT communication
AMQP: best for reliable, secure enterprise messaging
HTTP/HTTPS: best for web-based communication but inefficient for IoT

Overall, MQTT is the most suitable protocol for IoT devices because it balances low power usage with acceptable reliability.
