# -OS-MLFQ-scheduler

A multi-level feedback queue (MLFQ) scheduler in xv6.
1. Four priority levels, numbered from 0 (highest) down to 3 (lowest).
2. The highest priority ready process is scheduled to run whenever
   the previously running process exits, sleeps, or otherwise yields the CPU.
3. When a new process arrives, it should start at priority 0.
4. The time-slice associated with priority 0 is 5 timer ticks; for priority 1 it is also 5 timer ticks; 
   for priority 2 it is 10 timer ticks, and for priority 3 it is 20 timer ticks.
5. After each 1 second interval, if a runnable process has not been scheduled at all in that interval, 
   its priority should be bumped up by one level and given a new time-slice. 
   Note that this 1 second interval is system-wide; at this same point in time, every runnable process is evaluated for starvation.


