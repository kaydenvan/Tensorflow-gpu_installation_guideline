Instruction on how to enable GPU for Tensorflow

0. Reference Tensorflow documentation to install required software. Software version is the key.
https://www.tensorflow.org/install/gpu

1. Download NVIDIA Driver via the link below
At the moment of documentation, version 497 is used.
https://www.nvidia.com/download/index.aspx?lang=en-us

2. Install CUDA (Option)
At the moment of documentation, CUDA 11.0 is good enough.
https://developer.nvidia.com/cuda-toolkit

3. Install cuDNN
At the moment of documentation, cuDNN 8.0 is used in corporate with CUDA 11.0
https://developer.nvidia.com/rdp/cudnn-archive#a-collapse810-111

4. Required package
tensorflow-gpu==2.4.0
cudatoolkit==11.0
python==3.7 (or later)

5. Validation
In order to check if GPU is available, the following steps can help.
	open python
	import tensorflow as tf
	tf.config.list_physicla_devices() # GPU will be shown if installation is completed properly
	tf.test.is_built_with_cuda() # see if cuda algorithm is ready or not

credit: 
https://medium.com/analytics-vidhya/install-tensorflow-gpu-2-4-0-with-cuda-11-0-and-cudnn-8-using-anaconda-8c6472c9653f
https://github.com/tensorflow/tensorflow/issues/47147
https://towardsdatascience.com/installing-tensorflow-with-cuda-cudnn-and-gpu-support-on-windows-10-60693e46e781