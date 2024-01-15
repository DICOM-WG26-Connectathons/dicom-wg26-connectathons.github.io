# Creator Document Annotations

Partners: None
Multiplicity: Once for each slide/annotation object pair

## Purpose
The Annotation Creators document the annotations created to serve as a source of truth
when evaluating the Viewer and Annotation User systems.

## Evidence Required
1. See the Appendix:Image and Annotation Description
2. See the Appendix:Image Metadata for the **image metadata** required in this test.
3. See the Appendix:Annotation Metadata for the **annotation metadata** required in this test.
4. See the Appendix:Visualization of Annotations

## Procedure
1. Create a PDF document that describes the image and annotation data per the *Image and Annotation Description* appendix. Submit that document to the Test Manager for evaluation and distribution to all other participants.
2. Complete and submit a copy of the [Image and Annotation Metadeata spreadsheet](Image_and_Annotation_Metadeata.xlsx) to the Test Manager for evaluation and distribution to all other participants
   - Complete the first sheet in the spreadsheet with label Image Metadata
   _ Create one sheet of Annotation Metadata for each Annotation object that will be submitted in the context of the one original Whole Slide Image.
   - If you intend to submit data created in the context of other WSI data, complete and submit a separate spreadsheet for each Whole Slide Image.
3. Document how the Annotation objects should be rendered per the description in the *Visualization of Annotations* appendix. Create a zip of this evidence and submit it to the Test Manager for evaluation and distribution to all other participants.

## Evaluation
The first two items are objective. The third item requires more interpretation/nuance.

* Review the Image and Annotation spreadsheet for completeness.
   - Reject any incomplete spreadsheets and return them to be submitted again.
* Compare the metadata in the Image and Annotation spreadsheet with values pulled from the Archive systems for the data submitted by this Annotation Creator.
   - Reject any submissions where the spreadsheet does not match the data in the Archive systems. The Annotation Creator is required to resolve the issue and submit the spreadsheet when corrected or notify the Test Manager that the Archive systems have been updated (or both).
* Review the Image and Annotation Description PDF and the other evidence submitted for visualization of Annotation objects. If these are sufficient to provide guidance to the other participants, this last item can be resolved. If these are not sufficient, return them to the Annotation Creator with guidance on how to improve the evidence.
   - You might need to engage a Subject Matter Expert to determine if these are adequate and/or to get advice on what needs to be improved.
   - Keep in mind the goal is to provide a basis for reviewing the actions of other actors. There is no defined standard for that basis.


## Appendix Material

### Image and Annotation Description
Review of the Annotation objects requires an understanding of the pathology in the original WSI data as well as the Annotation object or objects submitted by the Annotation Creator.
In plain text, you will describe what is found in the original slide.
This can be as formal as formal as a Pathology Report or as informal as 1-2 sentences that describe the slide.
You will also describe what the Annotation objects are intended to specify.
You are not required to describe how your software works, including any machine learning models used or developed.

If you are submitting multiple Annotation objects for a single slide image, you will describe the original slide one time and each Annotation object one time.

### Image Metadata
Image metadata is required to help test partners identify the WSI data used by Annotation Creator. This section lists the metadata items that will be submitted. You will find these same items listed in  [Image and Annotation Metadeata spreadsheet](Image_and_Annotation_Metadeata.xlsx).

| DICOM Tag | Opt | Element Name or Other Name           |
|-----------|-----|--------------------------------------|
|    NA     |  R  | Annotation Creator Organization Name |
| 0008,0050 |  O  | Accession Number                     |
| 0008,0070 |  R  | Manufacturer                         |
| 0008,1090 |  R  | Manufacturer's Model Name            |
| 0010,0010 |  R  | Patient Name                         |
| 0010,0020 |  R  | Patient ID                           |
| 0018,1020 |  R  | Software Versions                    |
| 0020,000D |  R  | Study Instance UID                   |
| 0020,000E |  R  | Series Instance UID                  |
| 0020,0010 |  O  | Study ID                             |
| 0020,0011 |  R  | Series Number                        |
| 0048,0013 |  R  | Number of Focal Planes (enter 1 if 0048,0013 is not include in image) |
| 0048,0302 |  R  | Number of Optical Paths              |
| 2200,0002 |  O  | Label Text                           |

### Annotation Metadata
Annotation metadata is required to help test partners identify the annotations created by Annotation Creator. This section lists the metadata items that will be submitted. You will find these same items listed in  [Image and Annotation Metadeata spreadsheet](Image_and_Annotation_Metadeata.xlsx).

Some of the items are redundant with metadata values for the original image data.
Please do fill those in for completeness.

| DICOM Tag | Opt | Element Name or Other Name           |
|-----------|-----|--------------------------------------|
|    NA     |  R  | Annotation Creator Organization Name |
| 0008,0050 |  O  | Accession Number                     |
| 0008,0070 |  R  | Manufacturer                         |
| 0008,1090 |  R  | Manufacturer's Model Name            |
| 0010,0010 |  R  | Patient Name                         |
| 0010,0020 |  R  | Patient ID                           |
| 0018,1020 |  R  | Software Versions                    |
| 0020,000D |  R  | Study Instance UID                   |
| 0020,000E |  R  | Series Instance UID                  |
| 0020,0010 |  O  | Study ID                             |
| 0020,0011 |  R  | Series Number                        |

### Visualization of Annotations
The other participants, Test Manager and subject matter experts need to understand
what should be considered ground truth for the rendering of the graphic objects found
in your Annotation objects.
We imagine that the graphic objects will be distributed in the image based on the pathology, and that this distribution may not be uniform.
That is, there may be different graphic objects in different sections and/or the density of
any given typ of object may vary based on location.

We need the Annotation Creator to assess each Annotation object and provide this information.
1. Render the image that best fills one computer screen and shows the distribution of graphic objects. This rendering might show many graphic objects that are adjacent and not distinguishable at this magnification. Perform a screen capture at this rendering.
2. Identify one or more areas that should be of interest for the Viewing applications to render. If the graphic objects are more or less evenly distributed across the slide, you will likely select one area. If there are differences in the graphic objects themselves or significant differences in the density of objects in two or three regions, then identify those three regions. You are welcome to schedule a video conference call with the Test Manager for guidance. Use the tool of your choice to draw boxes/circles/etc. around these areas of interest and label them numerically (1, 2, 3).
3. Write a brief sentence or two about why these areas are of interest to the other application software. Include the numeric values and any differences between these areas.
4. Zoom in on the areas of interest, using your own software that continues to show the graphic objects in the Annotation object. As you zoom in, you should see a better version of the slide image and annotation.  Create screen captures of these zoomed in images.
5. Name the files with a convention that identifies the slide, the numeric index (1, 2, 3 ...) and the zoom used for rendering. For example: ACME_Image_A_Area_1_Zoom_5.png. Provide levels of zoom that utilize each image in the WSI stack. Do not just provide a view at the lowest zoom and the highest zoom.

The description above assumes you supply a single PDF with the text description and individual screen captures of the rendered images. You could also supply a singlel PDF with both the text and all screen captures.