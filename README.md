# A bit of information for the Inception

## Docker:

Docker is a software platform that allows you to build, test, and deploy applications quickly. It packages 
software into standardized units that are called containers and that have everything the software needs to 
run including libraries, system tools, code and runtime. Using Docker, you can quickly deploy and scale 
applications into any environment and know your code will run.

## Why to use Docker?

1. Applications are running in an isolated environment,
2. It is way more easy to run applications on different servers,
3. Аll application dependencies are installed inside the container,
4. Еasy to scale by increasing the number of the containers,
5. Very convenient to use during the application making process.

## So what is the difference between Docker and VM(Virtual Machine)?

| Virtual Machine | Docker |
| --- | --- |
| Occupy a lot of memory space | Occupy a lot less memory space |
| Long time to boot up | Quick boot up cause it uses the running kernel that you use |
| Difficult to scale up | Super easy to scale |
| Low efficiency | High efficiency |
| Volumes storage cannot be shared across the VM’s  | Volumes storage can be shared across the host and the containers |

## Docker components:

                            Docker components
                            /       |       \
                         client   dameon   host

                           container   image

                          repository   registry


**Container -** is the smallest element in the "Docker world". The applications are running in the container.
One application - one container. Containers are dynamic.

**Image -** is the base for creating containers. You can create different containers but with one base.
Images are static.

**Repository -** is a place where different versions of the images are.

**Registry -** is a place where different repositories are. It can be both local and remote.
The most known remote registry is Dockerhub. 


## The image structure:

                            The image structure
                               (layer set)
                                    |
                                  Image
                                    |
                                Layer 3
                                Layer 2
                                Layer 1
                             The basic layer

All layers are **read-only**. They are just a collection of files.
You can move/delete images. The images are kept in repositories.
There can be multiple versions of the image, but usually the basic layer remains the same.
There are official images in Dockerhub and images of the community.

## The repository structure:

1. Different versions are marked with different tags,
2. One version of an image can have multiple tags,
3. It can be local or in a remote registry of repositories (for example Dockerhub).

## The basic Docker commands:

1. **`docker version`** - shows the information about the client and the Docker server;
2. **`docker ps -a`** = shows the launched and stopped containers;
3. **`docker ps`** - shows the launched containers;
4. **`docker images`** - shows the local images list; 
5. **`docker run [image_name]: tag`** - creates and launches a container with the version that you want;
6. **`docker rm`** - removes the container;
7. **`docker run -it [image_name/container_name/ID]`** - connects to the process in the container (-i: interactive, -t: terminal);
8. **`docker container prune`** - removes all the stopped containers;
9. **`docker run -d [image_name]`** - launched on the background mode;
10. **`docker container inspect [ID/container_name]`** - details about the container;
11. **`docker stop [ID/container_name]`** - stops the container (if it did not work, you can use docker kill)
12. **`docker exec -it [ID/container_name] [process_name]`** - creates a process in the container if it is launched; 
13. **`docker run -d [image_name] --name [container_name]`** - launches the container with the name you want on the background mode;
14. **`docker run -p []:[] []`** = opens access to the server in the container;
15. **`docker run -v ${PWD}:[]`** - 

