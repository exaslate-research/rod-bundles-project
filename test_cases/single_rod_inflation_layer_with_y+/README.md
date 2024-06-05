* This case was made to prepare the model of the single rod with the inflation(gradient mesh) layer of the model and its respecetive outcomes without turbulence models and without including y+


```sh
foamCleanTutorials
blockMesh
surfaceFeatureExtract
snappyHexMesh -overwrite
touch a.foam
decomposePar
mpirun -np 8 simpleFoam -parallel
reconstructPar
```


Additionally, these commands were used to extract the faces which were used to produce the boundary layer (inflaation) mesh 

autoPatch 60 -overwrite
createPatch -dict system/createPatchDict_clean -overwrite
createPatch -dict system/createPatchDict_rename_single -overwrite



After these the boundaries inthe boundary folder in the polyMesh folder will be automatically renamed.
But the boundary conditions in the "p and u" dictionaries in the 0 folder needs to be updated to the respective case



