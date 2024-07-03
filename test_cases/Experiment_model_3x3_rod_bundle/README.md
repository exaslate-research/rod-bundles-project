* Experimental model 3x3 case simulated using simpleFoam solver. This case was simulate the outcomes for a initial case



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



autoPatch 60 -overwrite 
createPatch -dict system/createPatchDict_clean -overwrite


