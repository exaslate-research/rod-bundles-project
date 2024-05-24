* Single rod case simulated using simpleFoam solver by refining the mesh using "simplegrading" parameter in blockmeshdict. It is not much appropriate. Need to refine the mesh using snappyhexMesh for proper refinement of the mesh.


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
