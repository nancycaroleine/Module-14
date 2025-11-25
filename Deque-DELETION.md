# Exp.No:38  
## Deque - DELETION

---

### AIM  
To write a Python program to delete elements at FRONT END of deque using a collection built-in function.

---

### ALGORITHM  

1. Import the `deque` class from the `collections` module.  
2. Create an empty deque.  
3. Define how many elements to input (e.g., 3 inputs as in the example).  
4. Loop through the range of input size:  
   - Read an integer from the user.  
   - Append the integer to the deque.  
5. Remove the front element of the deque using `popleft()`.  
6. Print the final deque after deletion.  

---

### PROGRAM  
```
import collections

n1 = input()
n2 = input()
n3 = input()

de = collections.deque([n1, n2, n3])

de.popleft()


print("The deque after deletion is :")
print(de)
```
### OUTPUT

<img width="725" height="237" alt="image" src="https://github.com/user-attachments/assets/8d0b8eb3-c41d-4024-a792-23d041d23afa" />

### RESULT

Thus, the python code is written and executed successfully.
