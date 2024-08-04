* Single rod case simulated using simpleFoam solver. This case is for studying the effect of potentialFoam through the passing the flow past to the rod



```sh
foamCleanTutorials
blockMesh
surfaceFeatureExtract
snappyHexMesh -overwrite
touch a.foam
decomposePar
mpirun -np 8 potentialFoam -parallel
mpirun -np 8 simpleFoam -parallel
reconstructPar
```
