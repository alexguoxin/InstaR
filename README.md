## InstaR

[![Travis-CI Build Status](https://travis-ci.org/UBC-MDS/InstaR.svg?branch=master)](https://travis-ci.org/UBC-MDS/InstaR)

#### A Collaborative Software Development Project

<img src="img/logo.png" align="right" border = "10" width="250" height="250"/>

Date: February 9, 2018

#### Overview

According to a [study](http://comp.social.gatech.edu/papers/icwsm15.why.bakhshi.pdf) by Yahoo Labs, “Filtered photos are 21 percent more likely to be viewed and 45 percent more likely to be commented on. Have you ever wondered how you could transform your images using filters similar to Instagram in R?

We present this package that performs digital image processing on .png images.  It encompasses functions ranging from transformations like a simple flip, playing with color hues (rgb2gray) to 2D convolutions using a simple kernel matrix to do some interesting things! We have started with quite basic but diverse functions and hope to advance and add more with time.

#### Functions

###### Blur
This function performs convolution to de-emphasizes differences in adjacent pixel values. It has an averaging effect removing detail and noise resulting in blurring of the image.

###### Flip
This is a transformation function which flips the image either horizontally or vertically.

###### Greyscale
This function converts an RGB image to grayscale.

*__Non transparent backround .png images required__*

Note: See Usage section below

#### R ecosystem
"A picture paints a thousand words", however, a well-constructed image speaks even more than that without having to rely on a written description. We want to explore the elements of filters and their implementation in R. A similar package called ["magick"](https://cran.r-project.org/web/packages/magick/index.html)  exists in R which has standard filters like blur, sobel among others. We have started with a few basic functions but want to work towards building more advanced filters similar to the ones provided by Instagram.

#### Installation

To install `InstaR`, follow these instructions:

1. Please check if ```devtools``` has been installed. If not, open the console and input the following: `install.packages("devtools")` to install devtools from CRAN. Also, check the package dependencies down below.
2. Input the following into the console: 
```
devtools::install_github("UBC-MDS/InstaR", build_vignettes = TRUE)
```
3. You are all set to use go!

#### Usage

*__Non transparent backround .png images required__*

```library(InstaR)```

1.```flip(input_path, direction, output_path)```

Arguments:

* ```input_path```: path to input image
* ```direction```: direction of flip. "h" (horizontal) or "v"(vertical)
* ```output_path```: path to output image
* Example: ```flip("./img.png", "h", "./img_flip.png")```

2.```blur(input_path, output_path)```

Arguments:

* ```input_path```: path to input image
* ```output_path```: path to output image
* Example: ```blur("./img.png", "./img_blur.png")```

3.```greyscale(input_path, output_path)```

Arguments:

* ```input_path```: path to input image
* ```output_path```: path to output image
* Example: ```greyscale("./img.png", "./img_gs.png")```


#### Package dependencies

```png```

```testit```

```tableMatrix```

#### Collaborators:

[Bhatnagar, Tarini](https://github.com/tarinib)

[Guo, Xin (Alex)](https://github.com/alexguoxin)

[Nikel, Indiana](https://github.com/indiana-nikel)
