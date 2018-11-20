# Lab_01 - Hello World in QNX Executable project
Setup Momentics IDE + Neutrino SDP to setup a simple project and print out "Hello World"

================================================================================
# Lab_02_PartA - Understanding Signal Processing with Signal-Handlers
## Fully functional within the scope of the Lab_02 Part A
The program meets all the requirements and status of Lab_02_PartA. The program does behave as expected. However, if SIGUSR2 is sent as a signal, the program will terminate (regardless of the fact that there is no SIGUSR2-handler) because SIGUSR2 is also a termination signal by default and no message is displayed when SIGUSR2 is received (because this was not a requirement). Since there is only one process, there’s no worry for Zombie processes. The intention and preamble of the program is also written in the header of the source file.
## Known Issues
So far, the program runs smoothly and as intended. I have tested it in the scope of the lab. I haven’t tested it with random variable or addresses (if you just use a pointer without initializing it, eg: int *x; at that point ‘x’ would be pointing to “garbage-addresses/values”). Everything seems to be working on my end. Hopefully it goes well! 😊

================================================================================
# Lab_02_PartB - Demonstrating knowledge of Parent and Children process(es).
## Fully functional within the scope of Lab_02_PartB
The program meets all the requirements and status of Lab_02_PartA. The program does behave as expected. However, if you decide to kill the parent process while the child(ren) process(es) are active, you would make Zombie processes and the Neutrino will cripple and you will not be able to run any more program on/through it. You would have to restart Neutrino to fix that issue and to continue running other QNX projects through Neutrino.
## Known Issues 
There is no runtime error. If the value entered for number of children is equal to or below zero (numChildren <=0), then the program has no child process and treats it as such and will exit the parent process and terminates the program. The intention and preamble of the program is also written in the header of the source file.

================================================================================
# Lab_03 - Threads in Semaphores
## Fully functional within the scope of the Lab_03
The program meets all the requirements and status of Lab_03.
The program does behave as expected. 
## Known Issues
So far, the program runs smoothly and as intended. I have tested it in the scope of the lab.
However, if from all the threads are already unblocked and more sem_post is sent, it still tries to unblock the threads (which are already unblocked).

================================================================================
# Lab_04 – Inter-Process Communications
## Fully functional within the scope of the Lab_04
The program meets all the requirements and status of Lab_04.
The program does behave as expected. I have limit the decimal places to 2-decimal places for readability purposes.
## Known Issues
So far, the program runs smoothly and as intended. I have tested it in the scope of the lab.
I have also tested it with many decimal places. The program recognises that x/0 is an error. However 0/0=0 and it prints accordingly.
However, if one writes the command-line argument without spaces (example: 6+9), it would throw an error because the program reads that as one input/argument. 

================================================================================
# Lab_05 – Pulses
## Partially functional within the scope of the Lab_04
The function takes in the status but does not display it correctly.
It does however display the integer properly. I assume its can be fixed but I am running out of time.
## Known Issues
The status displays "status" for every status.

================================================================================
# Assignment1 – The Hacker Security Guard
## Fully functional within the scope of the Assignment1
The program meets all the requirements and status of Assignment1.
The program does behave as expected. This was assignment was quite fun. The more difficult part was knowing where and how things were communicating rather than the actual coding of the program.
## Known Issues
So far, the program runs smoothly and as intended. I have tested it in the scope of the lab.
However, it does not have a structure for the Person because the person's attributes were not used to calculate or process anything.

================================================================================
# Skill-Based-Assessment1 – The Electronic Puncher
## Author
Niladri Sengupta (Neal)
## 90-95%  functional within the scope of the SBA
The program does behave as expected. This was assignment was interesting and similar to assignment 1. Knowing where to place the sleep() function was tricky. 
## Known Issues
So far, the program runs smoothly and as intended. I have tested it in the scope of the lab.
However, for test1.txt it doesn’t stop the program because it’s still in sleep but since the sleep function is implemented in the display, the controller and input are still functional. Some print statements do not work in “real-time”. They have this weird behavior where they only print when they are out of the loop and a second print statement is in process – then they both print. I am guessing that’s because of the sleep() function being implemented in the display. I think I should have implemented everything (including the sleep() function in the controller instead of the display) separately instead of trying to modularize the code – which would make the code much longer but it would at least complete what is required of it.
