### Processes and Threads
- A process is made of:
	- A binary program
	- Data on which the program will execute
	- Resources required for execution, including files, devices which contains or provides the data required.
- In a classic program design, there is only one execution engine for each process.
- That is, there is only one thread of execution in one process.
- In modern computers, the modern process can consists of multiple execution engines.
- In such a design, a process can contain multiple threads.

### Threads
- A threads is a single execution engine capable of performing a series of instructions in a computer program.
- In a multiple threaded process, each thread needs to maintain its own set of data in order to perform its own series of instructions.
- E.g.
	- A web browser might have one thread display images or text while another thread retrieve data from the network.
	- A word processsor