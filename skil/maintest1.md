```cpp
#include "robot-config.h"     

using namespace vex;

int main() {
    Brain.Screen.print("maintest1 shoop da woop");
    while(1) {
        FrontLeftMotor.spin(vex::directionType::fwd, (Controller1.Axis1.value() + Controller1.Axis3.value())/2, vex::velocityUnits::pct);
        FrontRightMotor.spin(vex::directionType::fwd, (Controller1.Axis1.value() - Controller1.Axis3.value())/2, vex::velocityUnits::pct);
        BackLeftMotor.spin(vex::directionType::fwd, (Controller1.Axis1.value() + Controller1.Axis3.value())/2, vex::velocityUnits::pct); 
        BackRightMotor.spin(vex::directionType::fwd, (Controller1.Axis1.value() - Controller1.Axis3.value())/2, vex::velocityUnits::pct);
        
		vex::task::sleep(20);
    }

}
