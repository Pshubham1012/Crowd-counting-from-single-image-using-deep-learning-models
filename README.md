
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
### Classification-based Technique
The motivation behind adopting this approach lies in overcoming the scaling problem in crowd counting. The scaling problem refers to the substantial variations in crowd sizes observed within a single scene and across different scenes.
So rather than relying on multi-channel bulky models, a classifier was explored to determine the most suitable model for a given image based on its density.

***Note***: Code, Network architecture and other details are in a separate repository [here](https://github.com/Pshubham1012/Classification-approach/tree/main)

### Multiscale model
Multiple regression heads were incorporated in parallel, akin to the MCNN model, and dilated convolution kernels were employed to reduce the additional parameters introduced by the extra layers. This modification resulted in a more robust and stable model capable of better crowd-counting performance.

***Note***: Code, Network architecture and other details are in a separate repository.

### Self-supervised learning
Instead of relying on human-labelled data, self-supervised learning leverages the abundant unlabelled data that is often easier to obtain. The key idea is to design pretext tasks that require the model to learn valuable representations or predictive patterns from the data. These learned representations can then be transferred to downstream tasks or fine-tuned for specific tasks.
Autoencoding was employed, wherein the model learned to encode the input into a lower-dimensional representation by utilizing the same input for supervision. This allowed the model to capture salient features and patterns within the data. Furthermore, rotation prediction was employed, where the model learned to estimate the angle of rotation applied to an input. By leveraging self-supervised pre-training and multitasking, the model acquired a deeper understanding of the underlying structure of the data.

***Note***: Code, Network architecture and other details are in a separate repository.

### Future work(or work  in progress)
We can find pictures like those in a particular group of images, even if they don't have labels. We use a special model that changes images into numbers (vector embeddings). This model learns from pictures that do have labels, making it smarter. Then, we use this model to change the new, unlabeled images into numbers. We can see if these new numbers match the numbers from the labelled pictures. If they match well, the new pictures are similar to the ones in the group. We are creating a vector database for the particular dataset.
finding unlabeled data images similar to the particular dataset with the help of its vector database using vector embedding
vector embedding model finetuned on labelled data of a specific dataset and generated the vector embedding of that unlabelled test image to find whether it fits the distribution.
