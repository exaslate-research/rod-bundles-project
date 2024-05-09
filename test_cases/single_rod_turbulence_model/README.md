* Single rod case simulated including the K-Epsilon turbulence model using simpleFoam solver, the solution is converged but there is a small gap in the velocity profile. Need to find the cause in the meshing and resolve it to obtain a continous velocity profile.


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


  
