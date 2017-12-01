

## Reflection

Describe the effect each of the P, I, D components had in your implementation.

* Proportional portion of the controller steers the car towards center line in proportion to Cross Track Error (CTE). For higher values of the car overshoots the central line very quickly and could even go off road. For certain this behaviour isnt expected on a road with traffic.
* Differential portion takes the Propportional into account and reacts to balance the P effect and avoid overshooting. The higher value of D makes the cars ome to center quickly but the movement of CAR is very jerky.
* Integral portion makes the CAR to avoid any bias towards the CTE that could make the controller to retain a constant error. 

Hyperparameters are tuned manually. I measured the CTE and tried to keep this as low as possible. At the turns in some case the CTS was close to 1 in some instances, though the car motion appeared to be smooth and at the center of the track. Final values choosen were: (0.2, 0.004, 3.5)

