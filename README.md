#### Course:

###### ITCS 5152 - Computer Vision

#### Project Title:

###### Visualising Color Variation Under Different Lighting Conditions

#### Project Members:

###### Amit Shetty, Anirudh Narayanan, Naman Manocha, Nicolas Jones

#### Industry Partner:

###### Vishion

##### 1. Abstract:

The purpose of this project is to visualise the variation of color swatches used by building designers to decide what color to use. These colors are recognised as true colors or in our case (the ground truth) by using different lighting conditions to estimate our values. The standard followed here is [Sherwin Williams](https://www.sherwin-williams.com/painting-contractors/color/find-and-explore-colors/paint-colors-by-family)

##### 2. Data Preprocessing:

We will be using the color swatches provides by our indutry partner at Vishion. From the color swatches we have identified 33 different color samples. To study color variations we will be taking pictures of the color swatches in 3 different lighting conditions which are:

- Outdoor in cloudy conditions
- Indoor With no external light (near the window)
- Indoor with external light shining on the color swatch

We end up with 99 images that we will be using as our input samples along side 33 sample color data pulled directly form the Sherin Williams website. The data is present in the 'SummaryOfPictures4Project.xlsx' file. Therefore in total we have 132 color samples to work with.

In order to do a color variation we need to subject all colors to a standard filter process which does the following:

- Crop the central portion of the image by taking a 200*200 pixel box.
- Use the central pixel of the box as the input sample for the color comparision.
- Convert the pixel to a Jupyter notebook compatible format.
- Apply a 5*5 Gaussian filter to the image to smoothen it and have stable pixel values to compare against
- Split the central pixel into its constituent RGB values.

Once we have these values we extract the Sherwin Williams standards taken directly form the website and use various graphs to compare them. The following graphs ar used to visualise the color variations:

- 3D plot showing how far apart the observed color space and the Sherwin Williams standards are
- Plot showing the color varions between the central row of pixels and the Sherwin Williams stanadars since we are trying to observe how pixels sorrounding the central pixel are affected by the lighting conditions.
- sRGB color representation of the Observed colorspace using [Color Science](https://www.colour-science.org/)

##### 3. Sample Representation of Color Variation:

<div>
<img src="sample.png"></img>
</div>

##### 4. How much have we accomplished so far

From the perspective of what was asked of us from our industry partner we have accomlished all the goals set for us in our meeting. The goal being in what unique ways we can study variations between the Sherwin Williams standard and the observed color space under different lighting conditions. The goal being to help us understand how to meausre light's effect in color surfaces.

To add to our project, we hvae also incorporated the changes mentioned by the professor in our second stage project meeting. The goal being representing the the Observed and Sherwin williams coolr standard in the sRGB color space.

##### Conclusions

From our project we have learnt to use different standards to identify color variations in images. We hvae learnt how different lighting conditions can affect users perception of color and how this data can help indutry professionals who perform home renovations. We see other uses for this data such as online retailers selling clothes where the color shown on screen doesn't match the color the user receives which prompts a return to the online retailer costing them a lot of money. While there are many more techniques to study since color judgement is usually subjective we believe we have explored enough methods to shed some light to analysing the differences.
