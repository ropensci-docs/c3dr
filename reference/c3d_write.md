# Write a c3d file in R

Write a c3d file using the C++ ezc3d library.

## Usage

``` r
c3d_write(x, file)
```

## Arguments

- x:

  A c3d object.

- file:

  A string with the file path to write to.

## Value

Returns its input invisible.

## Details

This function takes an c3d object in R and writes it to a c3d file. The
function creates a new c3d file from scratch and inserts all point data,
analog data and parameters in the file. Note that the resulting file
will show minor discrepancies compared to the original file (e.g., in
terms of file structure). During import and export minor rounding errors
can occur.

Force platform data is exported by writing the analog channels with raw
force data and the corresponding parameters of the `FORCE_PLATFORM`
group for processing. This means that in the current version,
modifications to the processed force platform data (`obj$forceplatform`)
will not be exported. Make modifications to the analog channels holding
the raw data instead. If you delete analog channels in your data, make
sure that `obj$parameters$FORCE_PLATFORM$CHANNEL` still points to the
correct indices.

The header parameters of the c3d object will not be exported but
recreated based on the parameter section. If you want to change the
header you should change the appropriate parameters instead.

Be cautious when writing a modified c3d object to an c3d file, as
internal inconsistencies may lead to corrupt files. `c3d_write()` and
the underlying ezc3d function perform some basic checks but may fail if,
for example, parameters and data are inconsistent. You can use the
helper function
[`c3d_setdata()`](https://docs.ropensci.org/c3dr/reference/c3d_setdata.md)
for modifying point or analog data of a c3d object. Larger modifications
may requires expert knowledge of the c3d file structure and parameters.

## Examples

``` r
# read an example file
d <- c3d_read(c3d_example())

# create a temporary file
tmp <- tempfile()
on.exit(unlink(tmp))

# write c3d file
c3d_write(d, tmp)
```
