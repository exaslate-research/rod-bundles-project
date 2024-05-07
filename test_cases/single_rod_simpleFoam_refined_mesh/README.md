* Single rod case with simple foam and changes made to boundary walls to generate refined mesh but the refinement around the rod is not touched.

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
