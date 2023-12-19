# ANM-LD and Transfer Entropy Codes

## ANM-LD

ANMLD.zip file contains scripts, functions, parameter and input files necessary to run ANM-LD simulations presented in this paper.

**Scripts and called functions:**
* anm_gnm_target_overlap.m: The function for ANM mode overlap calculations.
* matlab_newmethod.m: The main MATLAB script file that is called by the batch script file.
* pdb2mat.m, mat2pdb.m: Helper functions to convert files between the PDB formats and MATLAB data structures.
* submitANMLD.sh: The batch script file that submits a new ANM-LD run.
* min.sh: The batch script file that submits the minimization.

**Parameter files:**
* min.in: AMBER parameter file used for the energy minimization steps. 
* LD_matlab.in: AMBER parameter file used for the LD molecular simulation. 
* ptraj.in: Script for outputting pdb files after minimization steps.
* tleap.in: AMBER parameter file used for topology and coordinate generation.

**Input files:**
* step.txt: The input file with the initial cycle number and the names of the initial and target PDB files. This file is updated at each cycle with the names of the created pdb files throughout the performed run.
* Initial.pdb: Dephosphorylated CFTR (5UAK) modified to have the same amount of residues as the target structure.
* Target.pdb: Phosphorylated CFTR (6MSM) modified to have the same amount of residues as the initial structure.
* Initial/Target_min.pdb: Minimized structures.
* Initial/Target_CA_min.pdb: Minimized files with only CA atoms.
* Initial/Target_min.rst:
* Target...algn.pdb/rst: Target structure aligned to the initial structure.

## Transfer Entropy

TransferEntropy.zip file contains scripts, functions, and input files necessary to run transfer entropy calculations presented in this paper.

**Scripts:**
* GNMtransferentropy_DegreeOfCollectivity.m: Main script that performs TE and collectivity calculations for 1-10 modes.
* OptimumTau_automated.m: Helper function that determines the tau to be used in the main TE script. 

**Input files:**
* 5uak_TE.pdb: Dephosphorylated CFTR modified to be compatible with the TE code.
* 6msm_TE.pdb: Phosphorylated CFTR modified to be compatible with the TE code.

## Citation

Please cite this article and the previous articles that ANM-LD has been introduced in:
* Ersoy Ayca, Altintel Bengi, Livnat Levanon Nurit, Ben-Tal Nir, Haliloglu Turkan, Lewinson Oded. Computational analysis of long-range allosteric communications in CFTR. bioRxiv 2023.06.07.543997; [doi: 10.1101/2023.06.07.543997]
* Acar B, Rose J, Aykac Fas B, Ben-Tal N, Lewinson O, Haliloglu T. Distinct Allosteric Networks Underlie Mechanistic Speciation of ABC Transporters. Structure. 2020 Jun 2;28(6):651-663.e5. [doi: 10.1016/j.str.2020.03.014]
* Yang M, Livnat Levanon N, Acar B, Aykac Fas B, Masrati G, Rose J, Ben-Tal N, Haliloglu T, Zhao Y, Lewinson O. Single-molecule probing of the conformational homogeneity of the ABC transporter BtuCD. Nat Chem Biol. 2018 Jul;14(7):715-722. [doi: 10.1038/s41589-018-0088-2]

Please cite the following articles if you would like to use Transfer Entropy:
* Hacisuleyman, A., Erman, B. Causality, transfer entropy, and allosteric communication landscapes in proteins with harmonic interactions. Proteins: Structure, Function, and Bioinformatics, 2017, 85(6), 1056-1064. [doi: 10.1002/prot.25272]
* Ersoy Ayca, Altintel Bengi, Livnat Levanon Nurit, Ben-Tal Nir, Haliloglu Turkan, Lewinson Oded. Computational analysis of long-range allosteric communications in CFTR. bioRxiv 2023.06.07.543997. [doi: 10.1101/2023.06.07.543997]
* Altintel B, Acar B, Erman B, Haliloglu T. Subsets of Slow Dynamic Modes Reveal Global Information Sources as Allosteric Sites. J Mol Biol. 2022 Sep 15;434(17):167644. [doi: 10.1016/j.jmb.2022.167644]
