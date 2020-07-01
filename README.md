# LinkTest

As part of acceptance testing, we require the LinkTest program from Jülich Supercomputing Centre (JSC) to be run. LinkTest is a parallel ping-pong test between all possible MPI connections within a cluster, outputting a communication matrix showing bandwiths and latency between all nodes. It is available from

https://www.fz-juelich.de/ias/jsc/EN/Expertise/Support/Software/LinkTest/_node.html

As with HPL, we will run LinkTest twice:

- compiled using the Intel compile and Intel MPI (version 2019.1 and 2019.6, respectively)
- compiled using gcc and OpenMPI 3.1.4

LinkTest command linke used will be 

     mpilinktest -i 60 -I 16 -k 4096 -S 1 

The results will be used to confirm that communication, especially within the islands, is of uniform latency and acceptable latency and bandwidth.
