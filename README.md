# AlexNet-TensorFlow-with-Weights
Since 2012, <a href="https://proceedings.neurips.cc/paper/2012/file/c399862d3b9d6b76c8436e924a68c45b-Paper.pdf">AlexNet</a> is one of the most used architectures in Deep Learning for image classification. This model was trained using <a href="https://www.kaggle.com/competitions/imagenet-object-localization-challenge/data
">ImageNet</a> dataset. The pretrained AlexNet model can be found in <a href="https://pytorch.org/hub/pytorch_vision_alexnet/">PyTorch</a>, however, it doesn´t exist a guide for Tensorflow implementation. Therefore, this repo include a guide for that purpose.



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

![AnPrompt-image](https://user-images.githubusercontent.com/117695726/210862581-a128676f-441d-4e24-a58b-d1a69b3289fa.png)

Make sure that you are working in the environment just created verifying the name in parenthesis showed in the Terminal. As it is shown next.

![Env_terminal](https://user-images.githubusercontent.com/117695726/210863280-716f7ee5-9164-4e92-8ac6-91dd0a5b6e69.png)


5. Install TensorFlow 2.10 in the environment just created in Anaconda with Anaconda Prompt.
  ```sh
  pip install tensorflow==2.10
  ```
  
<p align="right">(<a href="#readme-top">back to top</a>)</p>


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

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

Your Name - [@your_twitter](https://twitter.com/your_username) - email@example.com

Project Link: [https://github.com/your_username/repo_name](https://github.com/your_username/repo_name)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

Use this space to list resources you find helpful and would like to give credit to. I've included a few of my favorites to kick things off!

* [Choose an Open Source License](https://choosealicense.com)
* [GitHub Emoji Cheat Sheet](https://www.webpagefx.com/tools/emoji-cheat-sheet)
* [Malven's Flexbox Cheatsheet](https://flexbox.malven.co/)
* [Malven's Grid Cheatsheet](https://grid.malven.co/)
* [Img Shields](https://shields.io)
* [GitHub Pages](https://pages.github.com)
* [Font Awesome](https://fontawesome.com)
* [React Icons](https://react-icons.github.io/react-icons/search)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=for-the-badge
[contributors-url]: https://github.com/othneildrew/Best-README-Template/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/othneildrew/Best-README-Template.svg?style=for-the-badge
[forks-url]: https://github.com/othneildrew/Best-README-Template/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=for-the-badge
[stars-url]: https://github.com/othneildrew/Best-README-Template/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=for-the-badge
[issues-url]: https://github.com/othneildrew/Best-README-Template/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://github.com/othneildrew/Best-README-Template/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/othneildrew
[product-screenshot]: images/screenshot.png
[Next.js]: https://img.shields.io/badge/next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white
[Next-url]: https://nextjs.org/
[React.js]: https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB
[React-url]: https://reactjs.org/
[Vue.js]: https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D
[Vue-url]: https://vuejs.org/
[Angular.io]: https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white
[Angular-url]: https://angular.io/
[Svelte.dev]: https://img.shields.io/badge/Svelte-4A4A55?style=for-the-badge&logo=svelte&logoColor=FF3E00
[Svelte-url]: https://svelte.dev/
[Laravel.com]: https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white
[Laravel-url]: https://laravel.com
[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com
[JQuery.com]: https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white
[JQuery-url]: https://jquery.com 
