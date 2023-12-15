***

# How To Launch RocHPL Docker Application

***

 **1. Login to https://aac.amd.com/.**
    
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/d62dc96e-e37a-42b3-9b0e-72445014a621)


 **2. Click on Applications. Select HPL.**
    
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/c38b250f-24bd-4a15-8f65-2cca6aeb5bc9)
    
 **3. Select the desired RocHPL version with desired container type as docker/singularity.**
    
   **Note**: In this case, we have selected RocHPL_5_0_5_49 version and container as docker.
    
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/060103a0-9be8-4569-9b2c-c60fae091fb5)
    
 **4. Click on 'New Workload' button available on the top right corner.**
    
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/ace07a67-c914-41a7-b69e-b7aa83eee7a8)

 **5. Click Next button to continue.**

   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/9614e3fe-88b7-4914-9c08-595a775b9884)

 **6. Click Next to continue with default script.**

   **Note: Default script is for 8 GPUs**

   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/5f151625-c7f8-4403-8626-adc4a87783ef)

 **7. Select the allowed run time. The number of GPUs should be 8. Here, we have selected the run time as 1 hour, number of GPU’s as 8 and telemetry is enabled.
    Click on Next button.**

   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/c0b45582-c5ac-4b8f-88b9-ab234afba7af)
   
&emsp; The time for which workload is allowed to run should be specified in the **Maximum allowed runtime** field. By default 1 hour will be selected.

&emsp; If maximum allowed run time is 1 hour, it implies, workload will run for 1 hour and then it will be automatically stopped after 1 hour as it will not be allowed to exceed **Maximum allowed runtime**.

&emsp; Based on the time required for workload, user should change the **Maximum allowed runtime**.

&emsp; Once the workload is launched, user cannot change the total workload time. It has to be configured in this step.

 **8. Select the cluster and desired queue to run the job. In this case 1CN96C8G1H_4IB_MI250_Ubuntu22 was selected. Click on Next.**

   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/7bd91819-4031-4edb-a987-03ddfce4e7fe)


 **9. Review all the configurations selected and click on Run Workload.**
 
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/84f3eb1c-dcd1-4b02-9495-c18b36e7dcc2)
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/61295ad1-eb33-471d-884e-22b43d11c8ff)
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/0f9484e1-239f-4d2c-b037-5b43704d9c02)
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/fa0bd624-d914-4463-b594-6f8270fbef05)
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/1ca97119-fa09-4a4a-a7fb-9e3cbc114ae0)

 **10. Once the application execution is successful then the status gets changed into “Completed”.
     The user can check the STDOUT and STDERR logs by clicking on respective tabs.
     The Performace tab shows the telemetry collected.**
     
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/0beb8d01-4461-4d51-83a3-bf3dfc727bc0)

 **11. The final score in the STDOUT tab is the performance of RocHPL application.**

   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/dab96a0c-4e9f-41b0-bd52-6562089f8068)
