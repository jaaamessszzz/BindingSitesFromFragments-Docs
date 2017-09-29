*******************************
Align
*******************************

From the ``Compounds/`` directory, enter: ::

    bsff align <Compound_ID>

Where <Compound_ID> is the name of the project directory for your target molecule. After running ``search, every
subdirectory under ``<Compound_ID>/Fragment_PDB_Matches/`` contains PDBs with a ligand bound that contains the
corresponding fragment as a  substructure with the same local chemical environment as the target molecule.

For each ligand-protein complex, the ``align`` function will identify the fragment substructure and align the substructure
and all residues within 12A of the fragment onto the reference fragments in the ``Fragment_Inputs/`` directory. Protein-ligand
complexes are only use if they pass certain filters:

    * All atoms in the ligand are represented in the PDB
    * No ligand atoms have alternate location records
    * User-defined RMSD cutoff for poor alignments of fragment substructure onto reference

