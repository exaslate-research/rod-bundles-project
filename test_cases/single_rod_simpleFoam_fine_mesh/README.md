* Single rod case simulated using simpleFoam solver. Solution converged with the proper meshing but the velocity profile at the wall boundaries can be more accurrate, mesh refining should be done in the wall boundaries of the external domain and around the cylinders.



```sh
foamCleanTutorials
blockMesh
surfaceFeatureExtract
snappyHexMesh -overwrite
touch a.foam
decomposePar
mpirun -np 4 simpleFoam -parallel
```
