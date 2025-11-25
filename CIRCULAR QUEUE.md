# Exp No: 36  
## Circular Queue 
---

### AIM  
To write a Python program with a function to insert float values into a Circular Queue.

---

### ALGORITHM

1. Start  
2. Check if the Circular Queue is full  
   - If `size == max_size`, print `"Queue is full"` and exit the function  
3. If the queue is not full:  
   - Read the element to be inserted  
   - Convert it to float  
   - Insert the element at the `tail` position  
   - Update tail using: `tail = (tail + 1) % max_size` (circular increment)  
   - Increment `size` by 1  
4. End

---

### PROGRAM
```
class Queue:
    def __init__(self, size):  # <-- Fixed here
        self.items = [0] * size
        self.max_size = size
        self.head, self.tail, self.size = 0, 0, 0

    def enqueue(self, item):
        if self.is_list_full():
            print(f'Queue is full')
            return
        self.items[self.tail] = item
        self.tail = (self.tail + 1) % self.max_size
        self.size += 1

    def dequeue(self):
        item = self.items[self.head]
        self.head = (self.head + 1) % self.max_size
        self.size -= 1
        return item

    def is_list_full(self):
        return self.size == self.max_size

    def is_empty(self):
        return self.size == 0


size = int(input())
queue = Queue(size)
str1 = float(input())
str2 = float(input())
str3 = float(input())
queue.enqueue(str1)
queue.enqueue(str2)
queue.enqueue(str3)

print(queue.items)

```
### OUTPUT

<img width="827" height="357" alt="image" src="https://github.com/user-attachments/assets/8a84144d-3d83-4bad-b301-844e1ec78e0f" />

### RESULT

Thus, the python code is written and executed successfully.
