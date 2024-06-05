* Experimental model case simulated using simpleFoam solver. This case was made to obtain the y+ values of the boundary layer mesh to create a more appropriate mesh for the case


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


