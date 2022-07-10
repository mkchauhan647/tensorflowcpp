# tensorflowcpp

<b>Compiling tensorflow c++ for ubuntu</b>

<b>tensorflow c++ compile from source on ubuntu , linux.</b>

This is tensorflow cpp compiled source on ubuntu...

# Install and usage 

Just clone the repository and you are good to go... <br>
There is some examples that help you to understand the include and lib files of tensorflow. <br>
I will provied the include files after structurizing the files.. I don't have 
much knowledged about cmake including files and libs .. I am in middle phase so ... <br>Thank you and enjoy.

If you want to compile yourself then just follow the instructions below..
the instructionos is not clear but I have tried my best to put something that work for you !!!

# Information about the version 

tensorflow version: 2.9.0

bazel version: 5.1.1

ubuntu version : 22.04 LTS

python version: 3.10.4 or 3.10.5 (my 3.10.5) It will work on both perhaps.

# BUILD command used in compiling 

1. First clone the repository of tensorflow from https://github.com/tensorflow/tensorflow
2. Install the bazel from https://bazel.build/install/ubuntu and choose the version as above i.e 5.1.1
3. run the configure as " python configure.py " just hit enter nothing to do.. unless you want cuda, cudann graphic something like that.. 
4.  Just run the command for .so files <b>bazel build --local_ram_resources=7000 --jobs=5 tensorflow:tensorflow_cc</b>
5.  and for headers run <b> bazel build tensorflow:install_headers<b>

Here " --local_ram_resources is used to set the ram for bazel to use and jobs means the number of cpu that can be used to build....
I have not much ram and cpu so I have set according to mine. If you have then you can set your own.

It will take times based on your laptop speicifications... It took 4-5 hours to build in my laptop. Lol it's so frustrating, but lastly it will 
give a goosebumps when everything works fine 

After finished the build just copy the include and lib files in separate folder and place it properly to use efficiently because it's hard to organize the 
 include and lib files .. It's huge so.. be aware of this.
 
 Include and the lib files is located in bazel-bin folder goto bazel-bin/tensorflow and you will find .so files like libtensorflow_cc.so , libtensorflow_framework.so and a include folder containing all the required header files.
 

If you have any problem using this repo or compiling then please fill free to open contact me.. or open issues.. Thank you !!!
