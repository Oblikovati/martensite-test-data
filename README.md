# martensite-test-data

Input files for the Martensite test suites that need external geometry and
exchange data. Tests read them through a git submodule pinned to a commit of
this repository.

## dataset-7.9.0

The unchanged contents of the public test dataset archive
`opencascade-dataset-7.9.0.tar.xz`, published by OPEN CASCADE SAS as a release
asset of Open CASCADE Technology (release V7_9_0_beta1,
https://github.com/Open-Cascade-SAS/OCCT/releases/tag/V7_9_0_beta1).

- Archive SHA-256: `a92ed91c3271c299287c1c404bb9454d463251094bfc848acc44aee60e6a026c`
- Files: 3388

The files are redistributed as published, under the terms of the Open CASCADE
Technology distribution they belong to (GNU LGPL 2.1 with the Open CASCADE
exception). Do not edit a file in place: add a new dataset directory instead,
so pinned test baselines keep their inputs.
