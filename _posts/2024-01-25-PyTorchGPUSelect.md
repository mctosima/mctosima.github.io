---
layout: post
title: "Simplifying PyTorch Device Selection"
---

# Simplifying Device Selection in PyTorch: Auto-Selecting the Best Available GPU or CPU

Welcome to my latest blog post! As a PyTorch enthusiast, I'm excited to share a neat little snippet of code that I've found incredibly useful in my own deep learning projects. It's all about making the process of selecting the right processing device (GPU or CPU) as effortless as possible in PyTorch. Whether you're a seasoned pro or just starting out, this is something that can save you time and hassle.

### The Problem

If you've spent any time working with PyTorch, you know that selecting the right device for your operations can be a bit of a manual process. You might have to write extra lines of code to check if a GPU is available, and if not, default back to using the CPU. This can be especially cumbersome when you're testing your models on different machines with different hardware capabilities.

### The Solution: `check_set_gpu`

That's where my function `check_set_gpu` comes into play. This Python function automatically checks for the best available device - a GPU if one is available, or the Apple Metal Performance Shaders (MPS) fallback if you're on an MPS-enabled machine, or simply the CPU if that's all that's available. 

Here's how it works:

```python
import torch

def check_set_gpu(override=None):
    if override is None:
        if torch.cuda.is_available():
            device = torch.device('cuda')
            print(f"Using GPU: {torch.cuda.get_device_name(0)}")
        elif torch.backends.mps.is_available():
            device = torch.device('mps')
            print(f"Using MPS: {torch.backends.mps.is_available()}")
        else:
            device = torch.device('cpu')
            print(f"Using CPU: {torch.device('cpu')}")
    else:
        device = torch.device(override)
    return device
```

### How to Use It

Simply call `check_set_gpu()` in your code. The function will automatically detect and set the best available device. If you want to override the automatic selection and specify a particular device, just pass it as an argument like `check_set_gpu('cuda')` or `check_set_gpu('cpu')`.

### Benefits

- **Saves Time**: No more manual checking for device availability.
- **Flexibility**: Works across various hardware setups without any code changes.
- **Ease of Use**: A simple function call does all the work.

### Conclusion

I hope you find this function as useful as I have in streamlining your PyTorch workflows. It's a small piece of code, but it's one of those quality-of-life improvements that can make a big difference. Happy coding, and stay tuned for more tips and tricks!