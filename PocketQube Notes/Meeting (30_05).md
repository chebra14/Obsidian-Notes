#### Structure

- Look at low profile header
- Maybe move the boards higher
#### Connectors/Connections

- JST 4-pin, 1.25mm (Solar Panel connection)
- 5-pin 90 degree male-male, 1.27 pitch (ST Link and UART)
	- Must be flush with the board

##### Main Header:

- Changed configuration (EPS_RST Pin) 
- Height will change based on connector
##### ST Link:
- 3.3, swclk, GND, swdio, nsrt (1-5)
##### UART Debugger:
- 3.3, GND, TX, RX, NC
*NC = No Connect
##### RS485:
- No Populate on the A and B pull-up and pull-down resistors
##### LED:
- JLC Part number (C138543)

#### Mounting Holes
- See photo for foorprint
- NC to a ground
#### Resistors and Capacitors
- 0603 Imperial (OBC - 0201 Top)

- Resistors
	- 120 (LED)
	- 4k7
	- 120k
- Dean must check why he's using
	- 25 m
	- 50 m
	- \5k
	- 4k7
	- 10k
	- 11.2k
	- 26.7k
	- 29.4k
	- 100k
	- 120k
	- 137k
	- 222k
	- 667k
	- 1M
	- 6.8M

- Capacitors
	- 10u
	- 8p (OBC Clocks)
	- 12p (OBC Clocks)
	- 100n
	- 10n
	- 1u
	- 22u
	- 4.7u
	- 47u
	- 22n
	- 150u

#### Design Rules
- Checked in Meeting

General:

- Dean and Dane to give PCB by Tuesday
- Niel by Wednesday
