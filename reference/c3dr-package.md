# c3dr: Read and Write C3D Motion Capture Files

A wrapper for the 'EZC3D' library to work with C3D motion capture data.

## Details

An R package for working with motion capture data based on the C++
library [EZC3D](https://github.com/pyomeca/ezc3d). Users can read,
process, and write [C3D](https://www.c3d.org/) files containing
biomechanical data.

## Main functions:

- Use
  [`c3d_read()`](https://docs.ropensci.org/c3dr/reference/c3d_read.md)
  for the import of C3D data.

- Use
  [`c3d_data()`](https://docs.ropensci.org/c3dr/reference/c3d_data.md)
  and
  [`c3d_analog()`](https://docs.ropensci.org/c3dr/reference/c3d_analog.md)
  for retrieving the point and the analog data as a data frame.

- Use
  [`c3d_write()`](https://docs.ropensci.org/c3dr/reference/c3d_write.md)
  to write a c3d object to a C3D file.

## See also

Useful links:

- <https://github.com/ropensci/c3dr>

- <https://docs.ropensci.org/c3dr/>

- Report bugs at <https://github.com/ropensci/c3dr/issues>

## Author

**Maintainer**: Simon Nolte <s.nolte@dshs-koeln.de>
([ORCID](https://orcid.org/0000-0003-1643-1860))

Authors:

- Simon Nolte <s.nolte@dshs-koeln.de>
  ([ORCID](https://orcid.org/0000-0003-1643-1860))

Other contributors:

- Benjamin Michaud (Author of included EZC3D library) \[copyright
  holder\]

- German Sport University Cologne ([ROR](https://ror.org/0189raq88))
  \[funder\]

- Aymeric Stamm (reviewed the package (v. 0.1.0) for rOpenSci, see
  \<https://github.com/ropensci/software-review/issues/686\>)
  \[reviewer\]

- July Pilowsky (reviewed the package (v. 0.1.0) for rOpenSci, see
  \<https://github.com/ropensci/software-review/issues/686\>)
  \[reviewer\]
