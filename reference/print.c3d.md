# Printing c3d objects

Printing method for c3d objects

## Usage

``` r
# S3 method for class 'c3d'
print(x, ...)
```

## Arguments

- x:

  A `list` of the class `c3d` to be printed.

- ...:

  empty argument, currently not used.

## Value

The function prints basic information for the c3d object and returns it
invisibly.

## Details

Prints c3d objects by calling
[`format.c3d()`](https://docs.ropensci.org/c3dr/reference/format.c3d.md).

## Examples

``` r
# Import example data
d <- c3d_read(c3d_example())

print(d)
#> A c3d object with
#> - 55 data points and 340 frames
#> - 1.70 s measurement duration (200 fps)
#> - 69 analog channels (2000 fps)
#> - 2 force platforms with 3400 frames
```
