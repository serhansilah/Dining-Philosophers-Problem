# Dining-Philosophers-Problem
Barriers and Dining Philosophers Problem Using Java Threads  

In this project, I used Java threads and semaphores 
to implement a solution for a modified version of famous Dining Philosophers problem.

Task & Implementation Details

Here’s a short description of the problem: We have five forks, five plates and our five philosophers. 
At the beginning, philosophers are not at the table and they need to walk towards table. 
One philosopher can walk faster or slower than another philosopher, because of that philosophers 
must walk towards the table for a random amount of time, between 1 to 10 seconds. 
After reaching to the table, a philosopher must put his plate on the table and must wait for other philosophers.
When five philosophers sit around the table, they can start dining.
We will have five Java threads, one for each philosopher. 
While a philosopher waits other philosophers, the thread of the philosopher must be blocked 
until other philosophers arrive to the table. To achieve this, we must implement a Barrier for 5 threads.
When dining, these philosophers can either think or eat. In order to eat, they need 
two forks, the one on their left and the one on their right. If the forks are available,
they start eating; otherwise they need to wait until both forks are available. 
Due to different scenarios, as discussed in class, these philosophers may be deadlocked or they might starve.
We need an algorithm to avoid these situations.
We need to implement an algorithm so that no philosopher starves and they are never deadlocked. 
We should make use of semaphores and mutexes in order to achieve this.
Each philosopher thinks for a random amount of time, between 0 to 10 seconds. 
The thinking time should vary for each philosopher at each iteration, so we need to make use of random number generators.
After that, he becomes hungry and decides to eat. When a philosopher is hungry, his plate should turn red. 
If he can eat, then he starts eating; otherwise he waits in a hungry state (he doesn’t go back to thinking!).
When he is eating, his plate should turn blue After he finishes eating, he will go back to thinking. 
While the philosopher is thinking, his plate should be black and white. This procedure goes on forever.
For the duration of the program, we should also pay attention to the forks; the ones that are picked up and 
being used should be red, while the idle ones should stay black and white. 
Note that a philosopher does not pick any forks up while he is hungry, forks should only be picked up 
when the philosopher is allowed to eat.
