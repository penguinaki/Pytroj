# Pytroj

__Pytroj is a proof of concept attack against .pyc files.__ It searches for other .pyc files and injects itself into them. The injected code can be any python code (in this case it prints "You have been exploited").

This proof of concept only searches for .pyc files in its own directory. To use it:

     python -c 'import exploit, b, c'
     python exploit.pyc

The files b.pyc and c.pyc will now be infected. If you create another .pyc file (for example, python -c 'import byteplay') and run either b.pyc or c.pyc, the new file will also get infected.

Another way to run an infected file is to import it once the .pyc file exists:

     python -c 'import b'

The infected files print out a list of files that they have newly infected, followed by the phrase "You have been exploited"

After that, infected programs will continue to execute as normal.

For help, questions, or comments, feel free to contact us:

[Joey Geralnik](https://github.com/jgeralnik "jgeralnik")

[Leon Fedotov](https://github.com/LeonFedotov "im0b")

[Itzik Kotler](https://github.com/ikotler "itzikkotler")

++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

Information below refers to this fork only. 

__Pytroj is extended to infect running processes in memory.
All the information above still holds true.

To infect a running process use:

     python -c 'import exploit, process-name'
     
The running process will now be infected.

For more info, contact me at: https://github.com/penguinaki


