# ASE-similarity
The ASE measure for node similarity.
This is an instruction on using our softwares for computations related to graph invariants: [t,p]-spectrum and ASE index, where the former was introduced by Ricky Chen while the latter was recently introduced by Ricky Chen and Meng-Ting Wang.

1.  In order for obtaining the spreading power of every vertex,  one has to run the code "SI.exe". 

The inputs to the software are the name of the network and the diffusion rate,  affected time and number of repetitions of SI model.  The network name is usually in the form of "xxx.txt", listing the edges of the network.  The diffusion rate is a double type data between 0 and 1. The affected time determines the number of propagation steps of the SI model,  which is a positive integer greater than 0. The number of repetitions is to ensure the stability of the SI model results,  which is also a positive integer greater than 0.

It generates a series of files called “xxx SIxx_x.txt” based on the input diffusion rate and the affected time, which lists the spreading power of all vertices at a certain diffusion rate at each time t. For example, if the input network name is jazz, the diffusion rate is 0.1, and the affected time is 5, it will generate 5 files named "jazz SI0.1_1.txt", "jazz SI0.1_2.txt",... ... ,"jazz SI0.1_5.txt".

Run the software, first enter the name of the network "xxx",  then enter the diffusion rate, affected time and number of repetitions of SI model.

The vertices are ordered in the same way for all output files.
Please refer to the format of the network used in the paper.


2. The software "compute [t,p]-spe.exe"  produces the [t,p]-spectra of all vertices for  -maxdegree <= t <=0, -maxdegree <= p <=0 written into a single file "xxx tp chain.txt": a row is the [t,p]-spectra of the vertices for fixed t and p. Starting from the first row, these rows are respectively for t=-maxdegree & p=-maxdegree,  t=-maxdegree & p=-maxdegree+1,......, t=-maxdegree & p=0, t=-maxdegree+1 & p=-maxdegree, t=-maxdegree+1 & p=-maxdegree+1,......, t=-maxdegree+1 & p=0,......, t=0 & p=-maxdegree, t=0 & p=-maxdegree+1, ..... ,t=0 & p=0. Vertices are ordered in the same way in all rows.

The input of this software is the file of the interested network "xxx.txt".

Run the software,  just enter  the name of the network "xxx".


3. The software "compute adjacency [t,p]-spe.exe"  produces the adjacency [t,p]-spectra of all vertices for  -maxdegree <= t <=0, -maxdegree <= p <=0 written into a single file "xxx adjacency tp chain.txt": a row is the adjacency [t,p]-spectra of the vertices for fixed t and p, and the rest is the same as  "compute [t,p]-spe.exe". 

The input of this software is the file of the interested network "xxx.txt" and the [t,p]-spectrum of that network "xxx tp chain.txt".

Run the software,  just enter  the name of the network "xxx".


4. The software "compute ASE index.exe" produces similarity matrix of vertices (see the paper for definition)  written into a single file "xxx ASE similarity matrix.txt" and the most similar vertex for each vertex written into a single file "xxx ASE most similar node.txt"

 The input of this software is the adjacency [t,p]-spectrum of network "xxx adjacency tp chain.txt".

Run the software,  just enter  the name of the network "xxx".


Note 1: for the same network, vertices are ordered in the same way in different softwares.
Note 2: if you use our used networks, please also cite the original sources.
