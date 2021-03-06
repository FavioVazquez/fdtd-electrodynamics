# FDTD - Electrodynamics

Simple FDTD client for electrodynamics purposes.

# Compilation process

Below is the process to install required dependancies and compilation process. Now is only for Linux, tested on Ubuntu 14.04 LTS and 16.04 LTS. 

## Required libraries 

### [Allegro](http://liballeg.org/)

Allegro is a cross-platform library mainly aimed at video game and multimedia programming. It handles common, low-level tasks such as creating windows, accepting user input, loading data, drawing images, playing sounds, etc. and generally abstracting away the underlying platform.

To install the stable branch (5.2) run this command in your terminal:

```
sudo add-apt-repository ppa:allegro/5.2
```

Now, run these commands to install the development versions of Allegro:

```
sudo apt-get update
sudo apt-get install liballegro5-dev
```

### [GSL](https://www.gnu.org/software/gsl/)

The GNU Scientific Library (GSL) is a numerical library for C and C++ programmers. It is free software under the GNU General Public License.

The library provides a wide range of mathematical routines such as random number generators, special functions and least-squares fitting. There are over 1000 functions in total with an extensive test suite.

To install this library in ubuntu 14.04 run:

```
apt-get install gsl-bin
sudo apt-get install libgsl0ldbl
```

In 16.04 they have erased *libgsl0ldbl* so you will have to install the development version:

```
apt-get install gsl-bin
sudo apt-get install libgsl0-dev
```

The resources/docs can also be installed using: 

```
sudo apt-get install gsl-doc-info gsl-doc-pdf gsl-ref-html gsl-ref-psdoc
```

## Compilation Process 

### The basics.

If you don't have C++ compilers you will have to install them. Normaly Ubuntu comes with this compilers but if you don't have them, run this commands:

```
sudo add-apt-repository ppa:ubuntu-toolchain-r/test
sudo apt-get update
sudo apt-get install gcc-5 g++-5
```

### Compile using CLion

This compilation will be done using [CLion](https://www.jetbrains.com/clion/). In the future we will add more compilation ways, but for now, we recommend compiling with this method. It is easy, fast and bulletproof (if you follow the steps with care). 

CLion is a cross-platform IDE for C and C++. Thanks to native C and C++ support, including C++11 standard, libc++ and Boost, CLion knows your code through and through and takes care of the routine while you focus on the important things. Be sure to check the [web page](https://www.jetbrains.com/clion/) for the documentation and installation process. 

Although it is a subscription based IDE, they have discounts for startups, graduating studentds and competitive tool users, and free subscriptions for students, teachers, education, training, and open source projects. Check this [web page](https://www.jetbrains.com/clion/buy/#edition=discounts) for more information.

After you have succesfully installed everything to this point, is time to start the compilation process. The images could change depending on the version of CLion you are using. 

- Clone this repository

```
git clone https://github.com/FavioVazquez/fdtd-electrodynamics.git
```

- Open CLion

- Click Open Project

![1](https://github.com/FavioVazquez/fdtd-electrodynamics/blob/master/compImages/1.png)

- CLion will automatically detect the CMake files and will start building the program for you. No errors should ocurr at this stage, be sure to check the bundled CMake console in CLion for warnings and erros. 

- CLion will create a configuration file (src/config.h), this file has all the configuration needed to build and execute the code. Check it but before making any change see the heading of the file:

```C++
/*--------------------------------------------------------------------------
 * This file is autogenerated from config.h.in 
 * during the cmake configuration of your project. If you need to make changes
 * edit the modules/config.in.h file NOT THIS FILE.
 * --------------------------------------------------------------------------*/
```

- If everything worked you should be able to run the examples we have built for you. For example for runing the simlations of electromagnetic waves using FDTD do this: 

Select fdtd:

![2](https://github.com/FavioVazquez/fdtd-electrodynamics/blob/master/compImages/2.png)

Run the program:

![3](https://github.com/FavioVazquez/fdtd-electrodynamics/blob/master/compImages/3.png)

## PML (TBA)







