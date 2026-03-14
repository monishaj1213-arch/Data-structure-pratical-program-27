from collections import deque

class Queue:
    def __init__(self):
        self.queue = deque()

    def enqueue(self, item):
        self.queue.append(item)

    def dequeue(self):
        if self.is_empty():
            return None
        return self.queue.popleft()

    def peek(self):
        if self.is_empty():
            return None
        return self.queue[0]

    def is_empty(self):
        return len(self.queue) == 0

# Example usage
q = Queue()
q.enqueue(10)
q.enqueue(20)
print(q.dequeue())  # Output: 10
print(q.peek())  # Output: 20# Data-structure-pratical-program-27
