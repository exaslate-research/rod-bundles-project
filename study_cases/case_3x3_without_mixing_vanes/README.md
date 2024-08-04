* Experimental model case simulated using simpleFoam solver. This case is to verify the flow in the rod bundle with spacers and mixing vanes with coarse mesh


```sh
foamCleanTutorials
blockMesh
surfaceFeatureExtract
snappyHexMesh -overwrite
touch a.foam
decomposePar
mpirun -np 32 simpleFoam -parallel
reconstructPar
```



autoPatch 60 -overwrite 
createPatch -dict system/createPatchDict_clean -overwrite


