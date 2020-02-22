[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3678960.svg)](https://doi.org/10.5281/zenodo.3678960)

The artifact contains the [Patches](https://github.com/APRStudy/APRStudy/tree/master/Patches) and some [Execution logs](https://github.com/APRStudy/APRStudy/tree/master/Execution%20logs) after executing 16 open-source automated program repair systems (i.e., jGenProg, jKali, jMutRepair, Cardumen, AJRA, GenProg-A, Kali-A, RSRepair-A, Nopol,  DynaMoth, SimFix, kPAR, AVATAR, FixMiner, TBar, and ACS).
Results (i.e., [Patches](https://github.com/APRStudy/APRStudy/tree/master/Patches)) consist of the patches generated by executing 16 open-source automated program repair systems on Defects4J bugs with two different fault localization settings. 
Logs (i.e., [Execution logs](https://github.com/APRStudy/APRStudy/tree/master/Execution%20logs)) record the execution logs of 10 open-source automated program repair systems as the remaining 6 automated program repair systems do not provide execution logs. 

We utilize the recent platform [RepairThemAll](https://github.com/program-repair/RepairThemAll) to perform our study and record the corresponding execution logs, in which ***AstorSystem*** represents _jGenPRog, jKali, jMutRepair, and Cardumen_ four repair tools, ***ArjaSystem*** represents _Arja, GenProg-A, Kali-A, RSRepair-A_ four repair tools, and ***NopolSystem*** represents _Nopol and DynaMoth_ two repair tools.

In the directories of [Execution logs](https://github.com/APRStudy/APRStudy/tree/master/Execution%20logs) and  [Patches](https://github.com/APRStudy/APRStudy/tree/master/Patches), there are two sub-directories: ***NFL*** and ***PFL***.
 - ***NFL*** means the normal fault localization setting with GZoltar-v1.7.2.
 - ***PFL*** means that the fault localization setting is provided with the ground-truth bug positions.


### Patches
All patches are located in the directories that are named with fault localization setting and the related automated program repair system name.
For example, the patches generated by ***ACS*** with ***NFL*** are stored in the directory [Patches/NFL/ACS/](https://github.com/APRStudy/APRStudy/tree/master/Patches/NFL/ACS).
The file for each patch is named with the format **FL-Strategy/APR-tool/BugID_C-OR-P/Patch_Number1_Number2.txt**,
 - **FL-Strategy** is fault localization setting under which the patch is generated.
 - **APR-tool** is the APR technique that generates the patch.
 - **BugID** is the bug ids of the related Defects4J bugs containing two fields (i.e., **ProjectName** and **BugNumber**), for example, Chart-1.
 - **C-OR-P** denotes whether the generated patch is correct (C) or plausible (P).
 - **Number1** is the number of patches generated by each automated program repair system when the correct patch is generated.
 - **Number2** is the number of patches, that can pass the compiling process successfully, generated by each automated program repair system when the correct patch is generated.
 For example, Patches/NFL/ACS/[Chart-14_C](https://github.com/APRStudy/APRStudy/tree/master/Patches/NFL/ACS/Chart-14_C)/[Patch_116_32.txt](https://github.com/APRStudy/APRStudy/tree/master/Patches/NFL/ACS/Chart-14_C/Patch_116_32.txt): When setting with the normal fault localization, executing ACS on bug Chart-14. The generated patch for bug Chart-14 is correct.
 And there are 116 patch candidates generated by ACS for fixing bug Chart-14, 32 of them can pass the compiling process successfully.
 
### Correlation between Patches and Logs
When trying to match each patch generated under **RepairThemAll** framework with its corresponding execution log, please consider the step below:

1. Go to the **Execution logs** folder and choose corresponding **FL-Strategy**;
2. Choose correct **Repair System** according to the APR-tool you are concerning about, based on what we have introduced above;
3. Choose corresponding **ProjectName** and **BugNumber** according to the **BugID**;
4. Click on **APR-tool**.  

After entering the folder you can find a file named _repair.log_ and that is exactly what you are looking for.

