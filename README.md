# Conversion-of-Images-into-numpy-Array:

Introduction
In machine learning, Python uses image data in the form of a NumPy array, i.e., [Height, Width, Channel] format. To enhance the performance of the predictive model, we must know how to load and manipulate images. In Python, we can perform one task in different ways. We have options from Numpy to Pytorch and CUDA, depending on the complexity of the problem.

By the end of this tutorial, you will have hands-on experience with:

Loading and displaying an image using Matplotlib, OpenCV and Keras API
Converting the loaded images to the NumPy array and back
Conducting basic manipulation of an image using the Pillow and NumPy libraries and saving it to your local system.
Reading images as arrays in Keras API and OpenCV
Pillow Library
Pillow is a preferred image manipulation tool. Python version 2 used Python Image Library (PIL), and Python version 3 uses Pillow Python Library, an upgrade of PIL.

You should first create a virtual environment in Anaconda for different projects. Make sure you have supporting packages like NumPy, SciPy, and Matplotlib to install in the virtual environment you create.

Once you set up the packages, you can easily install Pillow using pip.

pip install Pillow

You can confirm that the library is installed correctly by checking its version.


# check Pillow version number
import PIL
print('Pillow Version:', PIL.__version__)

Pillow Version: 7.0.0

Great! The latest version is now downloaded. Let's move on to the next step.

Loading the Image
Here we will learn two ways to load and get the details of an image: use Pillow library and using Matplotlib library.

Method 1: Pillow Library
Select a test image to load and work with Pillow (PIL) library. Images can be either PNG or JPEG. In this example, we'll use an image named kolala.jpeg.
Either upload the image in the working directory or give your desired path. The Image class is the heart of PIL, and its properties help manipulate the pixels, format,
and contrast of the image.

The Image class uses these functions:*

open(): This can directly load the image. It has info properties like format, which gives information about the digital file format of an image, mode which gives a piece of information about pixel format (e.g., RGB or L), andsize`, which displays the dimensions of the image in pixels (e.g., 480x240).

show(): This will display the image. Your default photo preview application will pop up.

# load and show an image with Pillow
from PIL import Image
# Open the image form working directory
image = Image.open('kolala.jpeg')
# summarize some details about the image
print(image.format)
print(image.size)
print(image.mode)
# show the image
load_image.show()

JPEG
(800, 450)
RGB


Method 2: Matplotlib library
We will use the Matplotlib library to load the same image and display it in the Matplotlib frame. Just like PIL, it has the image class that performs the same function.
Functions used in this piece of code are imread(), which loads the image in the form of an array of the pixel and imshow(), which displays that image.

We will use the pyplot class from the Matplotlib library to plot the image into the frame.

# load and display an image with Matplotlib
from matplotlib import image
from matplotlib import pyplot
# load image as pixel array
image = image.imread('kolala.jpeg')
# summarize shape of the pixel array
print(image.dtype)
print(image.shape)
# display the array of pixels as an image
pyplot.imshow(image)
pyplot.show()

After the first step of loading the image using the dtype argument, we get a report on the data type of the array. In this case, it is 8-bit unsigned integers. 
The shape of the array is 800 pixels wide by 450 pixels high and 3 denotes color channels for red, green, and blue.

