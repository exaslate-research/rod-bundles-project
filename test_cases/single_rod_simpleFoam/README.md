* Single rod case simulated using simpleFoam solver. Solution did not converge due to improper meshing around the rods and walls. This case was simulated without any refinements and with an improper mesh.



```sh
blockMesh
surfaceFeatureExtract
snappyHexMesh -overwrite
decomposePar
mpirun -np 4 simpleFoam -parallel
```
