# stop-watch-system-with-ATmega32-Micro-controller
Project Overview

This project implements a stopwatch system using an ATmega32 microcontroller running at 1 MHz. The system utilizes six common anode 7-segment displays controlled through multiplexing, with time counting handled by Timer1 in CTC mode. External interrupts enable reset, pause, and resume functionalities.

Features
	•	Time Counting: Timer1 configured in CTC mode counts stopwatch time.
	•	7-Segment Display: Six common anode 7-segment displays connected via a 7447 decoder and controlled with transistors for multiplexing.
	•	Start on Power-Up: Stopwatch starts counting as soon as power is connected.
	•	Reset: A push button connected to INT0 resets the stopwatch (falling edge trigger).
	•	Pause: A push button connected to INT1 pauses the stopwatch (rising edge trigger).
	•	Resume: A push button connected to INT2 resumes the stopwatch (falling edge trigger).

Hardware Components
	•	ATmega32 Microcontroller (1 MHz clock)
	•	Six common anode 7-segment displays
	•	7447 BCD to 7-segment decoder
	•	NPN BJT transistors (for multiplexing)
	•	Push buttons (for reset, pause, and resume)
	•	Resistors (internal/external pull-up/pull-down)
	•	Wires, breadboard, and power supply

Pin Configuration
	•	PORTC (First 4 pins): Connected to 7447 decoder inputs.
	•	PORTA (First 6 pins): Enable/disable control for the 7-segments.
	•	INT0 (PD2): Reset button with internal pull-up.
	•	INT1 (PD3): Pause button with external pull-down.
	•	INT2 (PB2): Resume button with internal pull-up.

Multiplexing Technique

Multiplexing is used to control multiple 7-segment displays with fewer MCU pins. Only one display is powered at a time, but rapid switching creates the illusion of all displays being on simultaneously.

How to Use
	1.	Power up the system to start the stopwatch.
	2.	Press the reset button (INT0) to reset the stopwatch.
	3.	Press the pause button (INT1) to pause counting.
	4.	Press the resume button (INT2) to continue counting.
