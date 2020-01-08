## About Me
I am a computer engineering graduate from McMaster University in Canada with experience in embedded systems design and image processing. As well, I have two years of co-operative experience working with data/cost analytics and VBA automation.

In the past, I have work experience as a Project Analyst and a Document Control Specialist. I am confident in effectively reducing timelines on automation projects, meeting key objectives and handling large workloads in fast-paced environments. 

I was born and rasied in Canada and I currently live in Vaughan, ON. English is my native language and I am a beginner at spoken Cantonese.

### Projects (INCOMPLETE)
In this section, I have highlighted a few projects that I found fun and a valuable learning experience.

#### Project 1: Image Decompressor
[HW-Image-Decompressor](https://github.com/SimonVictorLy/HW-Image-Decompressor)

This project involved designing hardware in Verilog to reverse the McMaster Image Compression (.mic10) algorithm. This project was completed on an Altera DE2 board with a Nios II processor. The data was sent and recieve through the UART. Quartus and ModelSim were used to writing, compling and testing code.

![FlowChart](https://raw.githubusercontent.com/SimonVictorLy/Simon-Ly/master/imgs/Screenshot%20from%202019-09-25%2020-12-26.png)

In compression, the name of the game is to decrease the amount of space required to send and store an image whilst maintaining the upmost quality to the user. Humans can distingush brightness and contrast more than they can do with colour. We use this fact to our advantage by converting the RGB values to a YUV colourspace. In this representation, we an preserve the Y (brightness) and half the U and V values, leaving a two thirds of the original image.

Now we have reduced the colour aspect of our image but can we reduce the detail? It is easier to conceptualize the details of an image by seeing it in the frequency domain. Doing an actual spactial conversion is very computationally expensive, however, someone figured out Fast Fourier Transformations allowing us to explore the frequency space for savings. The low frequencies of an image represent the general details of an image while the higher frequencies are finer details. This project uses a predetermined quantization matrix to scale the high frequency components down and keep more low frequencies.

![BlockDiagram](https://raw.githubusercontent.com/SimonVictorLy/Simon-Ly/master/imgs/blockdiagramDQ5.png)

The scaling from the previous step will leave a bunch of zeros when saving the image. The last step is to save the image in lowest to highest frequency and use bit headers to encode common senerios. These senarios include a run of zeros, ones, negative ones, small numbers(-8 to 7) and everything else (-256 to 255).

#### Project 2: Raytracing Reflective objects using C++ and OpenGL
[Reflective Raytracing](https://github.com/SimonVictorLy/reflective-ray-tracing)

This project was my first real project in C++ where it required compliation of
multiple classes, headers, inclusions and source files. It was very mind
blowing learning about the amount of linear algebra required for light tracing,
object transformations and camera scaling. For someone who loves video games, It really helped me put into perspective the amount of work required to implement simple things. As well, the optimization choices that can be made to reduce the load on the users' computers. Knowledge of data structures and algorithms was crutial in ensuring a polished, modular and scalable peice of code.

Disclaimer: The original render was created in Windows 10 on Visual Studio. The
migration to Ubuntu using the GNU complier did not render the scene correctly
and needs additional modifications.

![Reflective Scene](https://raw.githubusercontent.com/SimonVictorLy/reflective-ray-tracing/master/rendering.png)

#### Project 3: Halftone Image Restoriation using MATLAB
[Halftone-Image-Restoration](https://github.com/SimonVictorLy/Halftone-Image-Restoration)

This project was part of an open-ended final assignment where we needed to
restore an image affected by halftone distortion. Initially, I have tried fixing the image using
loew frequency filters and mathematical averaging filters but it was not clear
enough for me. I decided to take the question further to develop my own
model-based approach to restoring the image. As I have mentioned above, the
lower frequencies must be preserved to keep the general description of the
image. My goal was to find the patterns in the higher frequency image that represented the halftone distortion and mask it out.

My solution was to recreate the halftone distortion using a harmonic mask
because in the frequency spectrum they looked very similar. The hard part of
this was automating the selection of harmonic offset, order and magnitude.   

```markdown
# Snippet of Code

### Create Harmonic Mask
img_xn_x = repmat(xn,larger_size,1);
img_xn_y = img_xn_x';
img_xn = img_xn_y.*img_xn_x;
img_xn = img_xn(1:row_count, 1:col_count);

### Fourier of Harmonic Mask
F_a = abs(fftshift(fft2(img_xn)));
F_a = imfilter(F_a, gaus_mat,'conv');
F_a = (1-rescale(F_a,0,1));

**Bold** and _Italic_ and `Code` text

```
![Halftone Images](https://raw.githubusercontent.com/SimonVictorLy/Halftone-Image-Restoration/master/old_method.png)


### Additional Interests

I also enjoy video editing, photoshop, strength training, volleyball, badminton and rock climbing.

#### Places Traveled 
Canada:  
  New Brunswick  
  Nova Scotia  
  Ontario  
  Prince Edward Island  
  
EU:  
  Amsterdam, NL  
  Berlin, DE  
  Bergen, NO  
  Copenhagen, DK  
  Malmo, SE  
  
UK:  
  London, EN  
  
US:  
  Boston, MA  
  Buffalo, NY  
  Chicago, IL  
  Las Vegas, CA  
  Los Angeles, CA  
  New York, NY  
  Orlando, FL  
  
Others:  
  Punta Cana, Dominican Republic  

### Contact Information

Feel free to reach out to me on my [Linkedin](https://www.linkedin.com/in/simon-v-ly/) or email me at simon.victor.ly@gmail.com to dicuss our mutual interests.
