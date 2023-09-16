## FeVACs: FEniCS Visualizing Acoustic Scattering

FeVACs is an open-source finite element software designed to streamline exterior acoustic analyses, particularly for scenarios involving multiple obstacles arranged periodically. It facilitates lattice placement parameters, mesh generation, variational formulation, and the display of contour plots for the results. The software also offers a browser-based solution display, enhancing the ease of sharing and comprehending this complex physical phenomenon.

## Installation
*Note: These instructions are intended for a specific system setup. Advanced users may use alternative methods based on their setup and preferences.*

1. To use this software with a Windows 10 Home operating system, follow these steps:

   Ensure you have the latest version of Docker (https://www.docker.com) installed on your system.

   *As of today, this software runs with Docker v4.22.1 on a computer with Windows 10 Home 22H2 OS. Please note that Windows Home or Education editions will only allow you to run Linux containers.*

3. Install FEniCS within a Docker container using the following command:

   docker run --name [CONTAINER_NAME] -w [WORKING_DIRECTORY] -v [LOCAL_PATH]:[CONTAINER_PATH] -d -p [HOST_PORT]:[CONTAINER_PORT] [IMAGE_NAME] '[JUPYTER_COMMAND]'

   Replace the placeholders with your specific values or paths as needed for your use case.

4. Install the necessary libraries through the Docker terminal:

   sudo apt-get update
   sudo apt-get install libglu1 libxcursor1 libxinerama1
   pip install --no-binary=h5py h5py

5. Clone this repository to your local machine:
   
   This can be done using GitHub Desktop (https://desktop.github.com/)

6. Run the installed container using Docker and access the FeVACs.ipynb Jupyter Notebook.

   *You can modify the input parameters to analyze various geometrical setups and obtain results for your analysis.*
