# NeRF-Homework
## General Overview
First of all you will be running the [NeRF](https://arxiv.org/pdf/2003.08934.pdf) (Neural Radiance Fields) architecture, after completing certain parts of the code. Then, you will be running a pretrained [D-NeRF](https://arxiv.org/pdf/2008.02268.pdf) architecture for a predetermined dataset. We expect you to complete these tasks in order and answer the questions in the report in the respective order as well. For the report please use the text editor and the column formatting of your preference. When uploading it, please do it as a PDF with the following name: `lastname_NeRF_code`. All of these methods are very recent so we expect you to have a lot of fun and learn a lot using them ! 
# NeRF
## Part 0: Installation
After cloning the repository, run the folowwing lines of code (you will be working in the pytorch environment): 
```
cd nerf-pytorch
conda activate pytorch
pip install -r requirements.txt
```
## Part 1: Completing the code
In this section you will be completing the code according to the explanations given in class. We marked the parts of the code you must fill in with "TODO"'s. Some of them have hints in the code itself. Please, after doing a "TODO" section, exchange the word "TODO" to "DONE" so that we can examine your code easier during evaluation. 

Now we present a list of the TODO's you have to complete in their respective order and the file in which they are located.

1. TODO 1 : define K as the camera parameters matrix. location: run_nerf.py 
2. TODO 2 : Report the functionality of get_embedder. location: run_nerf.py
3. TODO 3 : Discuss: Why do we call the function get_embedder again? How did the parameters vary this time? Relate your answer to the NeRF paper. location: run_ner.py
4. TODO 4 : Complete the None´s to instantiate the fully connected network of NeRF. location: run_nerf_helpers.py. In your report justify the modifications you made.
5. TODO 5 : Complete the None´s to instantiate the fully connected network of NeRF. location: run_nerf_helpers.py. In your report justify the modifications you made.
6. TODO 6 : Complete the fine network parameters according to the Coarse implementation. location: run_nerf.py
7. TODO 7 : Complete the optimizers parameters (learning rate, beta_1, beta_2). Answer: What is the role of these betas in the Adam optimizer?

Finally, answer in which Color Space are the inputs of the neural network. Why do you think this Color space is used? Discuss about its importance. In the load_blender.py (load_blender_data function) you will find a hint.

## Part 2: Training NeRF
Now download the datasets:
```
bash download_example_data.sh
```

To train a low-res `lego` NeRF:
```
CUDA_VISIBLE_DEVICES=x taskset -c n-m python run_nerf.py --config configs/lego.txt
```
After training for 50k iterations (~3-4 hours on a single GPU), you can find the resulting video at `logs/lego_test/lego_test_spiral_100000_rgb.mp4`.

![](https://user-images.githubusercontent.com/7057863/78473103-9353b300-7770-11ea-98ed-6ba2d877b62c.gif)



## D-NeRF

