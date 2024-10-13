* Serial
    ```sh
    blockMesh
    surfaceFeatureExtract
    snappyHexMesh -overwrite
    icoFoam
    ```
* Parallel
    ```sh
    foamCleanTutorials
    blockMesh
    surfaceFeatureExtract
    snappyHexMesh -overwrite
    touch a.foam
    decomposePar
    mpirun -np 4 simpleFoam -parallel
    reconstructPar
    ```
    
surfaceTransformPoints -scale '(0.001 0.001 0.001)' wing.obj wing1.obj
