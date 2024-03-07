# tema1, Vincentiu Tarsoaga, 334Ca

*Tema 1 APD*

    Tema 1 este despre eficientizarea unui program dat, folosind threaduri. Am 
primit implementarea secventiala a algoritmului Marching Squares, pentru
care a trebuit sa paralelizez functii, pentru a optine timpi de executie mai
buni, folosind 2 si 4 threaduri.

*Modificari:*
-Toate alocarile de memorie au loc in main, deoarece toate threadurile folosesc
zone comune de memorie
-Pentru a retine matricelepe care le modificam in program, am creeat o structura,
care pentru fiecare thread retine id-ul, numarul total de threaduri, imaginea initiala, 
imaginea actualizata, gridul si contour map-ul
-Pentru a sincroniza threadurile, am folosit o bariera, care este retinuta si ea in 
structura data ca parametru. 

*Functiile paralelizate*
-sample_grid
-march
-rescale_image

Fiecare thread primeste o memorie delimitata de parametrii start si end. Bariera este 
plasata la sfarsitul fiecare functii paralelizate, pentru a asigura sincronizarea 
threadurilor.