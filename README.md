# TOY-GPT
## It’s great to see you here to try out my toy!
This repository contains an experimental implementation of a character-level GPT-2 architecture. By sharing this project—called “toy-gpt”—I aim to demonstrate the fundamentals of building a GPT-like approach from scratch.
---

## Inspiration Behind the Project

This project was inspired by **Andrej Karpathy’s** exceptional video series on building GPT models from scratch. His hands-on approach and in-depth explanations provided the foundational knowledge needed to develop this implementation. 

You can explore the video series here: [Building GPT from Scratch by Andrej Karpathy](https://youtube.com/playlist?list=PLAqhIrjkxbuWI23v9cThsA9GvCAUhRvKZ&si=t6iFcNV2q4V741AV). It’s a highly recommended resource for anyone looking to understand the inner workings of GPT-like architectures!

---

## What is GPT (Decoder-Only Transformer)?
GPT (Generative Pre-trained Transformer) is a Transformer model that consists solely of the decoder component. In the Transformer architecture, there are generally two main parts: the “encoder” and the “decoder.” 
GPT focuses on text generation tasks by using only the decoder to predict the next word (or character). 
Well-known models such as GPT-2, GPT-3, and GPT-Neo operate on this principle.

### A Brief Look at the Transformer
Multi-Head Attention: A mechanism that examines different parts of the input sequence simultaneously through various attention heads.
Feed Forward Network: A fully connected layer that follows each attention layer, strengthening the neural network’s learning capacity.
Layer Normalization and Residual Connections: These help increase model depth while mitigating the vanishing gradient problem, making training more efficient.

### Why Does GPT-2 Use Only the Decoder?
GPT-2, which uses only the decoder part of the Transformer, operates as follows:

Masked Multi-Head Attention: The model applies masking in self-attention so it does not see future tokens.
Next Character Prediction: It attempts to predict the next character (or word vector) in the input sequence and outputs the probability distribution.
Autoregressive: The model uses previously generated predictions as inputs at each step, continuing to generate text.
In this repository, we have a character-based GPT-2 implementation. Instead of predicting words, each character is treated as a separate token for next-token prediction.

## Training Summary
I trained the model on about 522M tokens using Kaggle’s GPU environment (GPU 100). The total number of parameters is approximately 86.33 million. 
Below are some of the intermediate outputs recorded during training (training step, train loss, validation loss, elapsed time, etc.):

```bash
312.5s    step 4:   step 0:    train loss 6.7507,  val loss 6.7500
1390.6s   step 5:   step 500:  train loss 2.0468,  val loss 2.0476
2467.0s   step 6:   step 1000: train loss 1.5324,  val loss 1.5219
3543.2s   step 7:   step 1500: train loss 1.3649,  val loss 1.3581
4619.7s   step 8:   step 2000: train loss 1.2836,  val loss 1.2715
5696.6s   step 9:   step 2500: train loss 1.2271,  val loss 1.2097
6773.4s   step 10:  step 3000: train loss 1.1826,  val loss 1.1671
7850.6s   step 11:  step 3500: train loss 1.1567,  val loss 1.1330
8927.6s   step 12:  step 4000: train loss 1.1242,  val loss 1.1114
10004.2s  step 13:  step 4500: train loss 1.1163,  val loss 1.0915
11080.4s  step 14:  step 5000: train loss 1.0931,  val loss 1.0740
12156.4s  step 15:  step 5500: train loss 1.0785,  val loss 1.0548
13233.0s  step 16:  step 6000: train loss 1.0663,  val loss 1.0439
14310.4s  step 17:  step 6500: train loss 1.0521,  val loss 1.0282
15387.9s  step 18:  step 7000: train loss 1.0449,  val loss 1.0185
16464.8s  step 19:  step 7500: train loss 1.0338,  val loss 1.0066
17541.3s  step 20:  step 8000: train loss 1.0255,  val loss 1.0001
18617.4s  step 21:  step 8500: train loss 1.0230,  val loss 0.9904
19693.1s  step 22:  step 9000: train loss 1.0121,  val loss 0.9822
20769.6s  step 23:  step 9500: train loss 1.0086,  val loss 0.9717
21846.3s  step 24:  step 10000: train loss 1.0037, val loss 0.9668
22922.7s  step 25:  step 10500: train loss 0.9957, val loss 0.9618
23998.7s  step 26:  step 11000: train loss 0.9885, val loss 0.9515
25074.8s  step 27:  step 11500: train loss 0.9889, val loss 0.9476
26151.0s  step 28:  step 12000: train loss 0.9795, val loss 0.9421
27227.1s  step 29:  step 12500: train loss 0.9787, val loss 0.9339
28303.7s  step 30:  step 13000: train loss 0.9735, val loss 0.9339
29380.2s  step 31:  step 13500: train loss 0.9734, val loss 0.9267
30454.8s  step 32:  step 13999: train loss 0.9708, val loss 0.9202
```
## Model Output
```bash
akademisyen ABD başkan yardımcılığıyla birlikte... Milyonlarca konuşulan ve Türkiye ile İsrail arasında özellikle ABD ve İsrail’in Arjantin tek bir mutabakat ve savaşını toplamaya yönelmesini bir süre önceden bilmiyor. 
ABD eleştirileri, Türkiye’de ve Suriye’de yaşayan yaşlısının angaj riskini artırabilmesi durumunda acilen iyileşmesi engel olacak. Yasdıîçliler, “Normalden götürürken, lastik bir ideal bir davadır. 
Peki yangını çıktı. Mesela” başlığı “Türkiye, Irak’ın hukuk devleti konusunda” demişti.  
Türkiye’de İş ve Sözleşmemizin görev çalışmalarıyla ilgili bir şey olarak görüldüğümüz söz aldırması için Ankara’dan çelenk bir açılım yaptıklarını da söylüyor:  
“Ankara bir Bağdadist varsa bunların homojere vesil olması gerekiyor” dedi.  BDS ile İstanbul’daki TFF Başkanı Barış Fikri Ilicius, 2012 yılından bu yana bir kovanak oturumu yapmış, Atiker İstikamı, İstiklal Maçı, İstanbul. 
İstanbul Eğitim Kurumu Büyükşehir Belediye Başkanı Hamit Kuzu, Karadeniz, sözleşmeli öğrencilere Atiker Komu
```
- **The generated text may seem nonsensical**, but this behavior is expected from a character-based model trained without fine-tuning. 
    The purpose here is not to produce meaningful outputs but to demonstrate that the model can learn the structure of the Turkish language at a character level.

## Next Steps to Improve the Model:
- **Fine-Tuning:** Fine-tune the model on a high-quality, domain-specific dataset to generate more meaningful and coherent text.
- **Reinforcement Learning (RL):** Use RL techniques to further enhance the output quality and reduce noise.
- **RLHF (Reinforcement Learning from Human Feedback):** Incorporate human feedback to optimize the reward model and align the generated outputs to user expectations.
- **Scaling Up:** Train the model on a larger dataset with higher computational power to improve generalization and fluency.

## Contact
If you have any questions about Transformers or GPT, feel free to reach out to me on LinkedIn:  [canbingöl](https://www.linkedin.com/in/canbingöl/)
            
