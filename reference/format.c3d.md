# Formatting c3d objects

Formatting method for c3d objects

## Usage

``` r
# S3 method for class 'c3d'
format(x, ...)
```

## Arguments

- x:

  A `list` of the class `c3d` to be formatted.

- ...:

  empty argument, currently not used.

## Value

A character string with basic information for the c3d object.

## Examples

``` r
# Import example data
d <- c3d_read(c3d_example())

format(d)
#> [1] "A c3d object with\n- 55 data points and 340 frames\n- 1.70 s measurement duration (200 fps)\n- 69 analog channels (2000 fps)\n- 2 force platforms with 3400 frames"
```
