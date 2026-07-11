# Distributed Remote Code Execution & Evaluation System

A distributed system that safely executes and evaluates code submissions from
multiple users concurrently. Built using a queue–worker architecture to handle
submissions asynchronously, with Docker-based sandboxing for safe execution of
untrusted code.

## Status
Ongoing — final-year project (Team of 4)

## My Role
System design contribution and coordination across modules (Docker sandboxing,
task queue, and fault-tolerance components).

## Tech Stack
- Docker
- Message Queue (Queue–Worker Architecture)
- Worker Processes

## Key Features
- Asynchronous task processing via a queue-worker model
- Isolated Docker containers with CPU, memory, and time limits per submission
- Fault-tolerant task handling with automatic retry on failure
- Horizontally scalable across multiple concurrent workers

## How It Works
1. User submits code → stored as a task in a message queue
2. Worker processes pick up tasks and execute them in isolated Docker containers
3. Output is compared against expected test cases to determine correctness
4. Runtime and memory metrics are captured for each execution
