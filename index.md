## About Me
I am a recent computer engineering graduate from McMaster University with experience in embedded systems design and image processing. As well, I have two years of co-operative experience working with data/cost analytics and VBA automation.

Through my internships as a Project Analyst and a Document Control Specialist, I have demostrated how to effectively reduce timelines on projects, meet key objectives and handle large workloads in fast-paced environments. 

### Projects
I have highlighted a few projects below that I enjoyed and learned a lot from.

#### Project 1: Image Decompressor
[HW-Image-Decompressor](https://github.com/SimonVictorLy/HW-Image-Decompressor)

This project involved designing hardware in Verilog to reverse the McMaster Image Compression (.mic10) algorithm.

In compression, the name of the game is to decrease the amount of space required to send and store an image whilst maintaining the upmost quality to the user. Humans can distingush brightness and contrast more than they can do with colour. We use this fact to our advantage by converting the RGB values to a YUV colourspace. In this representation, we an preserve the Y (brightness) and half the U and V values, leaving a two thirds of the original image.

Now we have reduced the colour aspect of our image but can we reduce the detail? It is easier to conceptualize the details of an image by seeing it in the frequency domain. Doing an actual spactial conversion is very computationally expensive, however, someone figured out Fast Fourier Transformations allowing us to explore the frequency space for savings. The low frequencies of an image represent the general details of an image while the higher frequencies are finer details. This project uses a predetermined quantization matrix to scale the high frequency components down and keep more low frequencies.

The scaling from the previous step will leave a bunch of zeros when saving the image. The last step is to save the image in lowest to highest frequency and use bit headers to encode common senerios. These senarios include a run of zeros, ones, negative ones, small numbers(-8 to 7) and everything else (-256 to 255).

Altera DE2 board
NiosII
ModelSim

![Image](https://raw.githubusercontent.com/SimonVictorLy/Simon-Ly/master/imgs/Screenshot%20from%202019-09-25%2020-12-26.png)

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

#### Project 2: Raytracing Reflective objects using C++ and OpenGL
[Halftone-Image-Restoration](https://github.com/SimonVictorLy/Halftone-Image-Restoration)
#### Project 3: Halftone Image Restoriation using MATLAB
[Optimized Contrast Tone Mapping](https://github.com/SimonVictorLy/OCTM-Project)
### Additional Interests

I also enjoy video editing, photoshop, strength training, volleyball, badminton and rock climbing.

### Contact Information

Feel free to reach out to me on my [Linkedin](https://www.linkedin.com/in/simon-v-ly/) or email me at simon.victor.ly@gmail.com to dicuss our mutual interests.
