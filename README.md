# Race Condition in Simple Counter

This example demonstrates a race condition in a simple counter class.  When multiple threads call the `increment()` method concurrently, the final count may be lower than expected due to race conditions.

## Bug Description

The `increment()` method is not atomic. Multiple threads accessing and modifying the `count` variable simultaneously can lead to lost updates, resulting in an inaccurate count.

## Solution

The solution uses the `AtomicInteger` class, which provides atomic operations that prevent race conditions.