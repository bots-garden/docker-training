
Docker is a tool that allows you to run your applications inside containers, which are isolated and lightweight environments that have everything your app needs to run. Docker makes it easy to develop, ship, and run your app across different platforms and environments. You can use Docker to create, share, and manage your containers, and to scale up or down your app as needed. Docker is based on open source technology and has many benefits for developers and operators.

Docker and a virtual machine are both tools that help you run your applications in isolated environments, but they have some key differences. Here are some of them:

- Docker is a container-based model, which means it uses software packages called containers to run applications on any operating system. A virtual machine is not a container-based model, which means it uses a software layer called a hypervisor to run an entire operating system on a physical machine.
- Docker containers share the host operating system kernel, which is the core component of the OS that manages the hardware and software resources. Virtual machines do not share the host kernel, but have their own guest operating system for each instance.
- Docker containers are more lightweight and less resource-intensive than virtual machines, because they do not need to load the entire OS to start. Docker containers can also start up faster and result in better performance. Virtual machines are more heavy and consume more resources, because they need to load the whole OS and the hypervisor. Virtual machines also take longer to boot up and result in lower performance.
- Docker containers are more portable and easier to deploy than virtual machines, because they contain everything the application needs to run. You can create an application and store it into a container image, which you can then move and run anywhere. Virtual machines are less portable and harder to deploy, because they depend on the underlying hardware and software configuration of the host machine.


## Ops perspective

When you install Docker, you get two major components: 

- The Docker client 
- The Docker engine (sometimes called the “Docker daemon”) 

The engine implements the runtime, API and everything else required to run containers.

```bash
# images
docker images
docker pull ubuntu:latest

# containers
# launch a container from the downloade image
# The -it flags tell Docker to make the container interactive and to attach the current shell to the container’s terminal

docker run -it ubuntu:latest /bin/bash
ps -elf

```

### Attaching to running containers 

You can attach your shell to the terminal of a running container with the `docker exec` command. 

```bash
docker exec -it vigilant_borg bash
```

