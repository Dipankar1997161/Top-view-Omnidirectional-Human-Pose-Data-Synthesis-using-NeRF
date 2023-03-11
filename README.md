# Monocular-View-Synthesis-using-HumanNerf

The original code will be found in this repo: https://github.com/chungyiweng/humannerf.git

Kindly check that as this repo is just an experiment conducted. 

### Environment_setup
    conda create -n mononerf python=3.8
    conda activate mononerf
### Model Train

I trained the model on subject number 377 and 387 using the following command. Changing the activation function between Relu, Leaky relu and Elu to find the sufficient results. Also changing the model pipeline to achieve the 3D reconstructed results. Further training and updates will be given soon.
    
    python train.py --cfg configs/human_nerf/zju_mocap/377/adventure.yaml
    
The model was trained for a total of of 190 epochs, following a total iteration of 97000 approx. Total time for 1 scene training is 24+ hours on a Single Gpu.

### Progressive training results
Start of training (1000 iterations)
![prog_000100](https://user-images.githubusercontent.com/85514219/223475467-e2d5ec53-a801-4aed-8406-b29cfd9cbe92.jpg)

End of Training (95000 iterations approx)
![prog_095000](https://user-images.githubusercontent.com/85514219/223475475-ac22e403-9fd3-4362-b281-6bb4db7dee52.jpg)

### Rendered output
     python run.py \
        --type movement \
        --cfg configs/human_nerf/zju_mocap/377/adventure.yaml 
https://user-images.githubusercontent.com/85514219/223476707-476458d2-0ee2-46a3-b0fd-a6581505bc10.mp4

### More Updates Coming THANK YOU
