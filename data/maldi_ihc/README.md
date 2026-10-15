# MALDI-IHC mouse brain dataset

Targeted-modality validation data used in Supplementary Figs. 15–16 (SpaMetaboLearn zero-shot
generalization to a MALDI-IHC protein marker panel). Two mouse brain sections:

- `alz/` — APP-SAA/hAβSAA knock-in (Alzheimer's-model) mouse brain
- `wt/` — wild-type littermate control

Each folder contains:

- `maldi_ihc_resized_affine_downsampled.tif` — the 19-marker MALDI-IHC panel image, affine-registered
  and downsampled to match the companion H&E image's pixel grid
- `he_resized_affine.tif` — the registered hematoxylin and eosin (H&E) histology image for the same
  section
- `tissue_border.csv` — tissue-boundary coordinates used for the interior-token margin analysis
  (see `code/histology_masks.py`, `code/validate_histology_masks.py`)
- `*_roi*.roi` — blinded pathologist region-of-interest annotation files (ImageJ/Fiji ROI format),
  drawn from the H&E image alone before any MetaboFM/MSI data was consulted (see
  `code/prepare_histology_annotations.py`)

No proprietary or restricted data; deposited here to accompany the published manuscript.
