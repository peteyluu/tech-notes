## Docker

* Docker is a platform that use OS-level virtualization to deliver software in packages called containers
* Containers are isolated from one another and bundled their own software, libraries and configuration files, libraries and configuration files; they can communicate with each other through well-defined channels
* All containers are run by a single OS kernel and therefore use fewer resources than virtual machines
* A container can run on any Linux server; provide flexibility and portability; enabling the application to be run in various locations
* Docker containers are lightweight, a single server can run several containers simultaneously


**Components**

* **Software**
  * The Docker daemon, called `dockerd`, is a persistent process that manages Docker containers and handles container objects. The daemon listens for requests sent via the Docker Engine API
  * The Docker client, called `docker`, provides a CLI that allows users to interact with Docker daemons

* **Objects**
  * A __container__ is a standardized, encapsulated environment that runs applications. A container is managed using the Docker API or CLI
  * A __image__ is a read-only template used to build containers. Images are used to store and ship applications
  * A __service__ allows containers to be scaled across multiple Docker daemons. The result is known as a _swarm_, a set of cooperating daemons that communicate through the Docker API

* **Registries**
  * A repository for Docker images
  * Clients connect to registry to download ("pull") images or upload ("push") images
  * Two main public registries are Docker Hub and Docker Cloud
  * Docker Hub is the default registry


**Tools**

* __Docker Compose__ defines and runs multi-container applications
* Uses YAML files to configure the app's services and performs the creation and start-up process of all the containers with a single command
* `docker-compose` CLI allows users to run commands on multiple containers at once, for example, building images, scaling containers, running containers that were stopped, and more
* __docker-compose.yml__ file is used to define an app's services and includes various configuration options
  * `build` option defines configuration options such as the Dockerfile path
  * `command` option allows one to override default Docker commands, and more
* __Docker Swarm__ provides native clustering functionality for containers, which turns a group of Docker engines into a single virtual Docker engine
