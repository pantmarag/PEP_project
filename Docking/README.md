 # Docking process

Molecular docking is an established computational structure-based method used in drug discovery. It allows the identification of potential drug targets and predicting molecular ligand-target interactions at the atomic level. In this project we used the [AutodockVina](https://vina.scripps.edu/manual/) for as a docking scoring function. Because docking score does not provide a usefull information about the ligand-protein interaction, we did not rely on the score. The important output of the docking procedure in general, is the conformation of the ligand in the binding site. A proper conformation of the ligand in the binding site, can actually indicates a potential inhibition to the given target(Thrombin). Proper conformation means that the compound that we need to test conform all the crucial interactions with the key amino acids of the binding site.

For this project, we investigate the thrombin target and we were asked to find a potential new thrombin inhibitor. We took the [5AFZ](https://vina.scripps.edu/manual/) entry and we investigate the crucial interaction of the UET, the ligand that inhibits thrombin. We set this ligand as a control compound. The most crucial interactions were the above:

Hydrophobic interactions:

- VAL 213

Hydorgen Bonds:

- ASP 189
- SER 214
- GLY 216
- GLY 219

From the database that we created we took the compounds with the best IC50 values. Our mission was to adjust those compounds so as to gain more crucial interactions. Compared with the control compound, we docked three of them, 4 docking pose each.

The first compound with the best exparimantal data value, was aligned perfectly with the control compound. This might be a good indication for the proper docking pose. 

The second compound of our list was docked later on. Again the first docking pose was aligned perfectly with the control compound.

Later, we tried to enhance the given structures so as to gain more interaction and probably increase the affinity. We wanted to add some reasonable adjustments that can easily been synthesized by the chemists in the wet lab. The amino imino group which was presenting in the control compound was missing for the molecule which has the best IC50 value. So we implement this group to the benzene ring that was available. We wanted to gain the ASP 189 interaction. After the docking, we took 4 different poses. The third one had the conformation that we wanted. The docking score was the lowest but this is just a prediction. We considered not to rely on docking score but only on the conformation which is crucial in this step of drug discovery. Later, using Molecular Dynamics and Free Energy Perturbation we can asses the docking poses.

We gave a name to this compound, PEP1:

