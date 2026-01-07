tasklist: Displays a list of running processes.

tasklist /FI "imagename eq [process_name]": Filters the tasklist for a specific process (e.g., notepad.exe).

taskkill /PID [pid]: Terminates a process by its process ID (PID).

example:

What command would you use to find the running processes related to notepad.exe?

Answer: tasklist /FI “imagename eq notepad.exe”

What command can you use to kill the process with PID 1516?

Answer: taskkill /PID 1516
