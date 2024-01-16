# Participant Requirements

## Management
Management is defined as the Technical Project Manager with support as needed from participants or community members. The items listed under this *Management* section list items that will be provided as part of Connectathon testing.

1. Management will provide a limited WSI dataset (5-10 images) that are suitable for annotation by Annotation Creator systems. Notes:
   - These will be taken from previous WG 26 Connectathons and made available to all participants.
   - Management may choose to accept contributions of DICOM-compliant images from other sources.
   - This limited dataset is will not be large enough to serve as a training set for Machine Learning algorithms.
   - This limited dataset may or may not contain tissue types and/or pathologies that are suitable for a particular automated annotation algorithm.

## Archive

## Viewer

## Annotation Creator

1. Annotation Creator will provide source images that will be used for their annotations. Source images will be compliant with the DICOM VL Whole Slide Microscopy Image IOD with these additional requirements (taken from the 2024 DICOM Annotations Connectathon Proposal):
   - All slide pyramid imaging will be stored within a single, {StudyInstanceUID}.{ImagingSeriesInstanceUID}.
   - Source imaging will have Modality = SM
   - Source imaging will be brightfield imaging.
   - Source imaging will describe a focal plane and Z-Stack.
   - All source imaging will be described using DimensionOrganizationType = TILED_FULL to implicitly define the imaging frame positioning based on frame order.

2. Annotation Creator will test the source images with the dciodvfy tool and will only submit images that have zero errors as reported by that tool.
 - Annotation creator is responsible for testing the source images in their own laboratory but may contact the Project Manager for guidance / assistance.

 3. Annotation Creator shall create annotations that conform to the XXX IOD with these additional requirements (taken from the 2024 DICOM Annotations Connectathon Proposal):
    - Each annotation will be stored within the StudyInstanceUID of the imaging it is generated in reference to.
    - The DICOM annotation instances will be placed into a Series Instance UID that is different from the source imaging.
    - All DICOM instances within the series will describe annotations using the same annotation modality.

## Annotation Consumer

