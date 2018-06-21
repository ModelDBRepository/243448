README File for 
Bladder Small DRG Neuron Soma Model - Mandge and Manchanda, 2018

Abstract:
Bladder small DRG neurons, which are putative nociceptors pivotal to urinary bladder function, express more than a dozen different ionic membrane mechanisms: ion 
channels, pumps and exchangers. Small-conductance Ca2+-activated K+ (SKCa) channels which were earlier thought to be gated solely by intracellular Ca2+ concentration ([Ca]i ) have recently been shown to exhibit inward rectification with respect to membrane potential. The effect of SKCa inward rectification on the excitability of these neurons is unknown. Furthermore, studies on the role of KCa channels in repetitive firing and their contributions to different types of afterhyperpolarization (AHP) in these neurons are lacking. In order to study these phenomena, we first constructed and validated a biophysically detailed single compartment model of bladder small DRG soma constrained by physiological data. The model includes twenty-two major known membrane mechanisms along with intracellular Ca2+ dynamics comprising Ca2+ diffusion, cytoplasmic buffering, and endoplasmic reticulum (ER) and mitochondrial mechanisms. Using modelling studies, we show that inward rectification of SKCa is an important parameter regulating neuronal repetitive firing and that its absence reduces action potential (AP) firing frequency. We also show that SKCa is more potent in reducing AP spiking than the large-conductance KCa channel (BKCa) in these neurons. Moreover, BKCa was found to contribute to the fast AHP (fAHP) and SKCa to the medium-duration (mAHP) and slow AHP (sAHP). We also report that the slow inactivating A-type K+ channel (slow KA) current in these neurons is composed of 2 components: an initial fast inactivating (time constant ~ 25-100 ms) and a slow inactivating (time constant ~ 200-800 ms) current. We discuss the implications of our findings, and how our detailed model can help further our understanding of the role of C-fibre afferents in the physiology of urinary bladder as well as in certain disorders.

How to run the model:
(Assuming that NEURON is installed in the system)

Windows based Systems
1. Search for NEURON'S mknrndll tool in the Windows start menu and run it. 
Navigate to the model folder location using the "Choose Directory" option. 
When you reach the model folder, Click "List Dir" option and then "Make nrnmech.dll". This compiles all the mod files in this directory 
2. Run the model by double-clicking the mosinit.hoc

Unix based Systems
1. Navigate (change directory) to the model folder in using the terminal.
2. Compile the mod files by calling "nrnivmodl" (without inverted commas) from terminal.
3. Launch the model by using command: "nrngui mosinit.hoc".

For MacOS based Systems
1. Compiling mod files: Follow the instructions given here: https://www.neuron.yale.edu/neuron/static/docs/nmodl/macos.html
2. Launch the model by using command: "nrngui mosinit.hoc".

Below steps are common to all the OS types.

Generatiing, Fig 9A of the paper
>> Go to File in NEURON's Main Menu and click "load hoc".
In the Load menu, Select fig9A.hoc and press "Load".
Press "Init & Run" in NEURON's RunControl panel to generate Fig 9A

Generating Fig 16 A, C and D of the paper
>> Go to File in NEURON's Main Menu and click "load hoc".
In the Load menu, Select fig16ACD.hoc and press "Load".
Press "Init & Run" to generate Fig 16 A, C and D.
Change the gbar_skca3 in the SKCa Conductance Panel to 0.0027 and 0.0045 mho/cm2 and Init & Run for each change.

NOTE: If you are generating Fig 16 after generating Fig 9A, make sure that all previous Current 
Clamp Panel paramters (Delay, Duration and Amplitude) are set to zero.

Reference:
A biophysically detailed computational model of bladder small DRG neuron soma- 
Mandge and Manchanda, 2018 (accepted PLOS Computational Biology, DOI: 10.1371/journal.pcbi.1006293)
