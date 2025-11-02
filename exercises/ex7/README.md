# Exercise 7 - Validate Results: Complete Data Validation
<p align="justify">In this exercise, you will validate the outcome of the <b>selective data transition</b> and review how the migrated and transformed data is verified in the target system.</p>

This exercise consists of the following sub-exercises:
- [Exercise 7.1 – Review SFIN Migration](#exercise-71--review-sfin-migration)
- [Exercise 7.2 – Complete Data Validation](#exercise-72--complete-data-validation)

<br>

## Exercise 7.1 – Review SFIN Migration
<p align="justify">In this sub-exercise, you will review the <b>SFIN Migration</b> in the target system to ensure that the accounting conversion has been successfully completed.</p>

### Steps:
Follow these steps to complete the exercise:<br>
1.  Log on to the **TGT** system in SAP GUI, client **400**, using the user **DEMOXX** (replace *XX* with your exercise number, for example **DEMO01**), and open the transaction **FINS_MIG_STATUS** (Start and Monitor Migration).<br>
2.  The **SFIN Migration Monitor** appears. Review the configuration and ensure that the migration status is Completed.<br><br>
    During the migration process, the original source tables are copied into temporary tables in the target system. Since **SAP S/4HANA** introduces a new accounting data model, the financial data must be **converted and reorganized** into the **universal journal structure** (ACDOCA).<br><br>
    ![](/exercises/ex7/images/Screenshot-1-01.png)<br>

3.  This confirms that the **accounting data** has been successfully converted into the **universal journal** in the target system.<br>
4.  **Congratulations!** You have successfully completed this sub-exercise.<br><br><br> 


## Exercise 7.2 – Complete Data Validation
<p align="justify">After confirming the successful accounting migration, you will now complete the <b>data validation</b> in the <b>target system</b>. Using the <b>Data Transition Validation</b> (DTV) tool, you will execute the extraction and comparison steps to ensure that the migrated data in <b>SAP S/4HANA</b> is consistent with the source system.</p>

### Steps:
Follow these steps to complete the exercise:<br>
1.  Log on to the **TGT** system in SAP GUI, client **400**, using the user **DEMOXX** (replace *XX* with your exercise number, for example **DEMO01**), and open the transaction **DTV** (Data Transition Validation - Tool).<br>
2.  In the **Project ID** field, select **DTV_CS162_XX** [1] (replace *XX* with your exercise number, for example **DTV_CS162_01**) and choose **Change** [2].<br><br>
    ![](/exercises/ex7/images/Screenshot-2-01.png)<br>

3.  The project details open. Double-click **Maintain Systems** to review the configuration.<br><br>
    ![](/exercises/ex7/images/Screenshot-2-02.png)<br>

4.  The **Maintain** Systems screen opens. The **target system** (S4) has now been created and is available for validation.<br><br>
    ![](/exercises/ex7/images/Screenshot-2-03.png)<br>

5.  Use the **Back** button in SAP GUI to return to project overview. Choose **Execute Data Extraction**.<br><br>
    ![](/exercises/ex7/images/Screenshot-2-04.png)<br>

6.  Navigate to **Financial Accounting** > **General** > **Report** > **RFBILA00**, and select your **S4** system [1]. Generate the work items first [2], and then extract the data using **Run Selected** [3]. Use **Refresh** to monitor the current status.<br><br>
    ![](/exercises/ex7/images/Screenshot-2-05.png)<br>

7.  The data has now been successfully extracted, indicated by the **green traffic light**.<br><br>
    ![](/exercises/ex7/images/Screenshot-2-06.png)<br>

8.  Use the **Back** button in SAP GUI to return to project overview. Choose **Evaluate Data**.<br>
9.  Navigate to **Financial Accounting** > **General** > **Report**, and select **RFBILA00**. Choose **Run Selected** to evaluate the data and use **Refresh** to monitor the progress.<br><br>
    ![](/exercises/ex7/images/Screenshot-2-07.png)<br>

10. The data has now been successfully extracted, indicated by the **green traffic light**.<br><br>
    ![](/exercises/ex7/images/Screenshot-2-08.png)<br>

11. Once the evaluation is complete, double-click **RFBILA00** [1] to review the results.<br><br>
    Open the **Result** tab [2] to compare the evaluated data from both systems.<br><br>
    As you can see, the data between the **source** and **target system** is identical. Click the **table icon** [3] to display the detailed results.<br><br>
    ![](/exercises/ex7/images/Screenshot-2-09.png)<br>

11. The output for each system is displayed, confirming that the validation results match across both systems.<br><br>
    ![](/exercises/ex7/images/Screenshot-2-10.png)<br>

12. **Congratulations!** You have successfully completed this sub-exercise.<br><br><br> 


## Optional: Test Your Knowledge
Run this optional [quiz](https://quiz-app-gk8jvkhz.cfapps.eu10-005.hana.ondemand.com/cs162/quiz/e0c1mzp3) to test your understanding. If you prefer to skip it, continue with the next exercise.<br>

> **💡 TIP**: To open this link in a new tab, **right-click** and choose **Open Link in New Tab**.
<br>

## Summary
<p align="justify">You have now validated the results of the selective data transition and confirmed that the accounting migration was successfully completed in the target system. Using the <b>Data Transition Validation</b> (DTV) tool, you executed and compared the extracted data from both the <b>source</b> and <b>target systems</b>, verifying that the results are consistent and complete. With this, the <b>data validation phase</b> has been successfully finalized, ensuring the <b>accuracy and integrity</b> of your migration results.</p>
<p align="justify">🎉 <b>Congratulations</b> — This concludes the hands-on session <b>Data-Driven transition guidance toward the cloud</b>. You have successfully completed an end-to-end <b>Lean Selective Data Transition</b> using <b>SAP Business Transformation Center (BTC)</b>.</p>