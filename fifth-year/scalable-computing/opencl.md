
*(https://github.com/nating/personal-notes/blob/master/fifth-year/scalable-computing/opencl.md)*

# OpenCL

* Modern computing platforms contain one or more CPUs, one or more GPUs, DSP processors, accelerators, and more.

* OpenCL lets programmers write a single portable program that uses ALL resources in the heterogeneous platform.

* Individual processors have many (possibly heterogeneous) cores.

* OpenCL is short for Open Computing Language.

* OpenCL is the emerging intersection between CPU and GPU usage.

## The OpenCL Model

* In the **OpenCL Model** there is one **host** and multiple **OpenCL Devices**.

* Each OpenCL device is made up of one or more **Compute Units**.

* Each Compute Unit is divided into one or more **Processing Elements**.

* Memory is divided into **Host Memory** and **Device Memory**.

* The CPUs of a computer are all considered one OpenCL device, and each GPU is considered its own OpenCL device. One of the CPUs will also have to be its own host.

* One core of a CPU corresponds to one Compute Unit, each of which are considered to have one processing element.

## OpenCL concepts

* The functions executed on an OpenCL device are called **Kernels**.

* The big idea behind OpenCL is to replace loops with kernels (functions) executing at each point in a problem.

* In OpenCL programs, there is an N-dimensional domain of work items. The 'N' has to be chosen to best suit the algorithm.

* A programmer specifies up to 3 dimensions when executing a kernel.

* The total problem size in each dimension is called the **Global Size**.

* Each point in the iteration space is called a **Work Item**.

* Work Items are grouped into **Work Groups**.

* The work items in a work group share local memory and synchronise.

* Memory management in OpenCL is explicit.

* The hierarchy of memory in OpenCL is:
  * Private Memory - per work-item
  * Local Memory - per work-group
  * Global or Constant Memory - visible to all work groups
  * Host Memory - on the CPU

* The **Context** is the environment where kernels execute, and where synchronisation and memory management is defined.

* The context includes one or more devices, device memory, and one or more command queues.

* All commands for a device are submitted through a command queue.

* Each command queue points to a certain device within a context.

* A **Program Object** consists of:
  * A Context
  * The Kernel Source or Binary of a program
  * A List of target devices and build options

* The **Host Program** is the program that runs on the host to set up the environment for the OpenCL program and create and manage kernels.

* The 5 common steps of a host program are:
  1. Define the Platform (devices, contexts, queues)
  2. Create & Build the program
  3. Setup Memory Objects
  4. Define the Kernel
  5. Submit Commands

* There are **In-order** and **Out-of-order** queues which have their commands ran in or out of order.

* A **Buffer** object is a linear collection of bytes.

* An **Image** object defines a two or three dimensional region of memory.

* It is convention to put 'h_' or 'd_' before array variable names to keep track of which are normal host C arrays and which are OpenCL buffers which will live on the device.

...TODO
