# Unscented Kalman Filter Project
Self-Driving Car Engineer Nanodegree Program

---

## Sensor and Process Noise Matrix

Process noise standard deviation longitudinal acceleration = 2.5m/s^2

Process noise standard deviation yaw acceleration = 2.0rad/s^2.

Laser measurement noise standard deviation position1(x) = 0.15m.
  
Laser measurement noise standard deviation position2(y) = 0.15m.

Radar measurement noise standard deviation radius = 0.3m.

Radar measurement noise standard deviation angle = 0.03rad.

Radar measurement noise standard deviation radius change = 0.3m/s.

R_lidar_ << 0.0225, 0, 
			0, 0.0225;

R_radar_ << 0.09, 0, 0,
              0, 0.0009, 0,
              0, 0, 0.09;

## Model Accuracy

The algorithm gives as outputs [0.0369415, 0.0475329, 0.47795, 0.504106] for px, py, vx and vy RMSE which are less than or equals to the values [0.09, 0.09, 0.65, 0.65] when executed with the input file "sample-laser-radar-measurement-data-1.txt"

The algorithm gives as outputs [0.183759, 0.185465, 0.361421, 0.489954] for px, py, vx and vy RMSE which are less than or equal to the values [0.20, 0.20, 0.55, 0.55] when executed with the input file "sample-laser-radar-measurement-data-2.txt"

## Dependencies

* cmake >= v3.5
* make >= v4.1
* gcc/g++ >= v5.4

## Basic Build Instructions

1. Clone this repo.
2. Make a build directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`
4. Run it: `./UnscentedKF path/to/input.txt path/to/output.txt`. You can find
   some sample inputs in 'data/'.
    - eg. `./UnscentedKF ../data/sample-laser-radar-measurement-data-1.txt output.txt`

## Editor Settings

We've purposefully kept editor configuration files out of this repo in order to
keep it as simple and environment agnostic as possible. However, we recommend
using the following settings:

* indent using spaces
* set tab width to 2 spaces (keeps the matrices in source code aligned)

## Code Style

Please stick to [Google's C++ style guide](https://google.github.io/styleguide/cppguide.html) as much as possible.

## Generating Additional Data

This is optional!

If you'd like to generate your own radar and lidar data, see the
[utilities repo](https://github.com/udacity/CarND-Mercedes-SF-Utilities) for
Matlab scripts that can generate additional data.

## Project Instructions and Rubric

This information is only accessible by people who are already enrolled in Term 2
of CarND. If you are enrolled, see [the project page](https://classroom.udacity.com/nanodegrees/nd013/parts/40f38239-66b6-46ec-ae68-03afd8a601c8/modules/0949fca6-b379-42af-a919-ee50aa304e6a/lessons/c3eb3583-17b2-4d83-abf7-d852ae1b9fff/concepts/4d0420af-0527-4c9f-a5cd-56ee0fe4f09e)
for instructions and the project rubric.
