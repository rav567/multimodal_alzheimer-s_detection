Data Preprocessing Pipeline for Multi-modal Alzheimer's Disease Detection

**Overview**
This project standardises and prepares MRI and PET scans for deep learning-based Alzheimer’s Disease detection. The pipeline ensures spatial alignment, intensity consistency, noise reduction, and dataset expansion through data augmentation.

**Preprocessing Steps**

1. _Voxel Shape and Size Adjustment_
- Converted original DICOMs to .nii format for easier management.
- Resampled images to consistent voxel dimensions.
- Output stored in: pet_cn_vsschanges, pet_ad_vsschanges, mri_cn_vsschanges, mri_ad_vsschanges.
- File name: Voxel Shape and Size Adjustment.


2. _Brain Extraction_
- Skull stripping performed on MRI scans only using FSL’s Brain Extraction Tool (BET).
- PET scans were not skull stripped, based on ADNI PET processing standards.
- Extraction script run via WSL Ubuntu environment.


3. Intensity Normalisation
- Normalised MRI and PET intensity distributions to standardise dynamic ranges across subjects.
- Verified successful normalisation via histogram analysis.


4. Quality Assurance
- Visual inspection of normalised images confirmed tissue contrasts and intensity range consistency.
- No major artefacts or anomalies detected.


5. Co-registration
- PET scans were aligned (registered) to corresponding MRI scans using FSL FLIRT (rigid-body registration).
- Registration ensures voxel-level anatomical correspondence across modalities.
- Alignment verified through  visual overlays (validated, no further registration required).

6. Noise Reduction
- Applied SUSAN noise reduction on MRI scans to enhance tissue boundary clarity and suppress low-signal noise.

7. Data Augmentation
- Increased dataset size via:
- Random rotations (±10–15°)
- Random left-right flipping
- Random scaling (0.9× to 1.1×)
- Each original MRI-PET pair generated one augmented pair.

8. Final Quality Control
- Verified that augmented images differed appropriately.
- Adjusted voxel shape and size post-augmentation for consistency with original preprocessed data.

**Notes**
- Preprocessing prioritised maintaining anatomical structures while introducing realistic variations.
- MRI chosen as the reference modality throughout for superior spatial resolution.
- PET scans processed minimally to align with standard ADNI guidelines.
