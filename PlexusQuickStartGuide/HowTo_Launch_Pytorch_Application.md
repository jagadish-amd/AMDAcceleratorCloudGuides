***

# How To Launch PyTorch Docker Application

***

 **1. Login to https://aac.amd.com/.**
 
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/d62dc96e-e37a-42b3-9b0e-72445014a621)

 **2. Click on Applications. Select PyTorch.**
 
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/841e8a7d-5dec-40fe-8b79-7ba8eb1213ac)

 **3. In the 'Select An Application' pop-up, select the desired PyTorch version with container type as docker**
    
   **Note**: In this case, we have selected **PyTorch 1-12-1 ROCm5-4 Python 3-8** version and container as docker.
   
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/cf9ab1fc-4633-47de-af44-6f8cac58d59d)

 **4. Click on 'New Workload' button available on the top right corner.**

   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/49eb1722-d350-429a-8dae-247b9bdbb25d)

  **5. Click Next button to continue.**

   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/288c5513-1c13-482d-9e72-69c9cfd9e4fc)
  
  **6. In *Select Resources* page, specify the number of GPU's (e.g., 1 GPU) and max allowed runtime required for the workload. Click Next button.**

  **Note:** The maximum number of GPUs should be 8.

   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/913a2fc5-bdf2-4948-bf68-1e824b9d0a4c)
   
&emsp; The time for which workload is allowed to run should be specified in the **Maximum allowed runtime** field. By default 1 hour will be selected.

&emsp; If maximum allowed run time is 1 hour, it implies, workload will run for 1 hour and then it will be automatically stopped after 1 hour as it will not be allowed to exceed **Maximum allowed runtime**.

&emsp; Based on the time required for workload, user should change the **Maximum allowed runtime**.

&emsp; Once the workload is launched, user cannot change the total workload time. It has to be configured in this step.

  **8. Select the cluster and desired queue to run the job. In this case 1CN128C8G2H_2IB_MI210_SLES15 is selected. Click on Next.**

   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/433cd874-e38d-418f-9e9f-7d08cb14308c)

   **9. Review all the configurations selected and click on Run Workload.** 

   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/e4f457c7-9b65-4b0c-a96a-9b56776547e9)
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/6d4b30f1-6f07-4bba-b3a0-ab7a93d0ab05)
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/11f3064b-6a4b-4460-b5a0-6f84c8bc0841)
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/89d484f1-5b01-436c-b324-5d6614bbad74)

   **10. Once the workload is submitted, the workload status changes to *Running* when queue is available. Click on the running workload**

   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/e1f495c6-a9c7-4442-a1f9-ffd5771f3b98)

   **11. User can see the system logs in SYSLOG, output in STDOUT and errors in STDERR tabs.**
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/40241c24-85a4-4612-ba4e-d2c490ffefea)

   **12. A token will be generated in *STDOUT* tab in yellow color as shown below. Copy the token.**
    
   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/b76d78c4-5089-404c-b189-675bae7a76c4)


   **12. Once the interactive endpoints are enabled, click 'Connect' to launch ML Studio(Jupyter lab).**

   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/cac47a19-d778-47c2-953c-df444beef3d5)

   **13.Jupyter lab opens. Paste the token in 'Password or token' field. Click login.**

   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/08e56d2c-83a8-4725-b092-ee96a16a391a)

   **14. User can see the below screen. This Jupyter lab can be used for python based development work.**

   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/bc1829da-8b48-42cb-9345-48474f95cbd4)

   **15. Once the work is done with Jupyter lab, Close it** 
   
   **16. Click 'Finish Workload' button.**

   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/87c49830-f631-42cb-8970-f8c445982ba9)

   **17. Logs can be downloaded from STDOUT tab by clicking 'Download Logs' once workload is finished.**

   ![image](https://github.com/amddcgpuce/AMDAcceleratorCloudGuides/assets/137475062/33826588-f3fd-426a-a3e6-b1a297912146)
