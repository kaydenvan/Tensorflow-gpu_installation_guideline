# Instruction on how to enable GPU for Tensorflow

Step 0. Reference Tensorflow documentation to install required software. Software **version** is the key.<br>
https://www.tensorflow.org/install/gpu<br>

Step 1. Download NVIDIA Driver via the link below<br>
At the moment of documentation, version 497 is used.<br>
https://www.nvidia.com/download/index.aspx?lang=en-us<br>

Step 2. Install CUDA (*Option*)<br>
At the moment of documentation, CUDA 11.0 is good enough.<br>
https://developer.nvidia.com/cuda-toolkit<br>

Step 3. Install cuDNN<br>
At the moment of documentation, cuDNN 8.0 is used in corporate with CUDA 11.0<br>
https://developer.nvidia.com/rdp/cudnn-archive#a-collapse810-111<br>

Step 4. Required package<br>
tensorflow-gpu==2.4.0<br>
cudatoolkit==11.0<br>
python==3.7 (or later)<br>

Step 5. Validation<br>
In order to check if GPU is available, the following steps can help.<br>
	open python<br>
	import tensorflow as tf<br>
	tf.config.list_physicla_devices() # GPU will be shown if installation is completed properly<br>
	tf.test.is_built_with_cuda() # see if cuda algorithm is ready or not<br>

Credit: <br>
https://medium.com/analytics-vidhya/install-tensorflow-gpu-2-4-0-with-cuda-11-0-and-cudnn-8-using-anaconda-8c6472c9653f<br>
https://github.com/tensorflow/tensorflow/issues/47147<br>
https://towardsdatascience.com/installing-tensorflow-with-cuda-cudnn-and-gpu-support-on-windows-10-60693e46e781<br>
