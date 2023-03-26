# Threads

In Java, threads are a way to execute multiple tasks concurrently within a single program. Threads allow a program to perform multiple tasks at the same time, making it more efficient and responsive.

Threads are implemented using the Thread class in Java. A new thread can be created by either extending the Thread class or implementing the Runnable interface.

Here's an example of using threads in Java:

```

// implementing the Runnable interface
class MyRunnable implements Runnable {
    @Override
    public void run() {
        // code to be executed in the new thread
        for (int i = 0; i < 5; i++) {
            System.out.println("Thread: " + Thread.currentThread().getId() + " Count: " + i);
        }
    }
}

// creating and starting a new thread
MyRunnable myRunnable = new MyRunnable();
Thread thread = new Thread(myRunnable);
thread.start();

// main thread code
for (int i = 0; i < 5; i++) {
    System.out.println("Main Thread Count: " + i);
}
```

In this example, we first create a class MyRunnable that implements the Runnable interface. The class overrides the run() method, which contains the code to be executed in the new thread.

We then create a new instance of the MyRunnable class and pass it as an argument to a new Thread object. We then call the start() method to start the new thread.

Finally, we have the main thread print out a message 5 times. Both the new thread and the main thread will execute concurrently, and the output will be interleaved.

Threads are a powerful feature of Java that allow for concurrent execution of multiple tasks, improving the performance and responsiveness of a program. However, care must be taken when using threads to avoid race conditions and other synchronization issues.