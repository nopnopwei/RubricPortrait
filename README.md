# RubricPortrait

## Rubric cube portrait builder

Inspired from this [video](https://www.youtube.com/watch?v=zgK_fg1cXvM) and this [repository](https://github.com/Roman-/mosaic). The script inside `rubric.ipynb` takes in a `.PNG` image and convert it into a portrait that can be built with rubric cubes. A step by step instruction on how to build the portrait is also included by setting `show_steps=True`.
![](/img/ex1.png)

## General Workflow

The script is executable inside `rubric.ipynb` and can be easily executed by simply run the two code cells after replacing the `img_path`, `pixel_size` and `show_steps` in the second code cell. In addition, please note that the script will only work on `.PNG` files, and that the smaller `pixel_size` will mean better portrait quality, but at the same time, require more cubes to build the portrait.
![](/img/ex2.png)

## Method

The original image is manipulated by using the [Pillow](https://github.com/python-pillow/Pillow) library, alongside with modern data analysis libraries such as [Pandas](https://github.com/pandas-dev/pandas) and [Matplotlib](https://github.com/matplotlib/matplotlib). The manipulation method used in this project is known as the `Gradient Method`, where grayscale value for each grid are taken to replace each tone to the corresponding color from the rubric cube's color palette, with the color green being omitted because green usually does not look good in portraits.
![](/img/ex3.png)

## Limitation

Due to the limited colors being utilized, it is recommended to have a clear contrast between the background and the person/object you are trying to focus. Otherwise the background will blend in as show in the example below.
![](/img/ex4.png)
