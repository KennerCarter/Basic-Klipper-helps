## There are two main ways to reverse the direction of a stepper motor

### 1) In the firmware (recommended)

  a) Go to your printer.cfg file and open it
  b) Go to the axis that is moving in the wrong direction (CoreXY is different)
  c) Under that header and where it says dir_pin put an ! in front of the pin location
  d) Example:
    i) My X axis is moving in the wrong direction
    [stepper_x]
    step_pin: PB13
    dir_pin: !PB12 #I would remove the "!" in front of PB12 so it would be dir_pin: PB12
    enable_pin: !PB14
    microsteps: 16
    rotation_distance: 40
    endstop_pin: ^PC0
    position_endstop: 0
    position_max: 235
    homing_speed: 50

### 2) Changing the wiring

  a) Either find a wiring diagram/ pinout of your control board, OR find a multimeter
  b) In a stepper motor, there are two circuits (assuming it is a four-wire motor), and we need to switch to pins that are in the same circuit
  c) find which pins correspond with which circuit, and push the pins out and swap them.
