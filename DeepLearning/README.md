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