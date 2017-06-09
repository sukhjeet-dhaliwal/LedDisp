# Arduino LedDisp
## Getting Started

A sample code for a four-digit common anode display is shown below:

```arduino
#include <LedDisp.h>

LedDisp disp(11,7,3,5,6,10,2);

const int numOfDigits=4;
int digitPins[numOfDigits]={12,9,8,13};

void setup() {
  
  disp.setDigitPins(numOfDigits, digitPins);
	disp.setCommonAnode();
}  

void loop() {

    disp.write(13.28);

}
```

Key functionality includes:

- Supports arbitrary number of digits and multiple displays
- Supports displays with decimal points, colon and apostrophe
- Supports common anode, common cathode and other hardware configurations
- High level printing functions for easily displaying:
  - Numbers (integers, fixed point and floating point)
  - Text strings
  - Time (hh:mm) or (mm:ss)
- Automatic multiplexing with adjustable refresh rate
- Adjustable brightness through duty cycle control
- refreshDisp() to keep display bright after update once using write().
- Leading zero suppression.

For further information, please see the attached user guide.
