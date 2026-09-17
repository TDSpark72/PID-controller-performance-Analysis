# PID-controller-performance-Analysis

📌 Project Overview

This project presents the simulation and performance analysis of a Proportional–Integral–Derivative (PID) controller using MATLAB Simulink. The objective is to study how different PID parameters affect the transient and steady-state response of a closed-loop control system.

A first-order plant is controlled using a PID controller, and the system response is observed through a Scope. Different combinations of \(K_p\), \(K_i\), and \(K_d\) are tested to analyse overshoot, settling behaviour, rise time, and steady-state error.


---

🎯 Objectives

To design a closed-loop PID control system in MATLAB Simulink.

To understand the individual effects of P, I, and D actions.

To analyse the system's transient and steady-state response.

To compare system responses for different PID gain values.

To reduce overshoot and settling time while maintaining accurate tracking.

To understand the practical application of PID control in engineering systems.



---

🛠️ Software & Tools

MATLAB

Simulink

PID Controller Block

Step Input

Transfer Function

Gain

Scope

Feedback Loop



---

⚙️ System Model

The implemented closed-loop system consists of:

┌──────────────────────────────────────────────┐
          │                                              │
          │                    Feedback                   │
          │                                              ▼
Step ──► (+) ──► PID Controller ──► Plant ──► Gain ──► Output
         (−)                                      │
          ▲                                        │
          └────────────────────────────────────────┘

Plant Transfer Function

The plant used in the simulation is:

\[
G(s)=\frac{1}{0.5s+1}
\]

The overall system therefore consists of a PID controller followed by a first-order plant with unity feedback.


---

🧮 PID Controller

The continuous-time PID controller is represented by:

\[
C(s)=K_p+\frac{K_i}{s}+K_d s
\]

where:

\(K_p\) = Proportional gain

\(K_i\) = Integral gain

\(K_d\) = Derivative gain


The derivative action in the Simulink PID block also uses a filter coefficient to reduce the effect of high-frequency noise.


---

🔬 Simulation Experiments

Several PID parameter combinations were tested during the simulation.

Test	\(K_p\)	\(K_i\)	\(K_d\)

Test 1	20	40	1.0
Test 2	50	45	1.8
Test 3	30	45	1.8
Test 4	20	40	1.5


The system response was monitored using the Simulink Scope.


---

📊 Observations

The simulations show that changing the PID gains significantly changes the transient response.

Proportional Gain \(K_p\)

Increasing \(K_p\):

Makes the controller respond more strongly to error.

Generally reduces rise time.

Can increase overshoot and oscillations if excessively high.

Improves tracking response.


Integral Gain \(K_i\)

Increasing \(K_i\):

Helps eliminate steady-state error.

Improves final tracking accuracy.

Excessive integral gain can produce overshoot and slower settling.


Derivative Gain \(K_d\)

Increasing \(K_d\):

Provides damping to the system.

Can reduce overshoot.

Improves transient response.

Excessive derivative action may amplify measurement noise.



---

📈 Simulation Result

The Scope output demonstrates that the controlled system initially exhibits a transient response with overshoot, followed by damping and convergence toward a steady operating value.

The different simulations demonstrate the effect of PID tuning on:

Rise time

Peak overshoot

Settling time

Stability

Steady-state response


This comparison helps in selecting appropriate PID parameters for a desired control response.


---

🔄 Working Principle

1. A Step Input provides the desired reference value.


2. The reference is compared with the feedback signal at the summing junction.


3. The difference produces the error signal.


4. The PID controller processes this error.


5. The controller output is applied to the first-order plant.


6. The plant produces the system output.


7. The output is fed back to the summing junction.


8. The PID continuously adjusts the control action according to the error.


9. The Scope displays the resulting system response.




---

🚀 Applications

PID controllers are widely used in:

Industrial process control

Motor speed control

Temperature control

Robotics

Power-system control

Voltage regulation

Industrial automation

Aerospace and telemetry systems

Automotive control systems

Level and flow control



---

💡 Key Learning Outcomes

Through this project, the following concepts were studied:

Closed-loop control systems

Feedback control

PID control theory

MATLAB Simulink modelling

Transfer functions

Transient and steady-state response

PID parameter tuning

Overshoot and settling behaviour

Controller performance analysis



---

🔮 Future Scope

The project can be further enhanced by:

Implementing automatic PID tuning.

Comparing PID with PI and PD controllers.

Adding external disturbances and measurement noise.

Comparing Ziegler–Nichols, Cohen–Coon and automated tuning methods.

Implementing adaptive or fuzzy PID control.

Applying the controller to an actual motor or industrial process model.

Comparing performance using quantitative parameters such as ISE, IAE and ITAE.



---

📁 Project Structure

PID-Controller-Simulation/
│
├── PID_Controller_Simulation.slx
├── README.md
├── Results/
│   ├── PID_Response_1.png
│   ├── PID_Response_2.png
│   └── PID_Response_3.png
│
└── Documentation/
    └── Project_Report.pdf


---

👨‍💻 Project Summary

Simulation and Analysis of PID Controller is a MATLAB Simulink-based control-system project that demonstrates the design, simulation, and analysis of a closed-loop PID-controlled first-order system. By varying \(K_p\), \(K_i\), and \(K_d\), the project studies how controller tuning influences system stability, transient response, overshoot, settling behaviour, and tracking accuracy.

Technologies: MATLAB Simulink PID Control Control Systems Transfer Function Feedback Control
