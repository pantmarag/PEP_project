# [Course: Advanced Computational Methods in Drug Discovery by Jespers Willem](https://studiegids.universiteitleiden.nl/en/courses/115512/advanced-computational-methods-in-drug-discovery-ai-and-physics-based-simulations) 
# Report for the course Advanced Computational Methods in Drug Discovery. Given target: Thrombin 


![This is an image](https://www.jbc.org/cms/attachment/d1e34430-71a7-4cf6-93b6-d12d26e20697/gr1.jpg)

This repositry contains the whole project of the programming assignment for the [Advanced Computational Methods in Drug Discovery course](https://studiegids.universiteitleiden.nl/en/courses/115512/advanced-computational-methods-in-drug-discovery-ai-and-physics-based-simulations) taught by Assistant Professor Jespers Willem. The contibutors of the project is Pantelis Maragkoudakis Panagiotis Dimitropoulos and Ehsan Aslam.
Computer-aided drug design (CADD) comprises a broad range of theoretical and computational approaches that are part of modern drug discovery. CADD methods have made key contributions to the development of drugs that are in clinical use or in clinical trials. Such methods have emerged and evolved along with experimental approaches used in drug design. In this project  we will use some of the main advances in the field, such as Machine Learning prediction models, Docking, Interaction Fingerprints and generation of a Database of all the known inhibitors for the given target. The main aim of the project is to generate new potential selective inhibitors for the human Thrombin, by taking into consideration all the output of the Machine Learning Models and the steps of the Drug Discovery process. Our goal is to generate a set of ligands that are orientated in the binding pocket identical or even better compared with well known already synthesized in the lab compounds. Furthermore, we focus not only on the scores but also on the retrosynthesis path of the compounds. Our number one priority is to generate compounds that can be actually made in the wet lab.

For this project we used:
- The well known [Jupyter Notebook](http://jupyter-notebook-beginner-guide.readthedocs.io/en/latest/what_is_jupyter.html), which provides an intuitive flow.
- A good amount of the scripts were obtained by the [TeachOpenCADD](https://github.com/volkamerlab/teachopencadd),an open source programming packages for cheminformatics and structural bioinformatics are powerful tools to build modular, reproducible, and reusable pipelines for computer-aided drug design (CADD). Programming language `python`.
- We also used scripts for the CBR-teaching, an environment that was made by Willem Jespers for the aim of this course. Programming language `python`.
- For the Interaction Fingerprints we use the [Open Drug Discovery Toolkit](https://github.com/oddt/oddt),a  modular and comprehensive toolkit for use in cheminformatics, molecular modeling etc. ODDT is written in `python`, and make extensive use of Numpy/Scipy
- The re-written code is now embedded within the Jupyter Notebook . Especially we used the Noteable environment.


## Thrombin: Target discription 

### Protein information
Thrombin is a multifunctional serine protease (peptidase S1 family) that is known to be the central protease of the human blood coagulation cascade and is located extracellularly. (F2 - Prothrombin - Homo sapiens (Human) | UniProtKB | UniProt, z.d.) In this coagulation cascade, Prothrombin (coagulation factor II) is proteolytically cleaved to form thrombin. Next, soluble fibrinogen is formed into insoluble strands of fibrin by serine acting thrombin to form fibrin cloths in injured cells. Similarly, thrombin has a positive regulatory effects on coagulation factors and induces procoagulant, inflammatory, cellular proliferation and anticoagulant mechanism in the body. (Al-Amer, 2022) 

### Pathogenesis 
In the case of deregulation of thrombin in the blood coagulation cascade, abnormalities can occur which range from minor subclinical to serious life-threatening coagulopathies, i.e., during septicemia. (Danckwardt et al., 2013) Thrombin is multifunction and is not limited to only coagulator functions. Thrombin is involved in the innate and adaptive immune system and directs platelets, endothelial cells and various effector cells of the immune system which if deregulated can lead to sepsis. (Rittirsch et al., 2008) In both acute and chronic inflammation processes thrombin activates the complement cascade, or functions as a mitogen for immune effector cells. (Coughlin, 2000) When deregulated, abnormal platelet mediated thrombin upregulation can lead to excessive blood clotting and thrombosis.(Sambrano et al., 2001) 
Haemostasis plays an inherent part in the physiological regeneration processes, which are also engaged during tumorigenesis. (Dvorak, 2015) Thrombin and fibrin synthesis is directly activated by coagulator substances produced by tumour cells and/or indirectly via the activation of endothelial cells, thrombocytes, and leukocytes which produce cytokines, proteases, glycoproteins, and tissue factor-loaded microparticles. (Cancer, Clots and Consensus: New Understanding of an Old Problem - PMC, z.d.) This will eventually create a pro-tumorigenic micromilieu, driving drives cellular programs promoting cell growth, motility, angiogenesis, and invasiveness in tumours. (Nierodzik & Karpatkin, 2006)
As illustrated, thrombin is a multifaceted protein involved in many physiological processes and can negatively influence health when deregulates as these processes turn into pathophysiological conditions. This makes thrombin an ideal drug-target as an effective drug that regulates thrombin can be applied in many thrombin-related diseases and makes the drug highly impactful in the clinic. 

### Current drugs
Currently three classes of “Direct thrombin inhibitors” (DTIs) are available which act as anti-coagulants, directly inhibiting the enzymatic function of thrombin. (Sidhu et al., 2013) The three classes are, bivalent, univalent and allosteric inhibitors. The bivalent inhibitor mainly consists of large peptide molecules such as hirudin (Kim et al., 2008) and bivalirudin (Wakui et al., 2019). Univalent inhibitors involve small molecule inhibitors such as melagatran (Di Nisio et al., 2005) and inogatran (Kam et al., 2005) which share remarkable similarities with our newly designed ligand PEP1/2 in molecular structure, chemical groups, and size. 
As thrombin shows great levels of allosteric regulation, there is a growing interest in developing allosteric inhibitors for thrombin as it can function as a regulator instead of merely an inhibitor. Although advancements have been made with candidates such as sulfated pentagalloylglucopyranoside (SPGG)(Al-Horani & Desai, 2014), an allosteric inhibitor has yet to entered the clinic. 

### Active site
Thrombin’s active site is composed of a catalytic triad (Ser195, His57, and Asp102) of three pockets, each with their own characteristics and roles. As illustrated in diagram below, the three pockets are S1, S2 and S3/4. The S1 pocket is a basic-recognition site with Asp189 as the most important residue. The S2 pocket is a proximal hydrophobic pocket with Tyr60A and Trp60D as the main residues. The S3/4 pocket is lipophilic distal pocket mainly made of resides Leu 99, Ile174, and Trp215. (He et al., 2015)
These pockets are considered in the design of many strong and selective thrombin inhibitors including our designed thrombin ligands (PEP1/2). Our design emphasised binding with the S1 recognitions site as the entry we used (5AFZ) has a ligand (UET) in its crystallised structure which binds in the S1 pocket. We used the UET ligand as a base to reinvent a similar structured but improved ligand. 

<img width="394" alt="image" src="https://user-images.githubusercontent.com/117588718/200306380-7b14d10a-d0aa-4e4f-b599-16398e79c73c.png"> 
Figure: showing a three-dimensional representation of the thrombin active with a binded inhibitor and annotated binding pockets. (Rühmann et al., 2015)

### Discussion 
Our research consisted of three stages in which we first performed bioinformatics analysis on the selected entry 5AFZ to confirm the correct alignment of our protein structure, active site of the protein and to assess what ligands show good binding affinity with the binding S1 binding pocket. Next, we performed machine learning (ML) driven analysis to virtually screen compounds based on IC50 values and selected the best performing compounds. We assessed the best compounds and manually designed a ligand taking inspiration from chemical groups which showed high levels of interaction with the S1 binding pocket. Finally, we performed docking analysis on our designed ligands and compared the results with the four existing ligands based IC50 values including the UET ligand. In this comparison the emphasis was placed on docking poses instead of binding affinity values as these values are predictions and exclude the actual pose of a ligand which is more relevant when considering the actual fitting of a ligand in a binding site. Multiple re-evaluations of the docking poses resulted in two designed ligands: PEP1 and PEP2, that showed a greater docking pose-orientation compared to the four ligands which scored higher on affinity values. 

 
When trying our initial entry choice 2ZFF, problems occurred in ligand coordination which could not be fixed in the short working period. For this reason, we opted for a new but highly similar entry 5AFZ which also aligned perfectly with the initial entry choice. An explanation for the bad ligand orientation could be limitation in the code or wrong initial coordinates of the ligand which might be out of order. However, the 5AFZ showed none of the problems and we continued using this entry. 

 
Although we designed two ligands which show promising results in docking poses, this is not sufficient to continue research the potential of these ligands. Time has been a limiting factor which did not allow for a comprehensive assessment of the designed compounds. We wanted to try out the De novo generation, but because of complications and limited time, we were unable to perform De Novo Generation. The same things apply to Interaction Fingerprints and Free Energy Perturbation. Besides the lack of analysis approaches and the inherent limitations of validation the docking poses, there is bias present in the docking algorithm as we only used one algorithm. Future prospect would thus include more diversified analysis approaches and methods of validations which were firstly lacking. Also, the addition of molecular dynamics simulations will greatly increase our understanding of the interactions the ligands would have. Once the ligands are validated to be highly potent in binding and potentially inhibiting thrombin, AI driven retrosynthesis pathway generation can be applied to observed whether it is feasible to synthesis the ligands in a real-world experimental setting.


### Bibliography 
- Al-Amer, O. M. (2022). The role of thrombin in haemostasis. Blood Coagulation & Fibrinolysis, 33(3), 145–148. https://doi.org/10.1097/MBC.0000000000001130
- Al-Horani, R. A., & Desai, U. R. (2014). Designing Allosteric Inhibitors of Factor XIa. Lessons from the Interactions of Sulfated Pentagalloylglucopyranosides. Journal of Medicinal Chemistry, 57(11), 4805–4818. https://doi.org/10.1021/jm500311e
- Cancer, Clots and Consensus: New Understanding of an Old Problem—PMC. (z.d.). Geraadpleegd 1 november 2022, van https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2764390/
- Coughlin, S. R. (2000). Thrombin signalling and protease-activated receptors. Nature, 407(6801), Art. 6801. https://doi.org/10.1038/35025229
- Danckwardt, S., Hentze, M. W., & Kulozik, A. E. (2013). Pathologies at the nexus of blood coagulation and inflammation: Thrombin in hemostasis, cancer, and beyond. Journal of Molecular Medicine, 91(11), 1257–1271. https://doi.org/10.1007/s00109-013-1074-5
- Di Nisio, M., Middeldorp, S., & Büller, H. R. (2005). Direct thrombin inhibitors. The New England Journal of Medicine, 353(10), 1028–1040. https://doi.org/10.1056/NEJMra044440
- Dvorak, H. F. (2015). Tumors: Wounds That Do Not Heal—Redux. Cancer Immunology Research, 3(1), 1–11. https://doi.org/10.1158/2326-6066.CIR-14-0209
- F2—Prothrombin—Homo sapiens (Human) | UniProtKB | UniProt. (z.d.). Geraadpleegd 1 november 2022, van https://www.uniprot.org/uniprotkb/P00734/entry#family_and_domains
- He, L.-W., Dai, W.-C., & Li, N.-G. (2015). Development of Orally Active Thrombin Inhibitors for the Treatment of Thrombotic Disorder Diseases. Molecules, 20(6), 11046–11062. https://doi.org/10.3390/molecules200611046
- Kam, P. C. A., Kaur, N., & Thong, C. L. (2005). Direct thrombin inhibitors: Pharmacology and clinical relevance. Anaesthesia, 60(6), 565–574. https://doi.org/10.1111/j.1365-2044.2005.04192.x
- Kim, Y., Cao, Z., & Tan, W. (2008). Molecular assembly for high-performance bivalent nucleic acid inhibitor. Proceedings of the National Academy of Sciences, 105(15), 5664–5669. https://doi.org/10.1073/pnas.0711803105
- Nierodzik, M. L., & Karpatkin, S. (2006). Thrombin induces tumor growth, metastasis, and angiogenesis: Evidence for a thrombin-regulated dormant tumor phenotype. Cancer Cell, 10(5), 355–362. https://doi.org/10.1016/j.ccr.2006.10.002
- Rittirsch, D., Flierl, M. A., & Ward, P. A. (2008). Harmful molecular mechanisms in sepsis. Nature Reviews Immunology, 8(10), Art. 10. https://doi.org/10.1038/nri2402
- Rühmann, E., Betz, M., Heine, A., & Klebe, G. (2015). Fragment Binding Can Be Either More Enthalpy-Driven or Entropy-Driven: Crystal Structures and Residual Hydration Patterns Suggest Why. Journal of Medicinal Chemistry, 58(17), 6960–6971. https://doi.org/10.1021/acs.jmedchem.5b00812
- Sambrano, G., Weiss, E., Zheng, Y.-W., Huang, W., & Coughlin, S. (2001). Sambrano, G.R., Weiss, E.J., Zheng, Y.-W., Huang, W. & Coughlin, S.R. Role of thrombin signalling in platelets in haemostasis and thrombosis. Nature 413, 74-78. Nature, 413, 74–78. https://doi.org/10.1038/35092573
- Sidhu, P. S., Abdel Aziz, M. H., Sarkar, A., Mehta, A. Y., Zhou, Q., & Desai, U. R. (2013). Designing Allosteric Regulators of Thrombin. Exosite 2 Features Multiple Sub-Sites That Can Be Targeted By Sulfated Small Molecules for Inducing Inhibition. Journal of medicinal chemistry, 56(12), 5059–5070. https://doi.org/10.1021/jm400369q
- Wakui, M., Fujimori, Y., Nakamura, S., Kondo, Y., Kuroda, Y., Oka, S., Nakagawa, T., Katagiri, H., & Murata, M. (2019). Distinct features of bivalent direct thrombin inhibitors, hirudin and bivalirudin, revealed by clot waveform analysis and enzyme kinetics in coagulation assays. Journal of Clinical Pathology, 72(12), 817–824. https://doi.org/10.1136/jclinpath-2019-205922
