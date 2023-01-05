# AlexNet-TensorFlow-with-Weights

<!-- 
1. Visual Studio 2015,2017,2019, and 2022 https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-150
2. Cuda 11.3.1 https://developer.nvidia.com/cuda-11-3-1-download-archive?target_os=Windows&target_arch=x86_64&target_version=10&target_type=exe_local
3. TF 2.10 en anaconda: 
 conda install –c conda-forge cudatoolkit=11.2 cudnn=8.1.0
 pip install tensorflow

Los pesos y la arquitectura se basan de:
https://www.cs.toronto.edu/~guerzhoy/tf_alexnet/

Los pesos estan disponibles en:
https://www.cs.toronto.edu/~guerzhoy/tf_alexnet/bvlc_alexnet.npy

La arquitectura esta disponible en:
https://www.cs.toronto.edu/~guerzhoy/tf_alexnet/myalexnet_forward_newtf.py

Imagenes de ImageNet
https://www.kaggle.com/competitions/imagenet-object-localization-challenge/data

Artículo de AlexNet
https://proceedings.neurips.cc/paper/2012/file/c399862d3b9d6b76c8436e924a68c45b-Paper.pdf
GETTING STARTED -->

<!-- GETTING STARTED -->
## Getting Started

Since 2012, <a href="https://proceedings.neurips.cc/paper/2012/file/c399862d3b9d6b76c8436e924a68c45b-Paper.pdf">AlexNet</a> is one of the most used architectures in Deep Learning for image classification. This model was trained using <a href="https://www.kaggle.com/competitions/imagenet-object-localization-challenge/data
">ImageNet</a> dataset. The pretrained-AlexNet model can be found in <a href="https://pytorch.org/hub/pytorch_vision_alexnet/">PyTorch</a>, however, it doesn´t exist a guide for Tensorflow implementation. Therefore, this repo include a guide for that purpose.

To generate our pretrained-AlexNet for Keras/TensorFlow, we used the weights found <a href="https://www.cs.toronto.edu/~guerzhoy/tf_alexnet/">here</a> and can be downloaded from <a href="https://www.cs.toronto.edu/~guerzhoy/tf_alexnet/bvlc_alexnet.npy">here</a>. Nonetheless, to implement this version of pretrained-AlexNet you have to load the whole architecture and assign the weights to each layer. Thus, for a cleaner implementation of the pretrained-AlexNet model we proposed this repo with the pretrained-AlexNet model in .h5 format.

We tested our pretrained-AlexNet using Anaconda (2.3.1) and Spyder (5.2.2 and 5.3.3) with the next dependencies on Windows 10 in a NVIDIA GeForce RTX 3060 GPU and NVIDIA GeForce RTX 2070 Super. 

### Installation

1. Install <a href="https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-150">Visual Studio 2015,2017,2019, and 2022.</a> 
2. Install <a href="https://developer.nvidia.com/cuda-11-3-1-download-archive?target_os=Windows&target_arch=x86_64&target_version=10&target_type=exe_local">CUDA 11.3.1.</a> This step is crucial because AlexNet arquitecture was designed with the delineation of responsabilities between two GPUs. Nevertheless, by explicit installing CUDA it allows to implement AlexNet using just one GPU.
3. Create a new environment in Anaconda.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;a) Go to "Environments" in Anaconda Navigator.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;b) Go to "Create".

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;c) In the appering window assign a name for your new environment, select Python package 3.7.13, and create the new environment.

![Env_image](https://user-images.githubusercontent.com/117695726/210860873-7069ee88-d6f7-48a3-bcbf-34545e961379.png)


4. Open Anaconda Prompt Terminal. This step can be performed seeking in Windows searcher "Anaconda Prompt". Or with the following guide in Anaconda Navigator. Note: in this repo our new environment was named "redes2".

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Go to "Environments", under the name of your new environment select "Play" button and "Open Terminal".

![AnPrompt-image](https://user-images.githubusercontent.com/117695726/210872904-9eef9672-b76f-473a-a96c-4da596062056.png)

Make sure that you are working in the environment just created verifying the name in parenthesis showed in the Terminal. As it is shown next.

![Env_terminal](https://user-images.githubusercontent.com/117695726/210872873-07e06405-955d-46be-9281-afa0cd9995de.png)


5. Install TensorFlow 2.10 in the environment just created in Anaconda with Anaconda Prompt.
  ```sh
  pip install tensorflow==2.10
  ```
  

<!-- USAGE EXAMPLES -->
## Usage

1. Download our <a href="https://drive.google.com/file/d/1cv9Z_p6xMf9DlcN7RExvpuYswEFczsmD/view?usp=sharing">pretrained-AlexNet</a> for Keras/TensorFlow implementation.

2. Read the h5 file from Spyder with the following.
   ```sh
   import tensorflow as tf
   alexnet_model = tf.keras.models.load_model('/.../alexnet.h5')
   ```
3. Corroborate the loading of our model.
   ```sh
   alexnet_model.summary()
   ```


<!-- CONTACT -->
## Contact

Armando Reyes - [LinkedIn](https://www.linkedin.com/in/armando-reyes-5782371ba/) - reyesarmando.reyes@gmail.com

Eduardo Rivas - [LinkedIn](https://www.linkedin.com/in/eduardo-rivas-posada/) - eduardo.rivasp@ieee.org

