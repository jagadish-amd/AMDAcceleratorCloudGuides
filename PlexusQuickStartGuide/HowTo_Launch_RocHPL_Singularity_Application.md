***

# How To Launch RocHPL Singularity Application

***

1. Login to **https://aac.amd.com/.**
    
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/d62dc96e-e37a-42b3-9b0e-72445014a621)


2. Click on **Applications**. Select **HPL**.
    
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/c38b250f-24bd-4a15-8f65-2cca6aeb5bc9)
    
3. Select the desired **RocHPL** version with desired container type as **docker/singularity**.
    
   **Note**: In this case, we have selected **RocHPL_5_0_5_49** version and container as **Singularity**.
    
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/c1ffb82e-933f-4e03-88e4-f968b63dd6f2)

    
4. Click on **'New Workload'** button available on the top right corner.
    
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/62e9a55e-4b7b-420b-834c-bbe7a8f271a1)


5. Click **Next** button to continue.

   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/9614e3fe-88b7-4914-9c08-595a775b9884)

6. Click **Next** to continue with default script.

   **Note:** Default script is for 8 GPUs
      ```
      mpirun_rochpl -P 1 -Q 1 -N 90112 --NB 512
      ```

   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/bf9becb7-d66d-42db-a2e7-ab0f6a786160)
   

7. Select the allowed run time. The number of GPUs should be **8**. Here, we have selected the run time as 1 hour, number of GPU’s as 8 and telemetry is enabled.
   Click on **Next** button.

    ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/6b93f6c7-73b5-45ef-b84d-0d262e7acceb)


8. Select the cluster and desired queue to run the job. In this case **1CN128C8G2H_2IB_MI210_Ubuntu22** was selected. Click on **Next**.

    ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/61f68130-2acd-4661-8853-d3f10f1a3b02)


9. Review all the configurations selected and click on Run **Workload**.
 
    ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/608962cd-fb96-4bc5-9c92-82b114e712a5)
    ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/664534db-054f-40cc-b12d-f648c2c0fa90)
    ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/02559670-4793-445c-8320-f35aa9913ab2)
    ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/7d31d6c5-5e13-44c4-819f-a91e240792df)


10. Once the application execution is successful then the status gets changed into **“Completed”**.
     The user can check the **STDOUT** and **STDERR** logs by clicking on respective tabs.
     The **Performace** tab shows the telemetry collected.
     
    ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/47192b53-1c7f-43cb-a361-932dea1774e1)


11. The final score in the STDOUT tab is the performance of RocHPL application.

    ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/31f202b4-c7ef-4977-9c58-2f7ff876a715)
