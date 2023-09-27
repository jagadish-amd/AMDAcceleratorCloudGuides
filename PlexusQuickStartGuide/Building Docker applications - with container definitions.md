***

# Building Docker applications - with container definitions

***
This article describes how to create docker applications in AAC. To accomplish this procedure, you will need AAC Developer or Admin permissions.

**1.** Click on the top bar menu option **Applications**, and then click on **Applications** again.
![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475255/31842912-bb5f-43a5-b90a-26d4aa62fb8a)

**2.** Click on **New Application** button  
If you do not see the **+ New Application** button, you do not have Developer or Admin permissions.

**3.** Select **Docker** on the **Container type** screen. Click on the **NEXT** button.
![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475255/c63ff198-6f0e-4403-b5c2-3c5d5ed5053a)

**4.** Configure the general application attributes
In the general information panel, configure the general application attributes, see next image below.

**Name (required)**: Name of the application.  
**Description**: Description of the application.  
**Family**: The Application Family of this application.  
**Version number**: Version of the application.  
**Allow replicas**: Toggles replicas on / off. Kubernetes container feature.  
**Categories**: Assign a category to the application.  
**Architectures (required)**: Either x86_64 or arm64.  
**Accelerator**: either AMD GPU, NVIDIA GPU or Google TPU.  
**Is service**: Indicates that the application will be executed as a docker interactive.  
**Is stateful set**: Toggles statefulset on / off. Kubernetes container feature.  
**Ports**: Services can configure the application port to be exposed to users. Several ports can be configured by clicking in Add Port button.  
Example for Jupyterlab with SSH connection: ui: 8888, ssh: 22  
**Intel MPI**: Toggles Intel MPI on / off  
**Featured**: Toggles Featured on / off. When on, includes this application at the top of the Applications list in the Featured section.  
**Price per use**: Price charged to the user for using the app.  
**Price per hour usage**: Price charged to the user per hour of usage.  
**Price per core usage**: Price charged to the user per core usage.  
**Price per GPU usage**: Price charged to the user per GPU usage.  
**Stateful Sets**  Stateful sets are useful when you need to keep a predictable hostname list for multi-POD jobs, as in the following example:  

some_hostname_prefix_0 is the hostname of the 1st replica.  
some_hostname_prefix_1 is the hostname of the 2nd replica.  
some_hostname_prefix_2 is the hostname of the 3rd replica.

With stateful sets, the same hostname is kept between a POD failure / restart. This is useful for MPI jobs, or jobs where you need PODs to register to a centralized server e.g. Spark and NiFi. Since the hostnames follow a predictable pattern, you always keep the same fixed host list for your job, even after a POD failure / restart.  

**Repository authentication**  
In the case your application uses containers that are stored in a private image repository, you will need to setup the following authentication fields:

**User**: user of the docker image repository account.  
**Password**: the password of the docker image repository account. It can be also the security token provided by some repositories such as NVidia.  
**Server**: the docker repository server URL. This is the URL for Docker hub: https://index.docker.io/v1/
![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475255/43b19695-668e-4cc9-929f-5e957fa2ef23)

**5.** After filling in the application attributes, click on the NEXT button  
**6.** Configure the application settings  
In the settings panels, we can configure the application settings.

The most common settings to configure are:

**Help URI**: this contains a URL within help articles about the how to run the application.  
**Workload default prerun script**: this defines the default script to execute before the container scripts are executed. It can also be defined during the job submission process.  
**Workload default postrun script**: this defines the default script to execute after the container scripts are executed. It can also be defined during the job submission process.


After the application settings are configured, click NEXT.
![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475255/96d03916-7c53-4cb7-a004-1eed0812c70f)

**7.** Add container
Click the ellipses(...) button and then click **Add new container** on the dropdown menu.
![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475255/257c0def-79d8-4cd4-af8a-7674d28ecb9e)

Fill in the **CONTAINER INFORMATION** parameters:

**Name (required)**: Container name.  
**URL**: container URL  
**Architectures required)**: Select either x86_64, or aarch64.  
**Version**: container version
**GPU**: check this box if the container requires GPU resources.  
**Description**: Your description of the application container.  


Click **SAVE** to save the container.
![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475255/66eda6f2-8935-4c5f-9dad-8023cff88211)

**8.** Configure container  
Click on select container and then click on the container you just created, then click on the **Add application container** button.
![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475255/52eec0f7-48f3-48ef-ba4b-7f13b25134c1)

Set the following parameters to configure the application:

**Name**: Name to be used for this container when used inside this application. Within a given application each container name must be unique. You may use the same container multiple times within a given application -- but each use must have a different name (example: redis-server-1; redis-server-2 might be the names used within the application for multiple instances of the original redis-server container).  

**Order**: Order of execution of the container inside the application. Format integer (e.g. 1, 2, 3 etc.).  

**Number of CPUS**: Number of CPUS required by the container execution. Format integer. If you set number of cpus = 0, it will run without limits or under cluster default limits.  

**Memory**: Number of megabytes required by the container execution. Format integer. If you set memory = 0, it will run without limits or under cluster default limits.  

**Number of gpus**: Number of gpus required by the container execution. If the container requires the use of a gpu, and you do not setup any value, the AAC will use 1 gpu by default. Format integer.  




