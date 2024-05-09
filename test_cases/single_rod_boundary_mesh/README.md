* Single rod case with refined boundary mesh at the walls but not near the cylinder. When simulated using simpleFoam solver there are some gaps found in the velocity profile which needs to be fixed by more refinement of meshing.


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
