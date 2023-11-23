## Installation Instructions

Follow these steps to install and use the modified FEniCS 2019 image using Docker.

#### Step 1: Download the Modified FEniCS Container Image

##### For Windows OS:

You can download the image from the link below:
```
https://1drv.ms/u/s!Av-ZsDIYrM3Yj9VfElhWKORF8zH-ZA?e=iqE3H8
```
##### For Ubuntu OS:

You can download the image through terminal (ctrl + alt + t) by entering the command below:
```
wget -O FEniCS2019FeVAcS231011.tar "https://1drv.ms/u/s!Av-ZsDIYrM3Yj9VfElhWKORF8zH-ZA?e=iqE3H8"
```
This image will allow you to run FEniCS2019 with gmsh, meshio and other necessary libraries for FeVAcS v2.0.0 algorithms on Jupyter Notebooks.

#### Step 2: Load the Image

##### a) For Window OS:
Open PowerShell with administrator rights and enter the command below.

```
docker load -i FEniCS2019FeVAcS231011.tar
```

##### b) For Ubuntu OS:
Open terminal (ctrl + alt + t) and enter the command below.

```
docker load -i FEniCS2019FeVAcS231011.tar
```

#### Step 3: Install the Image

##### a) For Windows OS:
```
docker run --name FeVAcS_v200 \
-w /home/fenics \
-v "$(pwd)":/fenics:/home/fenics/shared \
-d -p 127.0.0.1:8888:8888 \
meteoguc/fevacs/v200 \
'jupyter-notebook --ip=0.0.0.0'
```

##### b) For Ubuntu OS:
```
docker run --name FeVAcS_v200 \
-w /home/fenics \
-v "$(pwd)":/home/fenics/shared \
-d -p 127.0.0.1:8888:8888 \
meteoguc/fevacs/v200 \
'bash -c "chmod -R 777 /home/fenics && jupyter-notebook --ip=0.0.0.0"'
```