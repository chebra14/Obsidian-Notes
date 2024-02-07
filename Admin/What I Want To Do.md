To develop a planning and control strategy that can be used on new surfaces types to identify the friction coefficient and then use the identified value to control the vehicle at high-speed.

I want to develop a way for any vehicle to drive the fastest it can on a track. When the car goes on the racing line, the line can either be very geometric (minimum curvature trajectory) or can be very square ("point-and-shoot"). 

Perhaps there needs to be a way to determine at what point on this spectrum between geometric and square the car needs to choose to drive on. I need to find where the limit is. After that, knowing where to sit on either side can be chosen by the car. The type of car and terrain will determine what the line should be, and how much to slide by (but it is not clear if the slide determines the line or vice versa).

I want the car to be able to drive any vehicle at the limit. So the control system must be able to adapt the slide to any car.

The limit:
The goal of driving on the limit is to drive the car where all 4 wheels are driving at its maximum potential at all times.


![[traction_circle.gif]]

WHAT MAY BE OUT OF MY SCOPE:
- Find the limit. (10% chance out).
- Decide how much to slide. (50% chance out).
- Control the slide. (30% chance out).
- Deciding what the line should be. (80% chance out). Perhaps just choose lines for now.

ISSUES:
- What is the relationship between tire slip angle (assuming neutral steer) (WHAT THE TIRES ARE DOING) and the vehicle side-slip angle (WHAT THE PLATFORM IS DOING).
- What is the relationship between friction and/or track geometry and/or car properties, to the amount of sliding required.

ONCE THESE ISSUES ARE SOLVED:
- The "Decide how much to slide" step can be SOLVED.

### SUMMARY:

The friction must be mapped for different inputs. This map tells the car **HOW** to slide or its sliding capabilities. The friction in relationship to car and track properties tells the car **WHERE** AND **WHEN** to slide. These properties can come from the racing line focus. For my own topic, this can just be hard coded for now. This is of course under the assumption that my theory about an amount of sliding is beneficial in certain situations. 

A control system is required to do the slide.

Simplistically, there must be a light to come on when the car is at the intended friction limit.