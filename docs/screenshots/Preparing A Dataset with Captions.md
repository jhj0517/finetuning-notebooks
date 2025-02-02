# Preparing A Dataset with Captions

I'll just cover some well-known considerations for LoRA training.

Generally, unless you're aiming for a particular style or overall aesthetic, your dataset will consist of images along with their corresponding captions in text files.

There are a few important things to keep in mind when making a dataset with captions. Let's take a look at them using some examples.

Here’s an example dataset with [diffusers/dog-example](https://huggingface.co/datasets/diffusers/dog-example):

![dog-example](https://github.com/user-attachments/assets/26405a3f-c54b-49fb-867d-aad68e3eae3d)

The dataset consists of 5 images of a puppy. 
<br>The **common feature** among these images **is that the puppy is sitting, rather than running or playing**.

If I want to train the model on the **puppy itself**, not on the **concept of a “sitting puppy.”** Then How should I do?

A key consideration when captioning images in a dataset is to emphasize features you want the model **to learn distinctly.** If there’s a **specific feature you want to isolate**, it’s recommended to **caption it more.**

For example, let’s say you want to train a LoRA for a character that wears a hairpin (This would be a better example). If you want the LoRA model to generate images of the character both with and without the hairpin, it’s recommended to include captions that specifically mention the hairpin. This principle also applies to other features, such as clothing, hairstyle, eye color, and so on.

Since I don’t want the LoRA from overfitting to the concept of “sitting,” I should specifically caption the puppy’s seated pose.

Let's prepare two different datasets, one with "sitting" captions and one without, and then compare the results after training the LoRA models.

1. Dataset without "sitting" captions : [dog-example-without-sitting](https://huggingface.co/datasets/jhj0517/dog-example-without-sitting)
![dog-prompt](https://github.com/user-attachments/assets/5b329033-1116-47de-9347-bcadb7ad693c)

2. Dataset with "sitting" captions : [dog-example-with-sitting](https://huggingface.co/datasets/jhj0517/dog-example-with-sitting)
![dog-prompt-sitting](https://github.com/user-attachments/assets/f5cf270b-76bd-4f59-aa82-c9ffccc8c281)

They're the same image dataset, but with different captions: one includes "sitting" and the other doesn't. I’ve temporarily named the puppy “A John’s dog” in the dataset. Since this word is used repeatedly in the captions, it will become the “trigger word” for the LoRA model.

I've trained each LoRA model for 1000 steps.
<br>here are some example results generated using these LoRA models with the prompt, 
<br>“A John’s dog is playing with a ball in the grass.”:

![playing with a ball (2)](https://github.com/user-attachments/assets/b5cb9c55-70c9-4a44-a355-f1e641b66183)


The image on the left was generated using the LoRA model without the “sitting” captions, while the image on the right used the LoRA model with the “sitting” keyword.

In my opinion, the right image appears less overfitted to the concept of “sitting.”

The seed used for both images was 77. You can regenerate the results or conduct further tests using these LoRA models from here:

https://huggingface.co/jhj0517/A-John_s-dog

A better example would involve a dataset with a character wearing a hairpin, hat, or some other distinctive clothing and so on, if I could find one.
