**BARRIERR.PY**

There are three threads (representing the runners: Huey, Dewey, and Louie).
Each runner (thread) sleeps for a random 2–4 seconds to simulate running time.
After sleeping, each runner prints a message showing the time they reached the finish line (the barrier).
The Barrier makes all threads wait until all three runners reach the same point.
Only when all have arrived, they can proceed.
Finally, the main thread prints “Race over!” after all runners have finished.

**CONDITION.PY**
one Producer thread that adds items to a shared list
one Consumer thread that removes items
The threads use .wait() and .notify() to ensure that:
The producer stops producing when the buffer (list) is full
The consumer waits when the buffer is empty
Thus, they work together smoothly without data corruption or race conditions.



**EVENT.PY**
There are teo things in this code consumer ,producer
The consumer thread:
Sleeps 2 seconds each time.
Waits until the event flag is set by the producer (event.wait()).
When event is set, it pops (removes) the last item from items.
The producer thread
The producer:
Runs 5 times.
Sleeps 2 seconds each time.
Creates a random number (0–100) and appends it to the list.
Logs the action.
Sets the event (event.set()) — signals that consumer can consume.

Clears it (event.clear()) — resets event for next cycle.

**MYTHREADLOCK.PY**
It creates nine threads, each running for a random duration. A lock ensures that only one thread runs its critical section (printing and sleeping) at a time — preventing output overlap or data conflicts. After all threads finish, the program prints "End" and the total execution time
Then it logs that it consumed the item.
multithreading and the use of a Lock to control access among threads.

**MYTHREADLOCK2.PY**
This program demonstrates multithreading with partial use of Lock.
It creates 9 threads, each printing its name and process ID, then sleeping for a random time (1–10 seconds).
However — unlike the previous version — the Lock is released before the sleep(), allowing multiple threads to run their “sleep” part simultaneously.
the both code are sae but the execution time is differrent because of lock acquires.

**RLOCK.PY**
Two threads run concurrently:
One adds items (adder)
One removes items (remover)
RLock prevents race conditions, so total_items always updates correctly.
Each thread sleeps 1 second after adding/removing, simulating a time-consuming process.
The final number of items = initial items + items added − items removed.

**SEMAPHORES.PY**
Implements Producer-Consumer problem using semaphore.
Consumer waits for item until producer signals via semaphore.
Producer produces item after 3 seconds and signals consumer.
Uses threads for concurrency and logging for clear output.
Semaphore ensures synchronization, preventing the consumer from consuming before the item is ready.

**THREAD NAME AND PROCESS**
Thread#1 starts and prints its message.
Thread#2 starts and prints its message.
Threads run concurrently, so the order is non-deterministic.
The main program waits until both threads finish.
Finally, End is printed.




4️⃣ Producer Class
