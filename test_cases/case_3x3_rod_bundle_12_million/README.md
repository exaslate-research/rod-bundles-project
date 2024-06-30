* Experimental model 3x3 case simulated using simpleFoam solver. This case was simulated using RNG K-Epsilon model for grid study. 12 million cells were used for this study.


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


