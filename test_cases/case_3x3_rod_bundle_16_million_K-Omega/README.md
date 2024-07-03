* Experimental model 3x3 case simulated using simpleFoam solver. This case was simulated using K-Omega SST model for turbulence model comparative study. 16 million cells were used for this study.


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


