
# **PID Controller** 
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)


Reflection
---
## the effect each of the P, I, D components
  * P: P component is proportional to the current Cross Track Error (CTE). That means the P term compensates steering angle in proportion to CTE.
  * I: I component is the integral of the CTE over time. This term eliminates residual error. If the car wheels are misaligned, there will still be a bias in the PD model after sufficient time has passed. The I component decreases the bias because the I value increases until the bias becomes zero.
  * D: D component is difference between current and previous value of CTE. This term prevents overshooting of the result.

## the final hyperparameters
  I first tried the final parameter setting (P, I, D) = (0.2, 3.0, 0.004) in the lecture. However, the vehicle follows a path like a circle. I realized there is no misalignment of wheels in the simulator and I fixed the I to zero. However, there is overshooting problem so I increased the D to 5. The final hyperparameter is (P, I, D) = (0.2, 0.0, 5)



