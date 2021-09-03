# multi-docker

This is an overcomplicated multi-container Fibonacci calculator used to demonstrate software engineering frameworks and technologies.

The user enters in an index and the application will display the n-th term Fibonacci value.

Ie. Entering Fibonacci of 4 will yield 3.

[For further reading](https://en.wikipedia.org/wiki/Fibonacci_number)

## Features
- The calculator has a basic frontend made using React, backend using Node + Express and runs on an Nginx server.
- The application will calculate the expected Fibonacci value and store them in a Postgres database.
- In addition, Redis is used to log all indexes that are inputted into the calculator.
- When a new index appears, the worker will calculate the respective Fibonacci value. This way, the same Fibonacci computations are not repeated.
- Postgres is deployed with persistent volume, so that in the event that something happens to the Postgres container/pod, the data stored will not be deleted upon the container restart.

