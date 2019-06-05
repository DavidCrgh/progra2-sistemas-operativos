Instrucciones:

1. Compilar con
        module load openmpi/4.0.1
        [PATH A OPENMPI/4.0.1]/mpicc LCS_mpi.c -o LCS_mpi

2. Crear archivo PBS, debe incluir las lineas:

        module load openmpi/4.0.1

   esta debe ir depues de todas las lineas #PBS y antes de
   la linea que corre el programa.

        mpirun LCS_mpi tests/[TAMANO]_test1.txt tests/[TAMANO]_test2.txt

3. Mandar a ejecutar el job:

    qsub [ARCHIVO PBS].pbs