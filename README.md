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

## github-issues

Input files attached to public issues of the Open CASCADE Technology GitHub
repository (https://github.com/Open-Cascade-SAS/OCCT/issues), for regression
cases whose input is in no published dataset archive. Each file is the
unchanged member of an issue attachment; `github-issues/SOURCES.json` records
the issue, the attachment URL and SHA-256, the member's size and SHA-256, the
retrieval date and the case it serves.

- `OCCT-466/cutCompound.shape`: issue #466 ("BRepBndLib::AddClose crashes"),
  member of the attachment `cutCompound.zip`; the input `bug_gh466.brep` of
  `tests/bugs/modalg_8/bug_gh466`.
- `OCCT-469/cutCompound2.shape`: issue #469 ("Bounding box is void when using
  BRepBndLib::AddOptimal"), member of the attachment `cutCompound2.zip`; the
  input `bug_gh469.brep` of `tests/bugs/modalg_8/bug_gh469`.

The files are redistributed as their reporters attached them to the public
Open CASCADE Technology issue tracker. Do not edit a file in place.

## occt-source-data

Unchanged files from the `data/` folder of the public Open CASCADE Technology
source tree (https://github.com/Open-Cascade-SAS/OCCT) at revision
`3d097a0328e71b826377d4814ab05ec3c3d23871`, for regression cases whose
`locate_data_file` input lives there rather than in a dataset archive.
`occt-source-data/SOURCES.json` records each file's OCCT path, revision, size
and SHA-256. The files are redistributed under the terms of that distribution
(GNU LGPL 2.1 with the Open CASCADE exception). Do not edit a file in place.

## occt-resource-textures

Unchanged predefined texture images from the `resources/Textures` folder of the
public Open CASCADE Technology source tree
(https://github.com/Open-Cascade-SAS/OCCT) at revision
`3d097a0328e71b826377d4814ab05ec3c3d23871`, for regression cases that use a
predefined texture by number (`vtexture <shape> <n>`, `vtextureenv on <n>`).
`occt-resource-textures/SOURCES.json` records each file's OCCT path, revision,
size and SHA-256. The files are redistributed under the terms of that
distribution (GNU LGPL 2.1 with the Open CASCADE exception). Do not edit a
file in place.

## fonts

Unchanged font files for text-rendering cases that name a specific font.

- `dejavu-2.37/DejaVuSans.ttf`: DejaVu Sans 2.37 (https://dejavu-fonts.github.io/),
  as shipped by the Debian package `fonts-dejavu-core` 2.37-8. It is
  redistributed under the Bitstream Vera licence with public-domain DejaVu
  changes; the full terms are in `dejavu-2.37/LICENSE` and the size and SHA-256
  in `dejavu-2.37/SOURCES.json`.
