***

# How To Launch RocHPCG Singularity Application

***

 **1. Login to https://aac.amd.com/.**
    
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/d62dc96e-e37a-42b3-9b0e-72445014a621)


 **2. Click on Applications. Select HPCG.**
 
![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/5d521fdb-046e-4963-9068-db42f71a59c9)

  **3. Select the desired RocHPCG version with desired container type as docker/singularity.**
    
   **Note**: In this case, we have selected rocHPCG 3.1.0_97 version and container as singularity.

   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/8287ac20-f394-43e9-87a8-beeb5fa14437)


**4. Click on 'New Workload' button available on the top right corner.**
    
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/c40fea48-800a-469b-afe4-6903998a22b9)


 **5. Click Next button to continue.**

![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/e420e08e-5b7b-4a48-819d-fea3d1f8dc7b)
   

 **6. Click Next to continue with default script.**
 
 **Note: Default script is for 8 GPUs** 
```
mpirun --mca pml ucx -np 8 hpcg 280 280 280 1860
```
  ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/5c8efebf-667b-491c-acce-bdf26cd56df4)


 **7. Select the allowed run time. The number of GPUs should be 8. Here, we have selected the run time as 1 hour, number of GPU’s as 8 and telemetry is enabled.
    Click on Next button.**
        
   **Note:** The time for which workload is allowed to run should be specified in the Maximum allowed runtime field. By default 1 hour will be selected.

    If maximum allowed run time is 1 hour, it implies, workload will run for 1 hour and then it will be automatically stopped after 1 hour as it will not be allowed to exceed Maximum allowed runtime.

    Based on the time required for workload, user should change the Maximum allowed runtime. Once workload is launched, user cannot change the total workload time. It has to be configured in the current step.

![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/edcfdb15-1925-4c44-a7a2-cd8280be1fd4)


 **8. Select the cluster and desired queue to run the job. In this case 1CN96C8G1H_4IB_MI250_Ubuntu22 was selected. Click on Next.**

 ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/81453264-cd3b-4db7-9fda-94bdd6a9fa01)
   

 **9. Review all the configurations selected and click on Run Workload.**
 
![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/663ae8f0-0286-4bc3-bfce-6ba464bd0547)
![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/71914540-ac30-4c86-8350-9485a656f0bb)
![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/9772f3da-a8ce-4021-bc22-af771f89e822)
![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/2d69c98f-3b6e-4ecf-9d24-57d081ba3ffd)



 **10. Once the application execution is successful then the status gets changed into “Completed”.
     The user can check the STDOUT and STDERR logs by clicking on respective tabs.
     The Performace tab shows the telemetry collected.**

  ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/b1728f29-e1d8-475d-a648-aed01426abfd)

 **11. The final score in the STDOUT tab is the performance of RocHPCG application.**

  ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/db340851-8c92-4e39-93b1-9aa36b4d8a85)

   
