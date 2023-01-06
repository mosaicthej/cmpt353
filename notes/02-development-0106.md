# Development Environment

use docker

## Software Development

- Development Environment vs Production Environment
- Need for different languages/frameworks
- Need to run networks

## Developing

### Local

#### Create Local Environment

- Install dependencies

#### Advantages

- In control of the environment
- Customize everything
- Low overhead

However, it is very dependent on the local environment, and make it hard to reproduce the environment and debug.

### VM

Simulate multiple computers on a single computer.

#### Advantages

- Total Isolation
- Replicating the production environment

But very slow and heavy, as it is running a full OS.

### Containers

(Docker) Running inside a container is like running inside a VM, but without the overhead of a full VM because containers share the host kernel.

Also in cloud computing, containers are used to run applications without having to install the application on the host machine.

An active community of developers and users make Docker one of the most popular containerization platforms.

#### Key Concepts

- **Dockerfile**: A file that contains a list of commands that the Docker client calls while creating an image
- **Image**: A template for creating a container
- **Container**: A running instance of an image
  think of an image as a class, and a container as an object of that class

#### In-class Exercise

- Create a Dockerfile
- Run the Dockerfile in docker
- explore the container....

### WebAssembly

- A new type of code that can be run in modern web browsers
- Allows you to run code written in languages other than JavaScript on the web (any compiled language that compiles to WebAssembly)

Tendency: To abstract away the environment. Abstraction saves time and energy, to unblock the development and to focus on the core logic and creativity.
