***

# How To Run Workload

***

Login to **https://aac.amd.com/**.
    
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/d62dc96e-e37a-42b3-9b0e-72445014a621)

A workload can be launched by following the below 6 steps.

## 1. Select the desired Application.

The application for which the workload has to be run can be selected in this step. It can be done in two ways as mentioned below.

&emsp; a. Navigate to **Applications** page. Select desired application for which workload has to be run.
   
&emsp; **Note**: In this case, we have selected Application as **HPCG**.
 
&emsp; ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/5d521fdb-046e-4963-9068-db42f71a59c9)

&emsp; c. Select desired version if prompted. It can be either docker or singularity.

&emsp; **Note**: In this case, we have selected rocHPCG 3.1.0_97 version and container as **docker**.

&emsp; <img src="https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/ee067057-d622-4418-a6ac-1faa977f61c0" width="900">

&emsp; d. Click on **New workload** button

&emsp; <img src="https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/39adef02-85a7-47bf-aee6-41fee259cc0d" width="900">


### &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp;**(or)**


&emsp; a. Navigate to **Workloads** Page. Click **New Workload** button

&emsp; <img src="https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/c926eef4-9f2c-4770-867c-90fb7ad8ddbd" width="900">

&emsp; b. Select desired application for which workload has to be run.

&emsp; **Note**: In this case, we have selected Application as **HPCG**.

&emsp; <img src="https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/ae1c9519-6a84-4d90-88bc-057b7dd69924" width="900">

&emsp; c. Select desired version if prompted. It can be either docker or singularity.

&emsp; **Note**: In this case, we have selected rocHPCG 3.1.0_97 version and container as **docker**.

&emsp; <img src="https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/ee067057-d622-4418-a6ac-1faa977f61c0" width="900">

&emsp; d. Click **Next** button.

&emsp; <img src="https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/b5f29f92-4981-42b6-b060-69774211f756" width="900">

## 2. Select Input Files

The files required for the workload can be uploaded in this step.

&emsp; a. Click **Upload files**.

&emsp; <img src="https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/82bb7a15-2a04-4685-a4c6-94eeeba38553" width="900">

&emsp; b. Click **Browse Files**

&emsp; <img src="https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/1eb244df-3cd0-465a-b67e-1633a1387ba7" width="900">

&emsp; c. Maximum of 5 files can be uploaded at one time. 

&emsp; d. Select the required files. Click **Next**.

&emsp; <img src="https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/2b3c9085-2752-4cac-b2ed-6496a21d6ae8" width="900">

## 3. Application Configuration

User can either continue with default script or enter custom commands into the following script fields. 

&emsp; ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/ce2ccd72-1286-458b-a28c-1939d5dd2669)

**Note:** Application configuration step will not be available for applications like pyTorch, tensorflow, Jammy etc.

&emsp; a. **Pre-run Script**

&emsp; &emsp; In this step, commands which are required to be executed before creating containers can be added into **Pre-run Script** field.

&emsp; b. **Run Script**

&emsp; &emsp; In this step, commands which are required to be executed in the container created can be added into **Run Script** field. Benchmarking script for 8 GPUs will be available by default for the selected application in this field. AMD Infinity hub can be referred for more benchmarking commands

&emsp; c. **Post-run Script**

&emsp; &emsp; In this step, commands which are required to be executed after creating containers can be added into **Post-run Script** field.

Click **Next**

## 4. Select Resources

Required inputs for workload like number of GPUs, maximum allowed run time, etc can be entered in this step.

![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/0e444fb9-bc8c-4f72-b271-d5d89d2d180d)

![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/ec881f53-0905-4669-ac67-bacbaf04e4e7)


&emsp; a. **Queue oversubscribe**

&emsp; &emsp; By default **Queue oversubscribe** will be disabled. 

&emsp; &emsp; ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/82bbb3ef-0b9b-4a94-b693-428361f48cc3)

&emsp; &emsp; Enabling **Queue oversubscribe** means GPUs allocated to the workload will be allowed to be shared among other workloads. 

&emsp; b. **Telemetry enabled:**

&emsp; &emsp; By default telemetry is enabled.

&emsp; &emsp; ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/32f4c796-5b4e-4d1f-96a3-a8fa5e1551f7)

&emsp; &emsp; If telemetry is enabled, once workload is completed, performance tab will be shown. If disabled, performance tab will not be shown on opening completed/finished workload.

&emsp; &emsp; ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/bea5e17f-8999-43fa-bd02-a93ce1a2ca6a)

&emsp; c. **Maximum allowed runtime**

&emsp; &emsp; The time for which workload is allowed to run should be specified in the **Maximum allowed runtime** field. By default 1 hour will be selected.

&emsp; &emsp; If maximum allowed run time is 1 hour, it implies, workload will run for 1 hour and then it will be automatically stopped after 1 hour as it will not be allowed to exceed **Maximum allowed runtime**.

&emsp; &emsp; Based on the time required for workload, user should change the **Maximum allowed runtime**.

&emsp; &emsp; Example: Maximum allowed time is changed to 2 hours and 30 min. That means, workload is allowed to run for a maximum duration of 2 hr and 30 min. 

&emsp; &emsp; ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/37e42e06-6f42-48af-b3e2-062cd3f97a1d)

&emsp; &emsp; Once the workload is launched, user cannot change the total workload time. It has to be configured before running.

&emsp; d. **Scheduled**

&emsp; &emsp; Scheduling a job is optional. This step can be skipped if you are trying to run the job immediately.

&emsp; &emsp; **Scheduled** field can be used to schedule the job for desired date and time which can be made reccuring daily or weekly.

&emsp; &emsp; To schedule a job, Click the below toggle button

&emsp; &emsp; ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/5ce78a5a-dc51-4b31-ab8f-ccccaf3a997d)

&emsp; &emsp; The time which the workload has to be triggered, How frequently the workload has to be triggered i.e, how many days per week or on which week days can be defined under **Scheduled** field.

&emsp; &emsp; Example1: 

&emsp; &emsp; Here, workload will be run for every two days at time 15:30. Last day is 9/20/2023 after which workload will not trigger.

&emsp; &emsp; ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/e3d4152f-2007-4fac-86b8-8ed77f7d10fa)

&emsp; &emsp; Example2: 

&emsp; &emsp; Here, workload will trigger every tuesday and wednesday at time 19:15. Workload will not trigger after 9/21/2023.

&emsp; &emsp; ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/4edb9383-20f8-44b1-bca7-8466b9a8c3e2)

&emsp; e. **Container Configuration**

&emsp; &emsp; The number of GPUS required for the workload has to be selected in this step. It should be selected based on the run script provided in the **Application Configuration** page for HPC applications whereas for AI/ML applications, GPUs should be selected as required by the user.

&emsp; &emsp; ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/e64c34ac-c5d2-4894-8b5f-ca4e809be52f)

Click **Next** to proceed.

## 5. Select Compute

Based on the number of GPUs selected in previous step, list of available queues will be displayed. Based on accelerator type and OS, required queue can be selected in this step. 

One of the nodes in the selected queue will be assigned for workload based on availability. If node is occupied, workload goes into pending state. Once the node is available, workload will start running.

**Note**: In this case, **1CN128C8G2H_2IB_MI210_SLES15** is selected.

  ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/6063268b-227c-4a2f-8967-456f69ed1b41)

Click on **Next**

## 6. Review Workload Submission

Review all the configurations which are selected in the previous steps.

Click on **Change** button of any of the sections in order to change the configurations if required.
 
![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/1953602c-4d0f-481d-b42e-5ddfc8ecae39)
![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/854b206a-c5a8-452a-b2cc-16e99dbadb94)
![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/854f7e2e-2c5b-47de-a453-6b2ea7ff3728)
![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/de586d6f-87ad-4e9d-8c4e-b6ebd9a3e49c)
 
Click **RUN WORKLOAD**

The workload will start running once the node is available. Please refer [HowTo_Monitor_Workloads](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/blob/main/PlexusQuickStartGuide/HowTo_Monitor_Workload.md) to understand the workload status.


Once the application execution is successful then the status gets changed to **'Completed'**
    
![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/4f113aa6-f7ba-4c26-b62e-c3c22df8b552)
