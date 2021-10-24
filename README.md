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

## Part 2: Training NeRF
Now download the datasets:
```
bash download_example_data.sh
```

To train a low-res `lego` NeRF:
```
python run_nerf.py --config configs/lego.txt
```
After training for 50k iterations (~3-4 hours on a single GPU), you can find the resulting video at `logs/lego_test/lego_test_spiral_100000_rgb.mp4`.

![](https://user-images.githubusercontent.com/7057863/78473103-9353b300-7770-11ea-98ed-6ba2d877b62c.gif)



## D-NeRF

