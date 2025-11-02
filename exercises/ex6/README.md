# Exercise 6 - Execute Data Validation: Configure DTV Project & Monitor Cycle
<p align="justify">In this exercise, you will explore the <b>execution phases</b> of your cycle. It manages the <b>end-to-end data transformation</b> between the source and target system - from preparing runtime objects to completing postprocessing activities.</p>
<p align="justify">Due to <b>time constraints</b>, the runtime-intensive phases will be reviewed using a <b>reference cycle</b>. Only the <b>Data Transition Validation</b> (DTV) project configuration will be performed manually in the source system.</p>

This exercise consists of the following sub-exercises:
- [Exercise 6.1 – Review Cycle Preparation](#exercise-61--review-cycle-preparation)
- [Exercise 6.2 – Copy & Review Generated DTV Project](#exercise-62--review-generated-dtv-project)
- [Exercise 6.3 - Configure DTV Project](#exercise-63---configure-dtv-project)
- [Exercise 6.4 - Review Run & Postprocess Cycles](#exercise-64---review-run--postprocess-cycles)

<br>

## Exercise 6.1 – Review Cycle Preparation
<p align="justify">In this sub-exercise, you will review the <b>Cycle Preparation</b> phase of the cycle. During this phase, the system generates runtime objects for transformation and postprocessing — and automatically creates a DTV project in the source system if the DTV tool was enabled.</p><br><br>

> **⚠️ CAUTION**: In this exercise, you will switch to the **reference implementation** cycle. Make sure to follow the instructions carefully to avoid inconsistencies in the process.

<br>

### Steps:
Follow these steps to complete the exercise:<br>
1.  Within your cycle, open **Manage Cycles** [1] context menu and select the **Transformation** [2] application.<br><br>
    ![](/exercises/ex6/images/Screenshot-1-01.png)<br>

2.  The **Transformation** overview is displayed. Choose **Manage Cycles**.<br><br>
    ![](/exercises/ex6/images/Screenshot-1-02.png)<br>

2.  In the **Manage Cycles** application, enter **CYCLE_REFERENCE_IMPL** in the search field [1] and press **Enter**. Then open the corresponding cycle [2].<br><br>
    ![](/exercises/ex6/images/Screenshot-1-03.png)<br>

3.  The **Reference Implementation Cycle** appears. Navigate to **2. Cycle Preparation**.<br><br>
    ![](/exercises/ex6/images/Screenshot-1-04.png)<br>

4.  Choose **Preparation Log** to display the execution details.<br><br>
    ![](/exercises/ex6/images/Screenshot-1-05.png)<br>

5.  The **Cycle Logs** applications opens. Enter **DTV** into the search field [1] and press **Enter**.<br><br>
    As you can see, two log entries confirm that the **DTV project** was created and configured successfully [2].<br><br>
    Through this automation, much of the technical setup is handled by the system, allowing you to focus on configuring only the **DTV reports** relevant for the business data validation.<br><br>
    ![](/exercises/ex6/images/Screenshot-1-06.png)<br>

6.  **Congratulations!** You have successfully completed this sub-exercise.<br><br><br> 


## Exercise 6.2 – Review Generated DTV Project
<p align="justify">After reviewing the cycle preparation, you will now analyze and copy the generated <b>Data Transition Validation</b> (DTV) project in the source system. The DTV project defines the validation scope and enables you to compare and verify data consistency between the source and target systems after the selective data transition.</p>


### Steps:
Follow these steps to complete the exercise:<br>
1.  Log on to the **SRC** system in SAP GUI, client **300**, using the user **DEMOXX** (replace *XX* with your exercise number, for example **DEMO01**), and open the transaction **DTV** (Data Transition Validation - Tool).<br>
2.  In the **Project ID** field, enter **DTV_REFERENCE_PROJECT_XX** [1] and choose **Copy** [2].<br>

    > **ℹ️ NOTE**: Normally, the project is created based on the Transformation Area ID. To simplify this exercise and make the setup more readable, a preconfigured reference project has been provided for you to copy.

    ![](/exercises/ex6/images/Screenshot-2-01.png)<br>

3.  The **Copy Project** dialog opens.<br><br>
    Enter **DTV_CS162_XX** (replace *XX* with your exercise number, for example **DTV_CS162_01**) as the **ID** [1], and choose **Continue** [2].<br><br>
    ![](/exercises/ex6/images/Screenshot-2-02.png)<br>

4.  The **DTV project** is now successfully copied. Choose **Change** to open the project details.<br><br>
    ![](/exercises/ex6/images/Screenshot-2-03.png)<br>

5.  The **Project Overview** appears.<br><br>
    As you can see, three steps have already been configured. Double-click **Maintain Systems** [1] to review the configuration.<br><br>
    ![](/exercises/ex6/images/Screenshot-2-04.png)<br>

6.  The **Maintain Systems** screen opens.<br><br>
    The source system has already been created and preconfigured. The target system will be configured automatically on the target system in the **Postprocess Cycles** phase.<br><br>
    ![](/exercises/ex6/images/Screenshot-2-05.png)<br>

7.  Use the **Back** button in SAP GUI to return to project overview. Choose **Project Global Data**.<br><br>
    ![](/exercises/ex6/images/Screenshot-2-06.png)<br>

8.  The **Project Global Settings** screen opens.<br><br>
    The settings from your **blueprint** have been extracted and preconfigured in the **DTV project**.<br><br>
    Click on **Company_Code** to review the configuration — this parameter already contains the value **2000**, which was transferred from the model.<br><br>
    ![](/exercises/ex6/images/Screenshot-2-07.png)<br>

9.  Use the **Back** button to return to the project overview. Choose **Define Test Specification**.<br>
10. Select all entries from the table except **RFBILA00** [1] and choose **Delete** [2].<br><br>
    ![](/exercises/ex6/images/Screenshot-2-08.png)<br>

11. The table now only contains the **RFBILA00** entry, as shown below.<br><br>
    This program is used to validate financial balances and will be configured in the upcoming exercise.<br><br>
    ![](/exercises/ex6/images/Screenshot-2-09.png)<br>
12. Use the **Back** button to return to the project overview.<br>
13. **Congratulations!** You have successfully completed this sub-exercise.<br><br><br>


## Exercise 6.3 - Configure DTV Project
<p align="justify">After copying the DTV project in the previous step, you will now configure it on the source system and perform the data extraction.</p>

### Steps:
Follow these steps to complete the exercise:<br>
1.  Within the project overview, double-click **Define Test Specification**.<br><br>
    ![](/exercises/ex6/images/Screenshot-3-01.png)<br> 

2.  Double-click the **RFBILA00** report to open the details. Select **Conditions** and change the parameters **BILBJAHR** and **BILVJAHR** to **2021**.<br><br>
    ![](/exercises/ex6/images/Screenshot-3-02.png)<br> 
3.  Use the **Back** button to return to the project overview and choose **Simulation**.<br>
4.  Select the **RFBILA00** report [1], the system **ECC** [2], and choose **Generate Workitems** [3].<br><br>
    ![](/exercises/ex6/images/Screenshot-3-03.png)<br> 

5.  The workitems have now been successfully generated.<br><br>
    ![](/exercises/ex6/images/Screenshot-3-04.png)<br> 

6.  Keep your selection and choose **Simulate**.<br><br>
    ![](/exercises/ex6/images/Screenshot-3-05.png)<br> 

7.  The simulation has now been successfully completed – 142 records were processed.<br><br>
    ![](/exercises/ex6/images/Screenshot-3-06.png)<br> 

8.  Use the **Back** button to return to the project overview and choose **Execute Data Extraction**.<br>
9.  In **Financial Accounting** > **General** > **Report** > **RFBILA00**, select your **ECC** system [1], and then choose **Import Simulation Results** to proceed [2].<br>

    > **💡 TIP**: If a simulation has already been executed, you can use **Import Simulation Results** to avoid performing the data extraction a second time.

    ![](/exercises/ex6/images/Screenshot-3-07.png)<br> 

10. The data has now been successfully extracted, indicated by the **green traffic light**.<br><br>
    ![](/exercises/ex6/images/Screenshot-3-08.png)<br> 

11. Double-click on the **ECC** system [1]. The details appear. Open the **Worklist Items** [2] or **Result** [3] tab to explore the extracted data from the source system.<br><br>
    ![](/exercises/ex6/images/Screenshot-3-09.png)<br> 

12. Use the **Back** button to return to the project overview. All relevant tasks have now been executed successfully.<br><br>
    ![](/exercises/ex6/images/Screenshot-3-10.png)<br> 

13. **Congratulations!** You have successfully completed this sub-exercise.<br><br><br> 


## Exercise 6.4 - Review Run & Postprocess Cycles
<p align="justify">After completing the configuration and data extraction on the source system, you will now review the execution and postprocessing phases using a reference cycle. These phases show how the migration and validation logic are executed in sequence and how the DTV project is transferred to the target system.</p>

### Steps:
Follow these steps to complete the exercise:<br>
1.  Within the reference cycle, open the **3. Run Cycles** tab.<br><br>
    ![](/exercises/ex6/images/Screenshot-4-01.png)<br>

2.  Choose **Go to Run Cycles**.<br><br>
    ![](/exercises/ex6/images/Screenshot-4-02.png)<br>

3.  Enter **FI Document** into the search field [1] and press **Enter**.<br><br>
    You can see how the data transformation, for example for **financial documents**, was executed during runtime.<br><br>
    ![](/exercises/ex6/images/Screenshot-4-03.png)<br>

4.  Use the **Back** button to return to the cycle overview.<br>
5.  Open the **4. Postprocess Cycles** tab.<br><br>
    ![](/exercises/ex6/images/Screenshot-4-04.png)<br>

6.  Choose **Go to Postprocess Cycles**.<br><br>
    In the postprocessing phase, the migrated data is converted to match the release and data structures of the target system using the ABAP upgrade mechanism. This ensures that the transferred data and configuration are fully compatible with SAP S/4HANA.<br><br>
    ![](/exercises/ex6/images/Screenshot-4-05.png)<br>

7.  Enter **DTV** into the search field [1] and press **Enter**.<br><br>
    The program **BDTS_DTV_TABLE_TRANSFER** is executed in this phase. It transfers the DTV project and related configuration tables from the source system to the target system and automatically extends the setup to include the new SAP S/4HANA environment.<br><br>
    ![](/exercises/ex6/images/Screenshot-4-06.png)<br>

8.  Use the **Back** button to return to the cycle overview.<br>
9.  **Congratulations!** You have successfully completed this sub-exercise.<br><br><br> 

## Optional: Test Your Knowledge
Run this optional [quiz](https://quiz-app-gk8jvkhz.cfapps.eu10-005.hana.ondemand.com/cs162/quiz/1dma2oio) to test your understanding. If you prefer to skip it, continue with the next exercise.<br>

> **💡 TIP**: To open this link in a new tab, **right-click** and choose **Open Link in New Tab**.
<br>

## Summary
<p align="justify">You have now validated the <b>preparation phase</b> and confirmed that the <b>DTV project</b> was successfully generated. In the source system, you copied, reviewed, and configured the project, executed the data extraction, and explored the runtime and postprocessing phases. With this, the <b>cycle execution</b> and <b>DTV project</b> have been successfully validated, and you are ready to <b>verify the results</b> in the next exercise.</p>

Continue to - [Exercise 7 - Validate Results: Complete Data Validation](../ex7/README.md)
