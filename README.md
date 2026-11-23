# data-mirror

Mirrored third-party files for an AI photo manager that runs on the user's
own computer, as a desktop app or self-hosted, so photos never leave it. The
app downloads these files at install time: machine-learning model weights
and, once a month, a taxonomy data bundle. This repository holds no code. Its
releases hold the files, unchanged, so that an installation still works when
an original host is slow or unavailable.

## What is here

Each file lives in a release of its own, tagged by its content
(`sha256-<first 16 hex digits>`). Files larger than 500 MB are split into
numbered parts (`.000`, `.001`, …). Every release also carries:

- `LICENSE.txt`: the licence the file is published under by its authors
- `CREDIT.txt`: the attribution that licence asks for

The release `index` holds `index.json`, which lists every file with its
SHA-256, size, licence, credit and download addresses. Next to it is
`index.json.sig`, an Ed25519 signature that the app checks before trusting
the index. The app checks every part and every whole file against its
SHA-256, so a changed or damaged file is never used.

## Origins and licences

Only files whose licence permits redistribution, including commercial use,
are mirrored here.

| File | Original source | Licence |
| --- | --- | --- |
| MegaDetector v6 (`MDV6-apa-rtdetr-e.pth`) | Zenodo record 15398270, Microsoft AI for Good Lab | CC-BY-4.0 |
| SigLIP 2 base (`google/siglip2-base-patch16-naflex`) | Hugging Face, Google | Apache-2.0 |
| BioCLIP 2 / BioCLIP 2.5 Huge (`imageomics/…`) | Hugging Face, Imageomics Institute | MIT |
| TreeOfLife-200M text embeddings (`imageomics/TreeOfLife-200M`) | Hugging Face, Imageomics Institute | CC0-1.0 |

All rights remain with the original authors. Please cite them, not this
mirror. Each release names its exact source and revision.

## Not affiliated

This mirror is not run by, endorsed by or affiliated with any of the projects
above.

## Removal requests

If you are a rights holder and want a file removed, please open an issue.
It will be taken down promptly.