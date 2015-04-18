This projects was written in C programming language and it is not an RTOS with a lot functions to manage registers, priorities and so forth for microcontroller.
But this project is like a cooperative "RTOS" focusing on a tiny (or better : a Pico) tasks scheduling for ALL microcontrollers.
You need to configure just one timer (e.g. 1 millisecond, is a good choice) to get a Pico tasks scheduler ready.
Your only limit is the microcontroller memory.
This kernel can create a task with a period, stop, resume and change a period of a task at any time. This kernel can delete all task at any time to create another sequencer as you want.
A TickGet function is supplied by the kernel to manage all timer as you want.
This project was compiled with gcc in Linux, and it's just an example to create your own project in microcontroller. To compile this project, open a terminal and enter in the project directory. At prompt, tape make and after the compilation, tape ./prog. To stop the programme tape CTRL+C.
For use this source code in microcontroller you have to create just one timer interrupt function and replace the function void Timer(void) to get your Pico-kernel for your own application. Of course you can delete my task example en delete printf in this code for use in microcontroller.
To resume this kernel is based on a circular linked list, to switch task on task. It is willingly written in a general way to help people to customise for theirs owns applications. There are no priority between task like a round-robin task scheduling. I make another version of this kernel sort of priorities but I don't know if it's a good choice. To resume this other version, the first task add in the scheduler was the highest level of priority, and the last task add in the scheduler was the lowest priority.

Enjoyed yourself, it's free and it was on BSD licence.




Sébastien PALLATIN