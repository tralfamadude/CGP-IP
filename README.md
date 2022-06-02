# CGP-IP

CGP-IP is a Python library based on CGP (Cartesian Genetic Programming: https://en.wikipedia.org/wiki/Cartesian_genetic_programming) to work on Image Processing.

This libraray is inspired from two papers :

- GENETIC PROGRAMMING THEORY AND PRACTICE X from RICK RIOLO, EKATERINA VLADISLAVLEVA, JASON H. MOORE, MARYLYN D. RITCHIE
- MARS TERRAIN IMAGE CLASSIFICATION USING CARTESIAN GENETIC PROGRAMMING from J. Leitner, S. Harding, A. F¨orster, J. Schmidhuber

This version (as the papers described) is typed. It uses only images in input and output.

A mixed typed version is in preparation and will be release soon.


# Setup

`conda create --name CGP-IP python=3.7
conda activate CGP-IP
pip install numpy
pip install opencv-python
pip install tqdm
pip install matplotlib`

# Test Data
One of the tests noted in the papers on CGP-IP is the dataset for the lunar images https://www.kaggle.com/datasets/romainpessia/artificial-lunar-rocky-landscape-dataset (creative-commons lic.), which is gigantic (5GB). To make testing against that more manageable, 250 images from that collection are included under lunar/ directory. The data is synthetic moon images similar to what an astronaut would see while walking on the moon. Because it is synthetic, it is easy to have nice masks to classify objects (large rock, small rock, "sky").

Annotation/Mask colors:

pebbles: no color
smallerrocks: green
larger rocks: blue
sky: red

- lunar/render  the grayscale lunar image, suitable as input
- lunar/clean   annotated mask with very small rocks removed
- lunar/ground  annotated mask with full details

The images in render/ directory is the input (X in DL terminology) for training.

Images from either clean/ or ground/ directories can be used for the output (Y in DL terminology) file in training. The clean/ one might be easier to learn.


