# UAV-based Crop Mapping and FCover Estimation
### Smallholder-Dominated Landscapes of Mozambique

**Author:** Collins Edem Hlordzie   
**Institution:** ITC, Faculty of GEO, University of Twente  
**Supervisors:** Dr. F. J. Ellsäßer | Dr. F. B. Osei  
**Year:** 2026  

---

## Overview
This repository contains the analysis code for my MSc thesis 
evaluating UAV-based RGB and multispectral imagery with SegFormer 
deep learning for crop type mapping and fractional vegetation cover 
(FCover) estimation across 19 sampling areas in Mozambique.

## Research Questions
1. How accurately can crop areas be segmented from non-crop areas 
   and compared with enumerator data?
2. How do UAV-derived FCover estimates differ from enumerator-based 
   assessments for the identified crop types?

## Key Findings
- MS model significantly outperforms RGB (McNemar p<0.001, OR=1.483)
- MS Maize FCover is the only class showing significant positive 
  agreement with enumerator data (r=0.178**, ρ=0.239***)

## Notebook Execution Order
| Step | Notebook | Description |
|------|----------|-------------|
| 1 | 01_label_generation.ipynb | Generate label rasters |
| 2 | 02a_RGB_tiling.ipynb | Tile RGB imagery |
| 3 | 02b_MS_tiling.ipynb | Tile MS imagery |
| 4 | 03a_data_split.ipynb | Train/val/test split |
| 5 | 04_RGB_training.ipynb | Train RGB model |
| 6 | 04b_MS_training.ipynb | Train MS model |
| 7 | 05_inference_and_fcover.ipynb | Inference + FCover |
| 8 | 06_full_19_inference.ipynb | Full 19-SA inference |
| 9 | 07a_agricultural_statistics.ipynb | Agri statistics |
| 10 | 07b_agri_figures.ipynb | Figures |
| 11 | 08_inferential_statistics.ipynb | Statistical tests |

## Data Access
Raw UAV orthomosaics and enumerator field data are restricted 
under the ITC research programme data-sharing agreement.  
Contact: rdm-itc@utwente.nl

## Requirements
pip install -r requirements.txt

## Citation
Hlordzie, C. E. (2026). UAV-based crop mapping and fractional 
vegetation cover estimation in smallholder-dominated landscapes 
of Mozambique. MSc Thesis, ITC, University of Twente.

## Licence
MIT — see LICENSE file.
