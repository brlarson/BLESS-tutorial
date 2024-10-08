READ ME File -- update accordingly 
This project presents a clinical use case involving automated monitoring of the patient-controlled opioid infusion after a surgical procedure.
It demonstrates how the trusted composition of Internet of Medical Things (IoMT) may be achieved across an imperfect network.
It also shows how a system level safety property, specified as an invariant, can be deduced from invariants of the highly assured and less assured sub-components 

This project is composed of four main folders:

1) aadl folder contains packages and properties sub-folders. The packages folder contains the AADL packages for Assertions (IoMT_Assertions.aadl), Types (IoMT_Types.aadl), Units(IoMT_Units.aadl), and AADL stucture and behavior specification (IoMTwin.aadl). The properties folder contains AADL properties specification (IoMT_Properties.aadl)
2) The diagrams folder contains AADL diagrams for IoMT system and its sub-systems
3) The proof folder has the proof file proof.txt containing 334 theorems. For each theorem a description on why it was created and how it is solved.
4) The proofscripts folder has the proof scripts (containing BLESS proof tactics) for each sub-system (IoMTwin_PO.ps, IoMT_RM.ps, IoMT_Coodinator.ps)  and their connections (Composition_All.ps). The IoMT_Master.ps runs all of them. 

In order to review the AADL models with structure and Behavior specification, generate verfication conditions, and to run proof scripts, follow below instruction:

1) Install OSATE from https://osate.org/download-and-install.html. Run OSATE and set the workspace.
2) To install BLESS, click Install Additional OSATE component under the Help menu and select BLESS (with praying hands). Follow the instructions to install BLESS. The successfull instalation will show praying hands icon in the Toolbar and BLESS menu in the menu bar.
3) Right click in AADL Navigator and import this project (IoMT) from git using this address:  https://github.com/brlarson/BLESS-models/tree/860f63ab758f2c42bba12aaa422814194e155dc8/IoMT
4) Open the IoMTwin.aadl under the IoMT->packages->aadl folder.  
5) Right click on the System SysIoMT.impl in the outline and click Generate BLESS Verification Conditions. This will generate all verfication conditions and will display required information in the console. 
6) Click get new script under Commands in the BLESS menu and select IoMT_Master.ps.
7) Click run proof script under Commands in the BLESS menu. This will run all the proof scripts and will generate theorem derivation window at the end. Track the theorem backwards to see how they are prooved.