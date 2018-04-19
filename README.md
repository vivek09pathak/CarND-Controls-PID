
Writeup Report

PID Controller Project

(Note - Hi , The visualization for the simulator on my machine is available at - https://youtu.be/dcjjD-29yKc)

The goals / steps of this project are the following:

    Tune the PID controller hyperparameters.
    Test the result on the simulator.
    Play around with the throttle.

Rubric Points
Here I will consider the rubric points individually and describe how I addressed each point in my implementation.
Writeup / README
1. Provide a Writeup / README that includes all the rubric points and how you addressed each one. You can submit your writeup as markdown or pdf. Here is a template writeup for this project you can use as a guide and a starting point.

You're reading it!
PID Controller
1. Student describes the effect of the P, I, D component of the PID algorithm in their implementation.
The PID controller has 3 main components:
    1.Proportional factor - it is a multiplication of cte error with proportional gain (p_error * cte)
    2.Differential factor - it is a multiplication of cte error rate with the differential gain (d_error * cte)
    3.Integral factor -It is a Steady state error obtained by previous steady error with integral gain (i_error * cte)

For the project, I used the p,i,d values from the classroom given in the PID impelementation lesson of the classroom-0.2 , 0.004 and 3.0. As it gave me decent result.

As I intitally thought of using twiddle,throttle control, but as my implementaion did not gave me as good result as by manual tuning of the hyperparameters.So I manually adjust the values.

For The PID implementation i tuned it at different parameters as started from classroom but I found that decreasing the proportional gain increased my rise time but decreased my overshoot and better stability so I kept it around 0.01.As for Intergral proportional I kept if around 0.001 as increasing the gain was causing longer time to settle down or getting.For Differential proportional it has some jerkiness at sharp turn but i kept it around 2.9 becausing increasing the gain was causing to get overdamped or deviate from its track so to make it centred oreinted i used this values though it has some jerkiness at sharp turns.

Discussion
1. Briefly discuss what could you do to make the implementation more robust?
Though manual tuning is not the correct way to impelement as i will try this one with different algorithms as i have more deep knowledge for PID implemetation using twiddle algo or controlling throttle etc.
