# Automation
The general purpose of automation is to simplify or replace human tasks, such as car driving. To achieve this, engineers must first develop a deep understanding of the systems they want to automate. This includes creating a useful mathematical model that accurately describes the system’s behavior. 
Once the system is well understood, engineers can design algorithms to perform three key tasks:

- Monitoring and Evaluation – An algorithm to measure the current status of the system and compare it with a desired goal state.
- Control – An algorithm to determine the necessary actions the system must perform in order to reach the goal.
- Actuation – An algorithm to execute all the required actions so that the system can achieve its tasks.

In general, this MCA (measurement, control, actuation) process forms a feedback loop, meaning that the system's output can be reused as input to maintain the desired status.

This is sufficient for an introduction to the topic. One final point to mention is that systems can be static or dynamic
- Static systems are influenced only by their initial state and have no memory of what happens over time—they are often called memoryless.

- Dynamic systems, on the other hand, are influenced by both their current state and their history over time.

Why this distintion is important? because it determines the type of  mathematical model we use. For dynamic systems, a valid mathematical model usually requires differential equations to describe how the system evolves over time. This is why the first lecture focuses on differential equations.

## AUTOMATION LESSONS

- [Differential Equation](lectures/diff/differential.md)
- [Cauchy](lectures/cauchy/cauchy.md)
- [Matrix representation of differential equation](lectures/matrix/mtrix.md)