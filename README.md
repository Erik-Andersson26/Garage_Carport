Hörmann Garage Door Controller (Raspberry Pi)
A Raspberry Pi–based home automation project that remotely controls a Hörmann garage door motor by simulating a physical button press on the motor's external control input.
How it works
A relay module is wired to the Hörmann motor's external push-button terminals (the same input used by a wired wall button). The Raspberry Pi triggers a brief momentary pulse via GPIO to close the relay contact for a fraction of a second — exactly replicating a manual button press — which opens, stops, or closes the door depending on its current state.
Hardware

Raspberry Pi 3
5V relay module (single channel)
Jumper wires connecting the Pi's GPIO to the relay, and the relay's NO/COM contacts to the motor's external button terminals

Software

Python 3 with RPi.GPIO
A simple script pulses the configured GPIO pin high for ~0.5s to actuate the relay

Status
Early stage — GPIO-to-relay wiring and pulse trigger logic implemented; next steps include wrapping the trigger in a small API/web endpoint for remote control.
