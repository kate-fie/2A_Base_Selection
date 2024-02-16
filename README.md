# 2A_Base_Selection

Bases for eyeballing and subsequent Syndirella elaboration performed on three input datasets:

1. [Matteo's ROCS iteration2](https://github.com/matteoferla/EV-A71-2A-elaborations)
2. [Josh's FEGrow iteration2](https://github.com/jthorton/EV-A71-2A-elaborations)
3. [Max's Fragmenstein pipeline run](https://github.com/mwinokan/2A_Fragmenstein)

Each dataset was reduced to <120 designs using the following respective strategies

1. best 120 free energies
2. best 20 predicted affinity with #protein clash < 9 per series (skipping x0365 and x1019)
3. see [here](https://github.com/mwinokan/2A_Fragmenstein/blob/main/README.md#filtering-view_outputsipynb)https://github.com/mwinokan/2A_Fragmenstein/blob/main/README.md#filtering-view_outputsipynb

For 1. & 2. refer to [combine_wave2.ipynb](https://github.com/mwinokan/2A_Base_Selection/blob/main/combine_wave2.ipynb)

Fragalysis ready SDF's can be found here:

1. [ROCS](https://github.com/mwinokan/2A_Base_Selection/blob/main/filtered_2A_iter2_ROCS_fragalysis.sdf)
2. [FEGrow](https://github.com/mwinokan/2A_Base_Selection/blob/main/filtered_2A_iter2_fegrow_top120_fragalysis.sdf)
3. [Fragmenstein](https://github.com/mwinokan/2A_Base_Selection/blob/main/filtered_2A_iter2_MW_Fragmenstein_fragalysis.sdf)

## KATE'S NOTES

1. ROCS:
   - Many are pretty interesting (stay close to fragment inspiration)
   - Some are large with many rings
   - Some never go near the catalytic site and instead are only in P3 + P5
   - I've selected compounds that are not too large to begin with (while keeping some large ones)
2. FEGrow:
   - Once again, many are interesting
   - Lots of large compounds with many rings
   - I tried to select only smaller compounds (choose very few (if any) with many rings)
3. Fragmenstein:
   - Overall much smaller/noodly
   - Important note:
     - Many of the compounds have a inspiration fragment of `A71x0922a` which has a benzene ring but in the <br />  `.sdf` it is a cyclohexane. So if elaborating them, the SMILES should be adjusted to reflect this.