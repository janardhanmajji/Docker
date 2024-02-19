
Assume Docker as a lunch box, where we pack all the required things and we can eat the ingredients in the box wherever we are comfortable.

Similarly, Docker is a container for packaging the application code, all the dependencies of the application along with the required software with the required version so that it runs in the same way in every environment (dev, prod, test etc.) in the same way the application runs in our machine.
$$\raggedright$$
$${\color{red}\textsf{\textbf{Why Docker?}}}$$

- **Consistency across environments**: It makes an application run in the same way across all the machines including all the Operating systems.
- **Isolation**: Maintains clear boundary between the dependencies of the app with other apps which helps us easy debugging and more security.
- **Portability**: It can be moved to different environments without any difficulty.
- **Light weight**: It shares the resources of the host which makes it light-weight. 
- **Version Control**: We can easily move to the previous version if something goes wrong similar to Git.
- **Scalability**: They can handle many users by creating multiple copies of the Docker Image
- **Docker Integration**: Ensures that the application is developed, tested and deployed efficiently.

**How Docker works?**

Docker has two main concepts - [[Docker Images]] and [[Docker Containers]]

**Docker Images**

A Docker image is a standalone, lightweight and executable package that includes everything which is needed to run a piece of software.

What does a Docker Image include:

A docker image includes:
- The code
- Run time (like Node js)
- Libraries
- System Tools
- Operating System

**Docker Containers:**

Docker Containers are runnable instances of Docker images. It takes the commands from the Docker image, execute them and make them as runnable instances.

**Docker Volumes:**

Persistent Data Storage mechanism. It allows data to be shared between the Docker container and the host machine (usually a computer, a server or among multiple containers). It is like a storage compartment outside the Docker container.

**Docker Network:** 

It is a communication channel which helps the containers to interact with each other and also to interact with the external world. Allows containers to share information while being isolated.

**Docker Workflow**

It consists 3 parts namely :

- Docker Client
- Docker Host (Docker Daemon)
- Docker Registry (Docker Hub)

**Docker Client:** 

It is the interface with which we interact with Docker. We give instructions via the command line or Graphical interface. The instructions/commands we pass helps the Docker client to Dockerize the image, pull an image etc..

**Docker Host:**

It is the back-ground process which takes the instructions from the Docker client and executes them. It helps in build images, running containers and managing all other Docker related tasks.

**Docker Registry:**

It is a central repository of Docker images. It hosts both public and private registries/packages. The Docker images are stored in the Docker Registry and if we run a container it pulls from Docker hub if it is unavailable locally.

In a single line, we issue all the commands to the Docker client which are executed by the Docker Host which manages the containers and builds the Images. The Images are stored in the Docker registry and can be shared to anyone.

**How to use Docker?**

Download from: https://docs.docker.com/get-docker/

Creating a Docker File:

Docker file is a set of instructions which tells how to build a Docker file. 

Some commands:

- FROM - used to specify the base image to use for new image
- WORKDIR - sets the working directory
- COPY - used to copy files and directories from build context to the docker image
- RUN - executes commands during image build
- EXPOSE - tells the port number
- ENV - sets the environment variables
- VOLUME - creates mount point for externally mounted volumes
- CMD - default command
- ENTRY POINT - default command

CMD can be overridden and ENTRY POINT cannot be overridden.

