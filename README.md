# Termux-LWJGL-Build

A set of modified prebuilt lwjgl snapshot jar for Termux on Android,especially for launching minecraft
This ver is compiled by clang and openjdk-21 in termux

## Tutorial for launching minecraft on termux native

First,install related packages(such as openjdk),especially a x server(eg. termux-x11) and graphic apis(for example,mesa for opengl),or you can use native vulkan by vulkanmod

Second,find a command line launcher(such as cmcl or portablemc) to install most minecraft libs(jars without natives run well on termux),add jvmArgs -Djna.boot.library.path=\<directory of your libjnidispatch \>,you can find libjnidispatch in jna/your version here,also add -Djava.library.path=$PREFIX/lib

Third,substitute all lwjgl jars to correct version of lwjgl here,including jars combined in the vulkan mod(remember version)

Then,launch x and launch minecraft

In addition,you can compile and install flite to $PREFIX to get text2speech experience
