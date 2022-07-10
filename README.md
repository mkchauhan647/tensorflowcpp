# tensorflowcpp
This is tensorflow cpp compiled source on ubuntu...

#Install and usage 
Just clone the repository and you are good to go... I will provied the include files after structurizing the files.. I don't have 
much knowledged about cmake including files and libs .. I am in middle phase so ... Thank you and enjoy.

If you want to compile yourself then just follow the instructions below..
the instructionos is not clear but I have tried my best to put something that work for you !!!

# Information about the version 

tensorflow version: 2.9.0

bazel version: 5.1.1

ubuntu version : 22.04 LTS

python version: 3.10.4 or 3.10.5 (my 3.10.5) It will work on both perhaps.

# BUILD command used in compiling 
bazel build --local_ram_resources=7000 --jobs=5 tensorflow:tensorflow_cc

Here " --local_ram_resources is used to set the ram for bazel to use and jobs means the number of cpu that can be used to build....
I have not much ram and cpu so I have set according to mine. If you have then you can set your own.

It will take times based on your laptop speicifications... It took 4-5 hours to build in my laptop. Lol it's so frustrating, but lastly it will 
give a goosebumps when everything works fine 


If you have any problem using this repo or compiling then please fill free to open contact me.. or open issues.. Thank you !!!
