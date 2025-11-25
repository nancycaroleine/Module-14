# Exp.No:40  
## APPLICATIONS OF QUEUE

---

### AIM  
To write a Python program to implement CPU Process Scheduling using a queue.

---

### ALGORITHM  

1. Start the program.  
2. Define the function `CalculateWaitingTime(at, bt, N)`.  
3. Initialize a list `wt` of size `N` with all values set to 0.  
4. Set `wt[0] = 0` for the first process.  
5. Print the table header: "P.No.", "Arrival Time", "Burst Time", "Waiting Time".  
6. Print the values for the first process.  
7. For each process from index `1` to `N-1`:  
   - Calculate `wt[i] = (at[i - 1] + bt[i - 1] + wt[i - 1]) - at[i]`.  
   - Print the process number, arrival time, burst time, and waiting time.  
8. Initialize `total_waiting_time = 0`.  
9. Add up all waiting times.  
10. Calculate average waiting time as `average = total_waiting_time / N`.  
11. Print the average waiting time.  
12. Get burst times as input from the user for 5 processes.  
13. Call `CalculateWaitingTime()` with `at`, `bt`, and `N`.  
14. End the program.

---

### PROGRAM  
```
# Python3 program to Calculate Waiting
# Time for given Processes

# Function to Calculate waiting time
# and average waiting time
def CalculateWaitingTime(at, bt, N):

	# Declare the array for waiting
	# time
	wt = [0]*N;

	# Waiting time for first process
	# is 0
	wt[0] = 0;

	# Print waiting time process 1
	print("P.No.\tArrival Time\t" , "Burst Time\tWaiting Time");
	print("1" , "\t\t" , at[0] , "\t\t" , bt[0] , "\t\t" , wt[0]);

	# Calculating waiting time for
	# each process from the given
	# formula
	
	#------ CODE HERE ------
	# each process
	for i in range(1,5):
	    wt[i]=(at[i-1]+bt[i-1]+wt[i-1])-at[i];
	    print(i+1 , "\t\t" , at[i] , "\t\t" , bt[i] , "\t\t" , wt[i]);
		
	#------ CODE HERE ------
	#------ CODE HERE ------
	

	# Declare variable to calculate
	# average
	average = 0.0;
	sum = 0;

	# Loop to calculate sum of all
	# waiting time

	#------ CODE HERE ------
	for i in range(5):
	    sum +=wt[i]
	    average = sum/5
	print("Average waiting time = ", average)    
	
	#------ CODE HERE ------
	

# Driver code

	# Number of process
N = 5;

	# Array for Arrival time
at = [ 0, 1, 2, 3, 4 ];

	# Array for Burst Time
bt=[]
for i in range(0, 5):
    ele = int(input())
    bt.append(ele)
	

	# Function call to find
	# waiting time
CalculateWaitingTime(at, bt, N);
```
### OUTPUT

<img width="761" height="346" alt="image" src="https://github.com/user-attachments/assets/59bade90-345c-4da8-8cd0-f055a5119f00" />

### RESULT

Thus, the python code is written and executed successfully.
