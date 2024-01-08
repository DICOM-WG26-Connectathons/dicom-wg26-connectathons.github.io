# Participant Requirements

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

## Annotation User

