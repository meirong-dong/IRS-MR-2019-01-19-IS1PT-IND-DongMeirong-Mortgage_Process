# Machine Reasoning Course Report - Individual

## SECTION 1 : PROJECT TITLE
1. Automated Qualifying Process to check if the mortgage amount is in limit
2. Automated AgeChecking Process to check if applicant's age is <65 and >=21 years old

### Mortgage Business Process Enhancement

---
## SECTION 2 : EXECUTIVE SUMMARY
The current Mortgage Process discussed during the class workshops demonstrates that how Machine Reasoning can simplify the mortgage application process by taking an automated rule-based approach and assist the final approver in assessing a mortgage application.

The discussed process can be further enhanced by enabling the rules engine to take into account the credit rating level of the applicant. Based on the Credit Score description by the [Credit Bureau of Singapore](https://www.creditbureau.com.sg/credit-score.html), we can additionally consider the Risk Grade of the application. In this report, we shall define an applicant to be more credible if the applicant has a Risk Grade of "CC" or higher (rating of 1825 to 2000).

The aforementioned rule shall be enhanced in the Guided Decision Table "MortgageMachineReasoningDT" with the corresponding validation (valid values of credit rating is between 1000 and 2000) added in the Guided Rule "Validate Credit Rating".


---

## SECTION 3 : USER GUIDE

### [ 1 ] To run the system using iss-vm

1. Download pre-built virtual machine from http://bit.ly/iss-vm

2. start iss-vm

3. Launch KIE 7.12 via the shortcut "Tool KIE 7.12"

4. After startup is complete, launch Google Chrome and click on the "KIE WB" shortcut

5. Login using role "wbadmin"

6. Create New Workspace

7. Import Project from [Github](https://github.com/yoke2/IRS-MR-2019-01-19-IS1PT-IND-WongYokeKeong-Mortgage_Process.git) or using the provided zip file "IRS-MR-2019-01-19-IS1PT-IND-DongMeirong-Mortgage_Process.zip"

8. Choose "Mortgage_Process" tile to import and click on OK

9. Deploy Project with Deployment Unit ID "mortgage-process_1.0.0-Enhanced"

10. Mortgage Process Instance can be launched with role "wbadmin"

11. Final Approval process can be completed by accessing Task Inbox using role "wbadmin"

### [ 2 ] To run the system in other/local machine:

1. Download jBPM Server 7.12.0 from https://download.jboss.org/jbpm/release/7.12.0.Final/jbpm-server-7.12.0.Final-dist.zip

2. Download and unzip it.
    * On Linux/Mac, run jbpm-server-7.12.0.Final-dist/bin/standalone.sh
    * On Windows, run jbpm-server-7.12.0.Final-dist/bin/standalone.bat
    * Open browser and go to http://localhost:8080/jbpm-console/kie-wb.jsp

3. Follow Step 5 in [1] onwards with
    * "wbadmin" configured with group "kie-server" and roles "process-admin", "admin", "analyst", "user"
 

---
## SECTION 4 : Appendix

### Enhancement Test Results Demonstration.pdf
* This file contains the test results before and after the implementation of the enhancements to Credit Rating Risk Grade and Credit Rating validation

---

**This [Machine Reasoning (MR)](https://www.iss.nus.edu.sg/executive-education/course/detail/machine-reasoning "Machine Reasoning") course is part of the Analytics and Intelligent Systems and Graduate Certificate in [Intelligent Reasoning Systems (IRS)](https://www.iss.nus.edu.sg/stackable-certificate-programmes/intelligent-systems "Intelligent Reasoning Systems") series offered by [NUS-ISS](https://www.iss.nus.edu.sg "Institute of Systems Science, National University of Singapore").**
