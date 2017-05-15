# Deeplearning config: makefiles, configs etc

## Theano

[.theanorc](https://github.com/tdeboissiere/Configs/blob/master/DeepLearning/.theanorc)

## Caffe

[Caffe makefile](https://github.com/tdeboissiere/Configs/blob/master/DeepLearning/caffe_Makefile.config)

## MXNET

[MXNET makefile](https://github.com/tdeboissiere/Configs/blob/master/DeepLearning/mxnet_Makefile)

## Tensorflow

To compile with additional flags:

	bazel build -c opt --copt=-mavx --copt=-mavx2 --copt=-mfma --copt=-mfpmath=both --copt=-msse4.2 --config=cuda -k //tensorflow/tools/pip_package:build_pip_package
	
## Error message with nvidia kernels when using apt get :

Error:

	Processing triggers for libc-bin (2.23-0ubuntu7) ...
	/sbin/ldconfig.real: /usr/lib/nvidia-375/libEGL.so.1 is not a symbolic link
	/sbin/ldconfig.real: /usr/lib32/nvidia-375/libEGL.so.1 is not a symbolic link



Fix: 

	sudo mv /usr/lib/nvidia-375/libEGL.so.1 /usr/lib/nvidia-375/libEGL.so.1.org
	sudo mv /usr/lib32/nvidia-375/libEGL.so.1 /usr/lib32/nvidia-375/libEGL.so.1.org
	sudo ln -s /usr/lib/nvidia-375/libEGL.so.375.39 /usr/lib/nvidia-375/libEGL.so.1
	sudo ln -s /usr/lib32/nvidia-375/libEGL.so.375.39 /usr/lib32/nvidia-375/libEGL.so.1
