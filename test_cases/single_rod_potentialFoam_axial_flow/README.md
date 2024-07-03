* Single rod case simulated using simpleFoam solver. This case is for studying the effect of potentialFoam through the passing the flow parallel to the rod



```sh
blockMesh
surfaceFeatureExtract
snappyHexMesh -overwrite
decomposePar
mpirun -np 4 simpleFoam -parallel
```
