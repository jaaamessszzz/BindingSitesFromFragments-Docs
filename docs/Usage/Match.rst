********************************
Match Binding Sites to Scaffolds
********************************

Ask James for scripts, press enter.

Filtering Matches
=================

Matches are filtered based on the following criteria:

    * CB within shell around ligand (11A)
    * Percentage of CB atoms in the protein-protein interface (based on an 8A° threshold) that are within 6A° of any ligand atom
    * Neighbor bin of motif residues (i.e. number of CA atoms within 8A° of any motif residue CA atom)

Matches that are within the top 20% of all of the above criteria are selected. These metrics primarily filters for ligands
that are buried within the dimer interface.

The following metrics are also calculated, but are not used to throw out matches:

    * Matched binding motif score as determined by Gurobi
    * Number of CB within 2A of ligand
    * Residue match score (i.e. sum of RMSDs between all matched motif residues to corresponding residues in defined motif)
    * Ligand match score (i.e. sum of RMSDs between all pairs of ligand placements from individual motif residues)

The following metrics were implemented by Roland, but are no longer used due to updates in the method:

    * Minimum number of motif residues per chain