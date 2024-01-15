# Store Original Images 

|                   |                                       |
|-------------------|---------------------------------------|
| Test Participants | Annotation Creator, Archive            |
| Test Driver       | Annotation Creator                    |
| Multiplicity      | Once for each slide that is annotated |

## Purpose
The Annotation Creator submits the original WSI data to the Archive system for storage.
There are later tests where the Archive system will need to respond to QIDO-RS and WADO-RS requests.

## Evidence Required
1. Email from Archive system that indicates the WSI data was received, stored, and is now available for QIDO-RS and WADO-RS requests.
   - No formal proof is required.
   - If the images were not stored, that will become obvious in later tests.

## Procedure
The Annotation Creator drives the test by contacting the Archive system and negotiating the mechanism for submitting the original WSI data to the Archive system. The Annotation Creator should send the Image and Annotation Metadeata spreadsheet to the Archive system as part of the communication process.

In the preferred mode, the Annotation Creator submits the original WSI data
to the Archive system using STOW-RS calls.

The Annotation Creator is allowed to submit DICOM Part 10 files to the Archive system using
a method negotiated by the two systems if STOW-RS is not possible.

After the Archive system has received the original image data and confirms it is ready for QIDO-RS and WADO-RS transactions, the Archive system will send an email to the Test Manager to indicate this task is complete. In the email, please indicate the slide data that was stored and the mechanism that was used (STOW-RS or DICOM Part 10 Out of Band).

## Evaluation
* Accept an email from the Archive system as evidence that this test was completed.
* Use the XXX script to send a QIDO-RS query to verify that the images are available for query.
   - A WADO-RS test is not required.

## Appendix Material

