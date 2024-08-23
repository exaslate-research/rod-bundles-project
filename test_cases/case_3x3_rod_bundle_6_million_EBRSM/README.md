* Experimental model 3x3 case simulated using simpleFoam solver. This case was simulated using EBRSM model for the comparative study of turbuelence models. 6 million cells were used for this study due to computational power.


```sh
foamCleanTutorials
blockMesh
surfaceFeatureExtract
snappyHexMesh -overwrite
touch a.foam
decomposePar
mpirun -np 10 simpleFoam -parallel
reconstructPar
```



autoPatch 60 -overwrite 
createPatch -dict system/createPatchDict_clean -overwrite


