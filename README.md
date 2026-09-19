# rov-gesture-control-glove
ESP32 + flex-sensor glove sending real-time directional commands over UDP to an ROV, with Raspberry Pi YOLO object detection for visual feedback
Gesture-Controlled ROV Interface (ESP32 Glove + Raspberry Pi + YOLO)

A gesture-controlled ROV system. A flex-sensor glove built around an ESP32 sends real-time directional commands over UDP to a Raspberry Pi mounted on the ROV, which drives the motors and runs YOLO-based object detection to give the operator visual feedback.

Final year project, 2025–2026.  Guided by [Dr Tuhina Halder, Department: ECE, Institution: ST. Thomas' College of Engineering and Technology].

System Overview
Flex-sensor glove ──► ESP32 ──► UDP over Wi-Fi ──► Raspberry Pi ──► Motor drivers ──► ROV thrusters/motors
                                                        │
                                                        └──► Camera ──► YOLO object detection ──► visual feedback



Layer	Components
Sensing	Flex-sensor glove [3]
Processing and transmission	ESP32 [Dev Module]
Wireless link	UDP over Wi-Fi
ROV controller	Raspberry Pi [4B]
Actuation	[DC Motor 5V]
Vision	[Pi camera], YOLO [version 8]
My Contribution (ROV / Raspberry Pi Side)

I was responsible for the ROV side of the system:

Set up the Raspberry Pi (OS, dependencies, and configuration for the ROV)
Trained/deployed the YOLO object detection model [version 8, what it detects: Aquatic life]
Implemented motor operation and control on the ROV, driven by the incoming directional commands
Teammate's Contribution (Glove Side)

[Srijani(ssreyz)] built the glove side of the system:

Flex-sensor glove and ESP32 hardware
Gesture sensing and command generation
UDP communication link between the glove and the ROV
Photos


License

Released under the MIT License.
