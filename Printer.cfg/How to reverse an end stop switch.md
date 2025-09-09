### Issue: 
When you run `QUERY_ENDSTOPS` it shoud report stepper_x: open stepper_y: open stepper_z: open, but it reports as triggered instead

### Fix:

1) Navigate to your printer.cfg
2) Go to the axis that has the issue  
3) Where it says endstpo_pin, either add an `!` or remove one that is already there  
4) Example:  
&emsp;  i) My X axis shows it is triggered when it isn't  
&emsp;  [stepper_x]  
&emsp;  step_pin: PB13  
&emsp;  dir_pin: !PB12  
&emsp;  enable_pin: !PB14  
&emsp;  microsteps: 16  
&emsp;  rotation_distance: 40  
&emsp;  endstop_pin: ^PC0 #Add an `!` to reverse it, so it would now be endstop_pin: !^PC0  
&emsp;  position_endstop: 0  
&emsp;  position_max: 235  
&emsp;  homing_speed: 50  
