ANDIS Potential Mannual  
*******************************
package version 1.0

1. Introduction.

   ANDIS is an atomic angle- and distance-dependent statistical potential devoted for
   protein structure quality assessment. Five angles are calculated for each atom-pair
   with distance < dcut (dcut is adjustable from 7.0 to 15.0 Angstrom) and residue
   separation ≥ 7 in protein structure. The observed frequencies of atom-pair distances
   and corresponding angles are converted to a combined statistical potential based on
   the inverse Boltzmann law. ANDIS naturally integrates the atomic orientation-dependent
   and distance-dependent interactions. We benchmarked ANDIS with a comprehensive list
   of publicly available statistical potentials. ANDIS demonstrate a significantly better
   ability of native recognition than the other tested potentials.

   The package includes following files:

     1) ANDIS         : The executable program to calculate ANDIS score;
     2) scoang.dat    : The score matrix of five distance-dependent angles (5*167*167*29*12);
     3) scodis.dat    : The score matrix of atom-pair distances (167*167*29);
     4) sidegeom.dat  : Side-chain geometry data;
     5) atom.dat      : Atom-type data;
     6) readme        : Readme file;
     7) example.pdb   : The example pdb file.

2. Installation.

   Download the "ANDIS.tar.bz2" file and unpack the files by running "tar jxvf ANDIS.tar.bz2" in Linux.

   Note: 
   "ANDIS" and other data files (scoang.dat, scodis.dat, sidegeom.dat and atom.dat) should be kept in the same folder.

3. Usage.

   E.g.1: ./ANDIS pdbfile [-c dcut]
   E.g.2: ./ANDIS pdbdir pdblist  [-c dcut]

   Notes:
   1. "E.g.2" is recommended for batch calculation (to avoid reloading score matrices).
   2. The "pdblist" file should be put in "pdbdir" along with all PDB files.
   3. Distance cutoff "dcut" should be in the range of 7.0-15.0 Angstrom (default: 15.0).
   4. A lower "dcut" is recommended for native structure recognition.

4. Contact.

   For question and comments, please contact: 
   Haiyou Deng (hydeng@mail.hzau.edu.cn)

5. Reference.

   Please cite following paper when you use the ANDIS potential:

   Zhongwang Yu, Yuangen Yao, Haiyou Deng, Ming Yi.
   ANDIS: an atomic angle- and distance-dependent statistical potential for protein structure quality assessment.
   BMC Bioinformatics (2019) 20:299

6. Data sets used for building and testing ANDIS potential.
   
   Download non-redundant PDB dataset (3519 experimental structures with Identity cutoff =20%, Resolution cutoff =2.0 angstroms, R-factor cutoff =0.25): https://github.com/haiyoudeng/PDBdataset
   
   Download 175 CASP10-13 decoy sets: https://github.com/haiyoudeng/CASP10-13
   
