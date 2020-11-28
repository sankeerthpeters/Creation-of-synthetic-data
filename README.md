# Creation-of-synthetic-data
To automate the process of generation of data (images and annotation files) for shiny objects(Shafts)  with a quality that is high and large variations in quantities under a given time frame.

## Requirements

Blender 2.8 or later (https://www.blender.org/download/)

## Thoughts on the implementation

Blender is an open source software which helps to design and code easily.

A brief algorithm breakdown;
- Importing required libraries
- Baking of dynamics
- Randomly hiding the shafts so that images with different number of shafts will be produced
- Randomizing the orientation so that the dynamics will be changed
- Creating compositor nodes which filters the object to get only edges
- finding out pixel coordinates, angle w.r.to x-axis and also xy plane and confidence intervals
- writing all the data into a textfile
- rendering a greyscale image(256x256)
- finally unhiding the shafts to make them ready for the next iteration

## order of parameters in textfiles
- class
- x,y pixel coordinates
- angle of shaft w.r.to x-axis
- angle of shaft w.r.to xy plane
- confidence interval- 1(number of visible vertices to maximum number of visible vertices on the longer edges of shaft)
- confidence interval- 2(number of visible vertices to maximum number of visible vertices on the smaller edges of shaft)
