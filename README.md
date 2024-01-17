# Text-to-Video-Generation
Generative AI is a rapidly growing field that focuses on developing algorithms that can create content independently, without being explicitly programmed. Text-to-video synthesis is one of the most fascinating applications of this technology, as it allows us to generate videos from simple text prompts. Here I learned how to input a simple text prompt, configure the pre-trained diffusion model by using DiffusionPipeline, and generate a video. 

## Generative Artificial Intelligence (GAI)

Generative artificial intelligence (GAI) is a type of AI that can create new content, such as text, images, music, and videos. GAI models learn the patterns and structure of their input training data and then generate new data with similar characteristics. GAI can learn from existing artifacts to generate new, realistic artifacts that reflect the characteristics of the training data but don't repeat it. Inputs and outputs to GAI models can include text, images, sounds, animation, 3D models, or other types of data.

![Screenshot (195)](https://github.com/CoderNitu/Text-to-Video-Generation/assets/87817227/1c5feeef-0862-4c67-8c40-f28c643b2652)


## Diffusion Models vs GANs

Generative Adversarial Networks (GANs) and Diffusion Models represent two approaches to generative AI. While both aim to generate high-quality samples, they differ in their underlying architectures and training methodologies

 1. Generative Adversarial Networks (GANs) were developed by Ian Goodfellow and his team in 2014, which has inspired the field of generative AI. This approach uses two simultaneously trained neural networks, one is the generator used to generate synthetic data (fake data), and the other is the discriminator, which is used to classify whether the input is real (image from training dataset) or fake (generated by the generator). The word adversarial points to the competitive dynamic between the generator and the discriminator, where the generator tries to fool the discriminator by passing fake data. The discriminator's job is to detect the fake data generated by the generator.
         The competitive nature of GAN training drives the iterative refinement of the generator's output. A loss function is calculated to quantify the difference between the discriminator's predictions and the ground truth labels; the generator minimizes this loss, while the discriminator maximizes it. As training continues, the networks update their parameters based on each other's feedback, gradually enhancing the quality and realism of the generated samples.
    
  ![GANs](https://github.com/CoderNitu/Text-to-Video-Generation/assets/87817227/f19dcea3-03b5-4630-858f-c30538cbd7aa)
  ![EXX-Blog-Gan-vs-diffusion-models-2](https://github.com/CoderNitu/Text-to-Video-Generation/assets/87817227/edab098f-cde4-4a1b-a9b6-a95675d20b42)

3. 




