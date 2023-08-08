
# Single Image Crowd Counting Using Deep Learning Models

Crowd counting and crowd analysis are essential research areas in computer vision and image processing. They involve estimating the number of people in a crowd and analysing their behaviour, movement patterns, and interactions. This field has seen significant advancements in recent years due to its broad applications in various domains, such as crowd management, surveillance, urban planning, and event organization.


## Overview
Current State-of-art results by SASNet
![vis25_with names](https://github.com/Pshubham1012/Crowd-counting-from-single-image-using-deep-learning-models/assets/124425044/b5008bb2-51c0-42ad-ae7f-685b7dd6ffe7)
## Challenges
![challenges](https://github.com/Pshubham1012/Crowd-counting-from-single-image-using-deep-learning-models/assets/124425044/03556f43-3a35-4002-8b65-8f2a508683a1)

Main problem; Scale variation
![scale and density problem](https://github.com/Pshubham1012/Crowd-counting-from-single-image-using-deep-learning-models/assets/124425044/5e54661c-672e-4a44-804e-dd03f7b7dd9b)

To address these challenges, researchers have primarily focused on enhancing network architectures, devising customized loss functions, and exploring various learning approaches.
## Proposed Solutions and Strategies
### Classification based Technique
The motivation behind adopting this approach lies in overcoming the scaling problem in crowd counting. The scaling problem refers to the substantial variations in crowd sizes observed within a single scene and across different scenes.
So rather relying on multi-channel bulky models, a classifier was explored to determine the most suitable model for a given image based on its density.

***Note*** : Code, Nework architecture, and other details are in seperate repo.

### Multiscale model
Multiple regression heads were incorporated in parallel, akin to the MCNN model, and dilated convolution kernels were employed to reduce the additional parameters introduced by the extra layers. This modification resulted in a more robust and stable model capable of better crowd-counting performance.

***Note***: Code, Nework architecture, and other details are in seperate repo.

### Self supervised learning
Instead of relying on human-labelled data, self-supervised learning leverages the abundant unlabelled data that is often easier to obtain. The key idea is to design pretext tasks that require the model to learn valuable representations or predictive patterns from the data. These learned representations can then be transferred to downstream tasks or fine-tuned for specific tasks.
Autoencoding was employed, wherein the model learned to encode the input into a lower-dimensional representation by utilizing the same input for supervision. This allowed the model to capture salient features and patterns within the data. Furthermore, rotation prediction was employed, where the model learned to estimate the angle of rotation applied to an input. By leveraging self-supervised pre-training and multitasking, the model acquired a deeper understanding of the underlying structure of the data.

***Note***: Code, Nework architecture, and other details are in seperate repo.