* Single rod case simulated using simpleFoam solver. This case was made to study the mesh of the model and its respecetive outcomes without turbulence models


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



