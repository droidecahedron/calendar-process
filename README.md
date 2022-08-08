# calendar
basic c program for scheduling given a text input of a schedule to create/reschedule/delete events with datetimes, locations, and descriptions.

usage : 
./location_updater < input.txt


Since we are using mmap and processes, no longer employ the
circular buffer for IPC, and the mmap with mutex/condition variables would now be the method of IPC.
Thus, each process accesses a shared mmap data region (one reads, one writes).

The condition and mutexes, however, are set up with mmap as we are no longer using pthreads, but processes.
