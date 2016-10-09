#Setup of DOL
##Description

The distributed operation layer (DOL) is a software development framework to program parallel applications. The DOL allows to specify applications based on the Kahn process network model of computation and features a simulation engine based on SystemC. Moreover, the DOL provides an XML-based specification format to describe the implementation of a parallel application on a multi-processor systems, including binding and mapping.

####DOL Application Programming Interface: 
The DOL defines a set of computation and communication routines that enable the programming of distributed, parallel applications for the SHAPES platform. Using these routines, application programmers can write programs without having detailed knowledge about the underlying architecture. In fact, these routines are subject to further refinement in the hardware dependent software (HdS) layer. 

####DOL Functional Simulation: 
To provide programmers a possibility to test their applications, a functional simulation framework has been developed. Besides functional verification of applications, this framework is used to obtain performance parameters at the application level. 

####DOL Mapping Optimization: 
The goal of the DOL mapping optimization is to compute a set of optimal mappings of an application onto the SHAPES architecture platform. In a first step, XML based specification formats have been defined that allow to describe the application and the architecture at an abstract level. Still, all the information necessary to obtain accurate performance estimates is contained. 




##How to install
###Download the DOL package in your linux OS.
####1.Configure the environment for your ubuntu, apply the following commands:
    sudo apt-get update
    sudo apt-get install ant
    sudo apt-get install openjdk-7-jdk
    sudo apt-get install unzip
####2.Create a new folder and unzip the 'dolethz.zip' and systemc into the folder by applying the following commands.
    mkdir dol
    unzip dol_ethz.zip -d dol
    tar -zxvf systemc-2.3.1.tgz
####3.Compile systemc : enter the dictionary of systemc and use command 'configure' to compile systemc
    cd systemc-2.3.1
    mkdir objdir
	cd objdir
	../configure CXX=g++ --disable-async-updates
    sudo make install
####4.Compile DOL : enter the dictionary of DOL, change the path into the path of systemc
    ant -f build_zip.xml all
    cd build/bin/main
####5.Go to the following path and try the example to evaluate if we have installed DOL successfully
    cd build/bin/main
    ant -f runexample.xml -Dnumber=1



    
##Experimental experience
Linux has a lot of troubles, I spend much time on my 12.0.4 ubuntu but failed, without finding the reason. Out of frustration, I downloaded the newest Linux and applyed the commands in the PPT carefully to achieve the final success.

Linux is a useful OS, and the most convinient part of Linux is that when downloading things, we just need to apply apt-get. Also, I find Github a very useful tool for us to share our code and update. I believe we can learn a lot from the class of embedded system.