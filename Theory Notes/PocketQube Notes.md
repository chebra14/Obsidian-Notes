
#### Creating Firmware 

Create objects in high level language
- code reusability
- Nice ways of testing and tracing
	- If something is going wrong you can trace to the source
	- Create modules (abstraction layers)

Define a standard
- Naming conventions
- Structural conventions
	- Naming conventions
	- Where is a function definition (Structural)
	- Filing convention

##### 3 Categories of Packages

Board support package creates abstraction from pins
- Extract main behaviour
- Essentially HAL library
Application packages
- Functional code
- Ex. robotic arm - different functions
	- Control of each link in the arm
- Function that makes the board unique
- INTERPERATE COMMAND
Telemetry and Tele-commands Structure (Message hub/passing structure)
- External instructions, information out of the system
- How does one application talk to another one
- Ex. Windows
	- One program talking to another app
	- Global variables (an example of a bad one)
- Sharing information
- PASS INFORMATION
Main loop
Interupt subrootine - lean as possible
If it looks dodgy and messy, it is dodgy.
Neatness and refactoring is important

When there is contention in sequence caused by an interupt
if (controlflag == true && input == true)
	//Error