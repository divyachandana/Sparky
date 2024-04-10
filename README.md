
# Sparky AI Assistant

Sparky is an AI assistant designed to assist users with various tasks, including reading books, papers, research materials, and providing support with images, graphs, and pictures.

## Getting Started

To get started with Sparky, follow these steps:

### 1. Clone the Repository

Open your terminal and clone the Sparky repository:

```bash
git clone [<repository-url>](https://github.com/divyachandana/Sparky.git)
```

### 2. Navigate to the Sparky Directory
Change directory to the Sparky repository:

```
cd sparky

```

Run with Docker
To simplify setup and usage, Sparky can be run within a Docker container.

### 3.1. Build the Docker Container
Build the Sparky Docker container using the provided Dockerfile:

```
sudo docker build -t sparky .

```
### 3.2. Run the Docker Container
Run the Sparky Docker container with the following command:

This Docker command is running a container named "sparky" with Nvidia GPU support (`--runtime nvidia`), giving access to camera (`--device /dev/video0:/dev/video0`), and audio devices (`--device /dev/snd:/dev/snd`). It's mapping port 8888 on the container to port 8888 on the host (`-p 8888:8888`), and mounting the local directory `/home/dc/Documents` to `/workspace` in the container (`-v /home/dc/Documents:/workspace`). Additionally, it's launching Jupyter Lab without authentication (`--allow-root --NotebookApp.token='' --NotebookApp.password=''`).

```
sudo docker run --runtime nvidia -it --rm \
    --privileged \
    -p 8888:8888 \
    --device /dev/video0:/dev/video0 \
    --device /dev/snd:/dev/snd \
    -v /home/dc/Documents:/workspace \
    sparky \
    jupyter lab --ip=0.0.0.0 --allow-root --NotebookApp.token='' --NotebookApp.password=''

```

This command sets up the container environment with necessary permissions and volume mappings, and launches Jupyter Lab with Sparky's functionality.

### 4. Access Jupyter Lab
Once the container is running, access Jupyter Lab in your web browser by navigating to http://localhost:8888.

### 5. Start Using Sparky
You're now ready to start using Sparky for various tasks! Refer to the documentation for usage instructions and examples.

![sparky](https://github.com/divyachandana/Sparky/assets/5434731/f21fc519-8da8-4df1-8dbd-cc3f97d4b8a2)

https://youtu.be/plg67ASwQAs
https://youtu.be/oaKm5daPFPc



This guide outlines the steps required to set up and run Sparky AI Assistant using Docker, providing clear instructions and explanations for each step. Adjust the paths and commands as necessary based on your specific setup.




