The artifact contains the [results](https://github.com/APRStudy/APRStudy/Patches) and some [logs](https://github.com/APRStudy/APRStudy/Execution%20logs) after executing 16 open-source automated program repair systems (i.e., jGenProg, jKali, jMutRepair, Cardumen, AJRA, GenProg-A, Kali-A, RSRepair-A, Nopol,  DynaMoth, SimFix, kPAR, AVATAR, FixMiner, TBar, and ACS).
Results (i.e., [Patches](https://github.com/APRStudy/APRStudy/Patches)) consist of the patches generated by executing 16 open-source automated program repair systems on Defects4J bugs with two different fault localization settings. 
Logs (i.e., [Execution logs](https://github.com/APRStudy/APRStudy/Execution%20logs)) record the execution logs of 10 open-source automated program repair systems as the remaining 6 automated program repair systems do not provide execution logs.


In the directories of [Execution logs](https://github.com/APRStudy/APRStudy/Execution%20logs) and  [Patches](https://github.com/APRStudy/APRStudy/Patches), there are two sub-directories: ***NFL*** and ***PFL***.
 - ***NFL*** means the normal fault localization setting with GZoltar-v1.2.0.
 - ***PFL*** means that the fault localization setting is provided with the ground-t	ruth bug positions.


### Patches
All patches are located in the directories that are named with fault localization setting and the related automated program repair system name.
For example, the patches generated by ***ACS*** with ***NFL*** are stored in the directory [Patches/NFL/ACS/](https://github.com/APRStudy/APRStudy/Patches/NFL/ACS).
The file for each patch is named with the format **BugID_Correct-OR-Plausible/Patch_Number1_Number2.txt**,
 - **BugID** is the bug ids of the related Defects4J bugs, e.g., Chart-1).
 - **Correct-OR-Plausible** denotes whether the generated patch is correct (C) or plausible (P).
 - **Number1** is the number of patches generated by each automated program repair system when the correct patch is generated.
 - **Number1** is the number of patches, that can pass the compiling process successfully, generated by each automated program repair system when the correct patch is generated.
 For example, Patches/NFL/ACS/[Chart-14_C](https://github.com/APRStudy/APRStudy/Patches/NFL/ACS/Chart-14_C)/[Patch_116_32.txt](https://github.com/APRStudy/APRStudy/Patches/NFL/ACS/Chart-14_C/Patch_116_32.txt): When setting with the normal fault localization, executing ACS on bug Chart-14. The generated patch for bug Chart-14 is correct.
 And there are 116 patch candidates are generated by ACS for fixing bug Chart-14, 32 of them can pass the compiling process successfully.
 