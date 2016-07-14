# About the TCP Congestion Control & the Algorithm
TCP Congestion Control is a one of the huge feature in TCP network area, and network module in system kernel. Since talking about the TCP congestion contol is too much for a day, I'll only write about the TCP Congestion Control Algorithm.

# What is the TCP Congestion Control Algorithm
To be simple, TCP Congestion Control Algorithm is a algorithm which determines how much to send a TCP payload to the receiver, without making a loss as much as possible. Since loss is the main reason how TCP gets it's delay, TCC Algorithm is the one of the important feature in TCP network module.

# Some well-know Algorithms
* Reno (New Reno)
	* VEGAS
	* HighSpeed
	* BIC
	* CUBIC
	* H-TCP
	* Compound TCP
	* Westwood
	* ECN
	* and much more!


# Why are there so many Algorithms?
	Yesh! As you can see the list above, there are so many algorithms, and various Operating Systems (OS) select different algorithms ans use as their default algorithm.
	Each algorithm has it's benifit. Some are good for Large bandwidth enviroment, some are good with the delay enviroment. One of the way to make your internet faster is to select  and apply the right algorithm for your internet enviroment.



# Reference
	* [https://en.wikipedia.org/wiki/TCP_congestion_control#Algorithms](https://en.wikipedia.org/wiki/TCP_congestion_control#Algorithms)
