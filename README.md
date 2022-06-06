# Semantic-segmentation for off-road dataset
This is a comparison study for semantic segmentation architectures, which is a computer vision technique, on, by layman's term, how a robot make estimation using pixels in images, conduct training and decide if the path forward can help it explore the world around. 

Goals:
- Fuel the love and insights on computer & robotic vision, and how can it be implemented in robots
- Extend the literature of semantic segmentation for recently developed techniques, networks, and dataset
- Create introductory notebooks for code to be compiled by all, as most relied on parallelized version where the lack of GPU access, such as NVDIA, is a setback. 

# Start
- No requirement.txt installation needed, as packages can be installed locally in .ipynb notebooks using `pip install [PACKAGE NAME]`
- Pretrained models are available in the pretrained_models directory as checkpoints
- There are a total of six Google Colab Notebooks for each architecture tested. Run on Google Colab to start. 

# Experimental setup
Architectures tested:
| Approach | Architecture | Optimizer |
| ------------- | ------------- | ------------- |
| 1 | Res 50 with parallel stacking layer (ReNext 50) + PSPNet  | Adam |
| 2 | Res 50 with parallel stacking layer (ReNext 50) + PSPNet  | Stochastic gradient descent with momentum|
| 3 | Res 50 + DeepLabV3  | Adam |
| 4 | Res 50 + DeepLabV3  | Stochastic gradient descent with momentum|
| 5 | Res 50 + Fully Convoluted Network (FCN)  | Adam |
| 6 | Res 50 + Fully Convoluted Network (FCN)  | Stochastic gradient descent with momentum|

# Results
- Predicted images are available in prediction directory
- Here's a sneak peak on the predictions that are either partially distinguishable or the pinnacle of abstract arts, after training with 5 epochs with batch size 20:

https://user-images.githubusercontent.com/73409526/172077784-765d3197-6333-4f1d-b864-962aeb1be5ed.mp4

    1st column, left to right: Actual footage, Ground truth, Approach 1, Approach 2
    2nd column, left to right: Approach 3, Approach 4, Approach 5, Approach 6

- Interactive version: https://suzanneongcodes.github.io/Semantic-segmentation/ [In progress]
