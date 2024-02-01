# Participant Requirements

## Publication of DICOM Objects
1. All DICOM objects produced during the event will be made publicly available at the conclusion of the Connectathon.
   - This includes original input images and Annotation objects produced by Annotation Creators.
   - This does not include screen captures or video recordings of how Annotation Viewers render Annotation objects and/or WSI data.

## Data Requirements
See the last section on *Image Datasets* to understand how these will be submitted and used during the event.
This section (Data Requirements) lists requirements on the WSI and Microscopy Bulk Simple Annotations objects.

### Whole Slide Imaging
1. Brightfield images will be used.
2. Only three channel 8-bit per channel color images are allowed.
   - Samples per Pixel (0028,0002) shall contain the value 3
   - Bits Allocated (0028,0100) shall contain the value 8
   - Photometric Interpretation (0028,0004) shall contain the value RGB, YBR_FULL_422, YBR_ICT or YBR_RCT
3. Modality (0008,0060) shall contain the value SM
4. Only TILED FULL images are allowed.
   - Dimension Organization Type (0020,9311) shall be present with a value of TILED_FULL.
5. Images shall contain one optical path.
   - Number of Optical Paths (0048,0302) shall be present with a value of 1.
   - Optical Path Sequence (0048,0105) shall contain one item.
6. Images will use one focal plane 
   - Extended Depth of Field (0048,0012) shall have the value NO.
7. No restrictions are placed on the type of staining used for the slide.

### Microscopy Bulk Simple Annotations
1. Annotations will conform to the Microscopy Bulk Simple Annotations Storage SOP Class IOD (DICOM Supplement 222).
2. Each annotation object will be stored within the StudyInstanceUID of the imaging it is generated in reference to.
3. The DICOM annotation instances will be placed into a Series Instance UID that is different from the source imaging.
   - All DICOM instances within the series will describe annotations using the same annotation modality.
4. Annotations will use 2D Coordinate Type
   - Annotation Coordinate Type (006A,0001) shall have the value 2D
5. Volume relative annotations will be used
   - Pixel Origin Interpretation (0048,0301) shall have the value VOLUME.
6. Annotation objects may contain multiple annotation groups.
   - Annotation Group Sequence is allowed to contain more than one item.
7. An Annotation Creator is required to supply at least one Annotation object for at least one WSI object.
   - Annotation Creators are not required to provide Annotation objects for all WSI objects used during the Connectathon.
   - Annotation Creators are not prohibitedd from providing Annotation objects for more than one WSI object.
8. An Annotation Creator is allowed to submit more than one Annotation object for a WSI object.

## Archive

## Viewer
1. Viewers will use QIDO-RS to search Archive systems for WSI and Annotation objects.
   - Private query mechanisms are not allowed.
2. Viewers will use WADO-RS to retrieve WSI and Annotation objects from Archive systems.
   - Private retrieve methods are not allowed.
3. Viewers shall be able to support multiple Annotation objects that are associated with one WSI object.
   - Viewers shall be able to convey the multiple Annotation objects to the user through their user interface.
   - The user shall be able to select and render any of the Annotation objects.
   - Viewers are not required to support simultaneous rendering of more than one Annotation object.
   - Viewers are not required to support rendering that would compare Annotation objects.
4. Viewers shall support and render Annotation objects with multiple Annotation groups.
   - Viewers shall be able to render all groups at one time or allow the user to render invidivual groups or subsets of groups.
   - Viewers are not allowed to render some groups in an Annotation object but not others.
   - Viewers shall present all groups to the human viewer. Depending on the software, the Viewer might present some groups but not others. However, the user must have a mechanism to see an inventory of all groups in any Annotation object.
5. Viewers shall support and render all Graphic Type (0070,0023) shapes:
   - POINT
   - POLYLINE
   - POLYGON
   - ELLIPSE
   - RECTANGLE
6. This requirement is driven by the requirement *Annotations will use 2D Coordinate Type*. Annotations reference one image with an associated DICOM SOP Instance UID. This image may appear at any level within the imaging pyramid. The Viewer is required to be able to render the Annotation object when the Viewer is rendering the image referenced by that Annotation object.
   - As the user zooms through the pyramid images at different zoom levels, the minimum requirement is that the Viewer be able to render the Annotation object when the user has reached a zoom level that corresponds to the reference image.
   - This requirement is silent on rendering the Annotation object when the user is viewing images in the pyramid other than the referenced image.


## Annotation Creator

1. Annotation Creators will use images provided by the Technical Project Manager or will use WSI data compliant with the DICOM Standard and that also meet the Connectathon restrictions listed in the section *Whole Slide Imaging*.
   - Annotation Creators that supply their own WSI data will test the source images with the dciodvfy tool and will only submit images that have zero errors as reported by that tool.
   - Annotation creator is responsible for testing the source images in their own laboratory but may contact the Project Manager for guidance / assistance.
2. Annotation Creators will create DICOM Annotation objects per the specifications listed in the section *Microscopy Bulk Simple Annotations*.
3. Annotation Creators shall provide Annotation objects to all participating Archive systems for storage and later retrieval.
   - The preferred method to submit the Annotation objects is using the DICOM protocol: C-STORE or STOW-RS.
   - Submission as DICOM Part 10 files using some out of band method is allowed. The Annotation Creator will negotiate a method to provide files with the Archive system(s) such as a service like DropBox.

## Annotation Consumer

## Image Datasets
Management is defined as the Technical Project Manager with support as needed from participants or community members.

1. Management will provide a limited WSI dataset (5-10 images) that are suitable for annotation by Annotation Creator systems. Notes:
   - These will be taken from previous WG 26 Connectathons and made available to all participants.
   - Management may choose to accept contributions of DICOM-compliant images from other sources.
   - This limited dataset is will not be large enough to serve as a training set for Machine Learning algorithms.
   - This limited dataset may or may not contain tissue types and/or pathologies that are suitable for a particular automated annotation algorithm.