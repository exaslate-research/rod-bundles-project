* Single rod case simulated using pisoFoam solver. Solution converged but the velocity profile at the wall boundaries can be more accurrate, mesh refining should be done in the wall boundaries of the external domain




```sh
foamCleanTutorials
blockMesh
surfaceFeatureExtract
snappyHexMesh -overwrite
touch a.foam
decomposePar
mpirun -np 8 pisoFoam -parallel
reconstructPar
```
