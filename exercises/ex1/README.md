# Exercise 1 - Build the Foundation: Upload UDP File
<p align="justify">In this exercise, you will extract the <b>Usage and Data Profiling</b> (UDP) analysis file from the source SAP ERP 6.0 system and upload it to the <b>Manage Analysis File</b> app in <b>SAP Cloud ALM</b>. The UDP file contains key system information such as company codes and transformation objects. It forms the foundation of your digital blueprint, enabling data scoping and migration in later steps.</p><br>

## Steps:
Follow these steps to complete the exercise:<br>
1.  Log on to the **SRC** system in SAP GUI, client **300**, using the user **DEMOXX** (replace *XX* with your seat number, for example **DEMO01**), and open transaction **SE38** (ABAP Editor).<br>
2.  In the **Program** field, enter **RC_UDP_START_DMR2** [1] and choose **Execute** (F8) [2].<br><br>
    ![](/exercises/ex1/images/Screenshot-01.png)<br>
3.  Choose **Download DRM2 Analysis Data** and save the file to your local disk.<br><br>
    ![](/exercises/ex1/images/Screenshot-02.png)<br>
4.  Switch to [SAP Cloud ALM](https://calm-consarea-sdt.eu10-004.alm.cloud.sap) and log in with the user **DEMOXX** (replace *XX* with your seat number, for example **DEMO01**).<br>

    > **💡 TIP**: To open this link in a new tab, **right-click** and choose **Open Link in New Tab**.

5.  Navigate to **Transformation** [1] &gt; **Manage Analysis File** [2].<br><br>
    ![](/exercises/ex1/images/Screenshot-03.png)<br>
6.  In the **Manage Analysis File** application, choose **Create**.<br><br>
    ![](/exercises/ex1/images/Screenshot-04.png)<br>
7.  Enter **UDP_CS162_XX** (replace *XX* with your seat number, for example **UDP_CS162_01**) as the **Name** and keep the default **Analysis Type**.<br><br>
    ![](/exercises/ex1/images/Screenshot-05.png)<br>
8.  Upload the file you downloaded in Step 3 and choose **Create**.<br><br>
    ![](/exercises/ex1/images/Screenshot-06.png)<br>
9.  Confirm that the analysis file has been successfully uploaded.<br><br>
    ![](/exercises/ex1/images/Screenshot-07.png)<br>
10. Open the **Analysis Results** tab to review the content of your uploaded file.<br><br>
    Here, you can see all **company codes** and **transformation objects** detected in the source system.<br><br>
    The **company codes** include details such as the controlling area, country, and data volume, while the **transformation objects** display information about the application component, category, and activity history. You will also notice a section for **HCM data**, which summarizes all **Human Capital Management**-related information identified during the analysis.<br><br>
    ![](/exercises/ex1/images/Screenshot-08.png)<br>
11. **Congratulations!** You have successfully completed this exercise.<br><br><br>


## Optional: Test Your Knowledge
Run this optional [quiz](https://quiz-app-gk8jvkhz.cfapps.eu10-005.hana.ondemand.com/cs162/quiz/45q8xcfn) to test your understanding. If you prefer to skip it, continue with the next exercise.<br>

> **💡 TIP**: To open this link in a new tab, **right-click** and choose **Open Link in New Tab**.
<br>

## Summary
<p align="justify">You have now extracted the <b>Usage and Data Profiling</b> (UDP) analysis file from the source SAP ERP 6.0 system and uploaded it to the <b>Manage Analysis File</b> app in <b>SAP Cloud ALM</b>. This step builds the foundation for creating the digital blueprint in the next exercise.</p>

Continue to - [Exercise 2 - Initialize Project: Create Digital Blueprint](../ex2/README.md)
