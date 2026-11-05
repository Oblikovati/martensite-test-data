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
- `OCCT-544/solid.brep.txt`: issue #544 ("Infinite loop when Simplifying Fuse operation,
  CPU to 100%"), the attachment itself; the input `bug_gh544.brep` of
  `tests/bugs/modalg_8/bug_gh544`. The issue and attachment state no licence.
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

The unchanged distribution terms are included as `LICENSE_LGPL_21.txt` and
`OCCT_LGPL_EXCEPTION.txt`, copied from the same source revision.

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

- `freefont-20211204/FreeSerif.ttf`: GNU FreeFont FreeSerif
  (https://savannah.gnu.org/projects/freefont/), as shipped by the Debian package
  `fonts-freefont-ttf` 20211204+svn4273-2. It serves a text-engraving case whose
  expected values hold only for this font. It is redistributed under the GNU GPL,
  version 3 or later, with the Special Font Exception; the terms are in
  `freefont-20211204/LICENSE` and `freefont-20211204/GPL-3`.

- `freefont-20211204/FreeSerifBold.ttf`, `FreeSansBoldOblique.ttf` and
  `FreeMonoOblique.ttf`: three more faces of the same package and under the same
  terms. With `FreeSerif.ttf` they serve the text of the bottle and snowflake
  samples, loaded by path so that those cases do not depend on the fonts installed
  on a machine.

The next two fonts serve the one-line-font case `tests/v3d/fonts/B6`, unchanged:

- `olf-testfont-2.000/OLFTestFont-Regular.ttf`: OLF TestFont 2.000, the free test
  sample of Creative Juncture LLC (https://www.onelinefonts.com). Its embedded
  licence refers to the vendor EULA, which restricts copying and redistribution,
  and no redistribution grant was found. It is kept here by the maintainer's
  decision (2026-11-04); the rights holder may ask for its removal.
- `machine-tool-gothic-1.0/machtgth.ttf`: Machine Tool Gothic 1.0 by Engineering
  Geometry Systems. Its licence is unknown. It is kept here by the same decision,
  on the same terms.

Each folder's `SOURCES.json` records where the file came from, its size and SHA-256.

## drivers

`lavapipe-mesa-26.1.6-noble-x86_64.tar.xz` holds the software Vulkan driver that the
renderer's recorded images were captured with, so CI and contributors reproduce them
exactly. It is `libvulkan_lvp.so`, unchanged, from the Pop!_OS package
`mesa-vulkan-drivers 26.1.6-1pop0~1787580452~24.04~a5619ea` (noble, amd64), an ICD manifest
that points next to the library, the package's `copyright` file (Mesa is under the MIT
licence) and `SHA256SUMS`. The driver links the Ubuntu 24.04 `libllvm20` 20.1.2.

- Archive SHA-256: `5ff06be966031b198983ca3cef4bad2226cb3e254feedd9239b4b8c04292323e`
