# Semantic-segmentation for off-road dataset
This is a comparison study for semantic segmentation architectures, which is a computer vision technique, on, by layman's term, how a robot make estimation using pixels in images, conduct training and decide if the path forward can help it explore the world around. 

Goals:
- Fuel the creators' love and insights on computer & robotic vision, and how can it be implemented in robots
- Extend the literature of semantic segmentation for recently developed techniques, networks, and dataset
- Create introductory notebooks for code to be compiled by the public, as most relied on parallelized version where the lack of GPU access, such as NVDIA, is a setback. 

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
Mean Pixel Accuracy

{% include figure2.html %}

{% include figure4.html %}

Mean Intersection over Union

{% include figure.html %}

{% include figure5.html %}

F1 Score

{% include figure3.html %}
