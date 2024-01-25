# Text-to-Video-Generation
Generative AI is a rapidly growing field that focuses on developing algorithms that can create content independently, without being explicitly programmed. Text-to-video synthesis is one of the most fascinating applications of this technology, as it allows us to generate videos from simple text prompts. Here I learned how to input a simple text prompt, configure the pre-trained diffusion model by using DiffusionPipeline, and generate a video. 

## Generative Artificial Intelligence (GAI)

Generative artificial intelligence (GAI) is a type of AI that can create new content, such as text, images, music, and videos. GAI models learn the patterns and structure of their input training data and then generate new data with similar characteristics. GAI can learn from existing artifacts to generate new, realistic artifacts that reflect the characteristics of the training data but don't repeat it. Inputs and outputs to GAI models can include text, images, sounds, animation, 3D models, or other types of data.

![Screenshot (195)](https://github.com/CoderNitu/Text-to-Video-Generation/assets/87817227/1c5feeef-0862-4c67-8c40-f28c643b2652)


## Diffusion Models vs GANs

Generative Adversarial Networks (GANs) and Diffusion Models represent two approaches to generative AI. While both aim to generate high-quality samples, they differ in their underlying architectures and training methodologies

 ## 1. Generative Adversarial Networks (GANs): Breathing Life into Synthetic Data
   
   Generative Adversarial Networks (GANs) were developed by Ian Goodfellow and his team in 2014, which has inspired the field of generative AI. This approach uses two simultaneously 
   trained neural networks, one is the generator used to generate synthetic data (fake data), and the other is the discriminator, which is used to classify whether the input is real 
   (from the training dataset) or fake (generated by the generator). The word adversarial points to the competitive dynamic between the generator and the discriminator, where the 
   generator tries to fool the discriminator by passing fake data. The discriminator's job is to detect the fake data generated by the generator. The competitive nature of GAN training 
   drives the iterative refinement of the generator's output. A loss function is calculated to quantify the difference between the discriminator's predictions and the ground truth 
   labels; the generator minimizes this loss, while the discriminator maximizes it. As training continues, the networks update their parameters based on each other's feedback, gradually 
   enhancing the quality and realism of the generated samples.

 ![gans_gfg-(1)](https://github.com/CoderNitu/Text-to-Video-Generation/assets/87817227/eb063050-7f9c-44f3-9652-6d07d52021e2)
![EXX-Blog-Gan-vs-diffusion-models-2](https://github.com/CoderNitu/Text-to-Video-Generation/assets/87817227/ac778b14-e173-430f-a527-a38ad2720104)

 ## 2. Diffusion Models: An Elegant Journey from Noise to Data

   Diffusion models are generative AI models that create high-resolution data domain samples. They use Gaussian noise (a type of random noise that is often added to the input data, 
   which helps the diffusion model to generate new data that is similar to the training data, even when the input is not perfect)
   The diffusion Model works using two processes :
   # (a) Forward Diffusion process
       The forward diffusion process is a Markov chain that starts from the original data x and ends at a noise sample ε. At each step t, the data is corrupted by adding Gaussian noise 
       to it. The noise level increases as t increases until it reaches 1 at the final step T. At this point, x_T is completely random and independent of x.

                                                        x_t = √(1 – βt) * x(t-1) + √β_t * η_t

       where β_t is the noise level at step t, and η_t is a standard Gaussian random variable. The noise level β_t increases as t increases until it reaches 1 at the final step T. 
       At this point, x_T is completely random and independent of x.

   ![Forward-process-1024x388](https://github.com/CoderNitu/Text-to-Video-Generation/assets/87817227/34147d33-271e-4cd9-885d-baddfd6ee4f0)

   # (b) Reverse Diffusion process
       The reverse diffusion process is the inverse of the forward diffusion process. It starts from a noise sample ε and ends at a data sample x. At each step t, the noise is reduced by 
       subtracting Gaussian noise from it. The noise level decreases as t decreases until it reaches 0 at the initial step 0. At this point, ε0 is equal to x.

                                                        ε_t = √(1 – β_t) * ε(t+1) – √β_t * η_t

      where β_t is the same noise level as in the forward diffusion process, and η_t is a standard Gaussian random variable. The noise level β_t decreases as t decreases until it reaches 
      0 at the initial step 0. At this point, ε_0 is equal to x.

   ![Reverse-process-1024x388](https://github.com/CoderNitu/Text-to-Video-Generation/assets/87817227/915e2e08-77c2-43f0-b2b0-02dd01a671f9)

   The noise schedule and the number of steps are two important hyperparameters that affect the performance of the Diffusion Model. They determine how fast and how smoothly the data is 
   transformed into noise and vice versa. The noise schedule is a sequence of noise levels β_t that control the amount of Gaussian noise added or subtracted at each step t. The number of 
   steps T is the length of the forward and reverse diffusion processes. It affects the quality and diversity of the generated data. A larger T means that the data is more corrupted by 
   noise, which makes it harder to recover from the noise, but also allows for more variation in the data. A smaller T means that the data is less corrupted by noise, which makes it 
   easier to recover from the noise, but also limits the variation in the data. There is a trade-off between the noise schedule and the number of steps. A more aggressive noise schedule 
   (larger β) requires more steps to achieve better quality, while a less aggressive noise schedule (smaller β) requires fewer steps to achieve good diversity. The optimal choice of 
   these hyperparameters depends on the data domain, the score function architecture, and the computational budget.

   ## ABOUT DIFFUSION MODEL USED

   The model I used is based on a multi-stage text-to-video generation diffusion model, which inputs a description text and returns a video that matches the text description. Only 
   English input is supported. This model is developed by Model Scope and it also has limitations regarding the number of frames, language use, length of the text prompt, video quality, 
   etc that you can view on their website:  https://huggingface.co/ali-vilab/text-to-video-ms-1.7b

   ## Diffusion Pipeline

   A diffusion pipeline is a way to run diffusion models in inference by combining all the necessary components into a single class. These components include schedulers, processors, and 
   multiple independently-trained models. The DiffusionPipeline is the fastest way to load any pre-trained diffusion pipeline from the Hub (online repository or web page where the pre- 
   trained model is stored or hosted at) for inference.

   ## Multimodal AI

Multimodal AI is a type of artificial intelligence (AI) that can process, understand, and generate outputs for more than one type of data. It combines multiple types of data, such as images, text, speech, and numerical data, with multiple intelligence processing algorithms to achieve higher performances. Multimodal AI often outperforms single-modal AI in many real-world problems. It leverages diverse data types, offering a richer representation of information. This approach enhances contextual understanding, resulting in more accurate predictions and informed decisions.

 



   




   



 




