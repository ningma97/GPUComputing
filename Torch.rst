Torch on ShARC
==============

Torch is a scientific computing framework with wide support for machine learning algorithms that puts GPUs first. It is easy to use and efficient, thanks to an easy and fast scripting language, LuaJIT, and an underlying C/CUDA implementation.

The following is an instruction on how to setup Torch on your local user account.

Request an interactive session e.g. ::

	qrshx -l gpu=1 
	
Load the relevant modules for ShARC ::

	module load apps/python/anaconda3-4.2.0
	module load libs/cudnn/5.1/binary-cuda-8.0.44
	
Create a conda environment to load relevant modules on your local user account and activate it ::

	conda create -n torch python=3.5 anaconda3-2.5.0 
	source activate torch

Install CMake, this is needed to build the Torch binaries ::
	
	conda install cmake

Download Torch distro from github and run the install script ::

	git clone https://github.com/torch/distro.git ~/torch --recursive
	cd ~/torch
	./install.sh
