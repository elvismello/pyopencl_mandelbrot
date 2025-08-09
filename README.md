# pyopencl_mandelbrot

![alt text][test_image]

[test_image]: https://github.com/elvismello/pyopencl_mandelbrot/blob/main/test.png "mandelbrot test"

One of the result of me applying some concepts for using GPU kernels with python using ```pyopencl```.

## Requirements

A jupyter notebook environment is needed with ```pyopencl```, ```numpy```, ```matplotlib``` and ```Pillow```. Current working and compatible versions are

```
pyopencl==2025.1
numpy==2.2.4
matplotlib==3.10.1
Pillow==11.1.0
```


## Usage

Simply running all cells with the default parameters generates a view of the entire mandelbrot set, saving it on ```test.py```.

The fourth cell has some variables that control the side resolution, iteration limit, initial value and view window respectively with:
```
RESOLUTION = 2**8
ITER_LIMIT = np.uint16(300)
INITIAL_Z = 0

X_LIM = (-2, 1)
Y_LIM = (-1.5, 1.5)
```

The current code generates a square image with side ```RESOLUTION``` that iterates for at most ```ITER_LIMIT``` before deciding whether a coordinate is part of the mandelbrot set or not, starting from the ```INITIAL_Z``` value. ```X_LIM``` and ```Y_LIM``` control the region from where coordinates are sampled and iterated upon.
