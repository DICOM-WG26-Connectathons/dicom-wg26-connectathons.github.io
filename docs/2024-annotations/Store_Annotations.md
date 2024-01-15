# Store Annotations

|                   |                                       |
|-------------------|---------------------------------------|
| Test Participants | Annotation Creator, Archive            |
| Test Driver       | Annotation Creator                    |
| Multiplicity      | Once for each slide that is annotated |

## Purpose
The Annotation Creator submits one or more Annotation objects to the Archive system for storage.
This test is closely related to the *Store Original Images* test.
For any original image, the Annotation Creator will create and submit one or more Annotation objects.
There is one instance of this test that corresponds to that original WSI data.
If the Annotation Creator creates multiple Annotation objects for one slide,
the Annotation Creator and Archive will report the results of all Annotation storage
for that slide in on test instance.

This could have been included as part of a single test that documents the storage of
both the original images and Annotation objects.
We have chosen separate test cases for now.

## Evidence Required
1. Email from Archive system that indicates the Annotation objects were received, stored, and are now available for QIDO-RS and WADO-RS requests.
   - No formal proof is required.
   - If the Annotation objects were not stored, that will become obvious in later tests.

## Procedure
The Annotation Creator drives the test by contacting the Archive system and negotiating the mechanism for submitting the Annotation objects to the Archive system. The Annotation Creator should send the Image and Annotation Metadeata spreadsheet to the Archive system as part of the communication process.

In the preferred mode, the Annotation Creator submits the Annotation objects
to the Archive system using STOW-RS calls.

The Annotation Creator is allowed to submit DICOM Part 10 files to the Archive system using
a method negotiated by the two systems if STOW-RS is not possible.

After the Archive system has received the Annotation objects and confirms those obects are ready for QIDO-RS and WADO-RS transactions, the Archive system will send an email to the Test Manager to indicate this task is complete. In the email, please indicate the slide data that was stored, the list of Annotation objects that were stored, and the mechanism that was used (STOW-RS or DICOM Part 10 Out of Band).

## Evaluation
* Accept an email from the Archive system as evidence that this test was completed.
* Use the XXX script to send a QIDO-RS query to verify that the Annotation objects are available for query.
   - A WADO-RS test is not required.

## Appendix Material

