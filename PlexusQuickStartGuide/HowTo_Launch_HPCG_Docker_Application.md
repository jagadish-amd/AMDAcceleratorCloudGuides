***

# How To Launch RocHPCG Docker Application

***

1. Login to **https://aac.amd.com/.**

    ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/d62dc96e-e37a-42b3-9b0e-72445014a621)


2. Click on Applications. Select **HPCG**.

    ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/5d521fdb-046e-4963-9068-db42f71a59c9)

3. Select the desired **RocHPCG** version with desired container type as **docker/singularity**.
    
   **Note**: In this case, we have selected **rocHPCG 3.1.0_97** version and container as **docker**.

    ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/7c489772-18f4-464c-a0be-6b3048c59be1)


4. Click on **'New Workload'** button available on the top right corner.

    ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/e4814a18-fa65-4ab8-83c4-a7d20a0e4ba3)


5. Click **Next** button to continue.

    ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/e420e08e-5b7b-4a48-819d-fea3d1f8dc7b)
   

6. Click **Next** to continue with default script.
    **Note:** Default script is for 8 GPUs
    ```
    mpirun --mca pml ucx -np 8 rochpcg 336 168 672 1860
    ```
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/ce2ccd72-1286-458b-a28c-1939d5dd2669)


7. Select the allowed run time. The number of GPUs should be 8. Here, we have selected the run time as 1 hour, number of GPU’s as 8 and telemetry is enabled.
   Click on **Next** button.

   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/0605bc6f-7136-4b7b-9d79-3faf33a444d0)
   

8. Select the cluster and desired queue to run the job. In this case **1CN128C8G2H_2IB_MI210_SLES15** was selected. Click on **Next**.

   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/6063268b-227c-4a2f-8967-456f69ed1b41)
  

9. Review all the configurations selected and click on **Run Workload**.
 
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/1953602c-4d0f-481d-b42e-5ddfc8ecae39)
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/854b206a-c5a8-452a-b2cc-16e99dbadb94)
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/854f7e2e-2c5b-47de-a453-6b2ea7ff3728)
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/de586d6f-87ad-4e9d-8c4e-b6ebd9a3e49c)


10. Once the application execution is successful then the status gets changed into **“Completed”**.
    The user can check the **STDOUT** and **STDERR** logs by clicking on respective tabs.
    The **Performace** tab shows the telemetry collected.

    ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/4f113aa6-f7ba-4c26-b62e-c3c22df8b552)


11. The final score in the STDOUT tab is the performance of RocHPCG application.**
    
    ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137474607/01b04c4f-c514-41b1-8028-e7ae476e6b3d)
