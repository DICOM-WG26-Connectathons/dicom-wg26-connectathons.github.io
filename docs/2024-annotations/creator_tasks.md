# Annotation Creator Tasks
These are instructions to complete Annotation Creator tasks.


## AC-103: Submit proof of conformant source images to Project Manager
- For those using images from the 2023 ECDP Connectathon, send an email to the Project Manager and list each DICOM WSI (pyramid) that you will use when creating Annotation Objects.
- For those supplying different images,
   1. Validate the DICOM images using the [DICOM Validator Tools - dciodvfy and dcentvfy](http://www.dclunie.com/dicom3tools/dciodvfy.html). Only images that validate with zero errors will be accepted.
   2. Submit the output of those tools to the Project Manager for review.
   3. Share those images with the Project Manager using one of the methods described below.
   4. Submit those images to the Archive systems using one of the methods described below.

## AC-104: Submit proof of conformant annotations objects to Project Manager
1. Validate the Annotation Object(s) using the [dciodvfy validator tool](http://www.dclunie.com/dicom3tools/dciodvfy.html). This will test the integrity of each Annotation Object by itself.
2. Validate each Annotation Object with the associated DICOM WSI pyramid using the [dcentvfy validator tool](http://www.dclunie.com/dicom3tools/dciodvfy.html). This will test the integrity of the Annotation Object in the context the source images.
3. Submit the output of those tools to the Project Manager for review.

## AC-105: Submit screen captures of rendered images + annotations
The goal of this task is to provide evidence of how the annotations should render to be used as a guide when we evaluate the Viewer applications.
This is not simple to describe with a clear set of renderings to include.
For example, if your application generates 10,000 graphical objects for a single image, a single screen capture at the lowest magnification that shows overlapping anotations that cannot be distinguished is not very helpful.
Submitting a single graphical object at the lowest magnification such that the rendering shows only a dot in a sea of cells is also not helpful.

You will want to submit a small number of screen captures that will show a high level view of the annotation graphical objects and other views at higher magnification that will show more detail of the annotations.
It will be important that the screen captures or possibly out of band text will show or describe landmarks on the slide to help the Project Manager and Viewer representatives compare the expected rendering with that produced by Viewer applications.

See the section below for options on submitting the rendered images.

## AC-106: Submit annotations to all archives
Annotation Creators who choose to use ECDP 2023 images found on the NEMA FTP server do not need to submit those images directly to the Archive systems.
Those Creators need only identify the images to the Project Manager who will coordinate image submission with the Archive Systems.

Annotation Creators using their own image set will need to submit those images to the Archive systems with their Annotation objects.

Use one of the methods desscribed below for submitting DICOM objects to the Archive systems.


# File Sharing and Submission Options

## Methods for sharing DICOM Images and Annotation Objects with Project Manager
This section describes sharing DICOM objects with the Project Manager.
It is related to sharing objects with the Archive systems described in the next section.

If you are using images found on the NEMA FTP server, you do not need to share those files with the Project Manager.
As long as you identify the DICOM WSI pyramid(s), the Project Manager will find them.

There are three methods you may use to share DICOM files with the Project Manager.
The goal is to get the files to the Project Manager as soon as possible.
When selecting from the methods below, do not choose sending directly to Archive systems if that proves difficult or time consuming.

1. Submit a zip of the DICOM objects to Dropbox using this link (Dropbox upload link)[https://www.dropbox.com/request/uu3fuuPy9hzJUAELLiWy].
   - This will not require you to create a Dropbox account or register. You will need to supply a name and email address to be used to notify you and the Project Manager when the upload is complete.
   - This will go into a private Dropbox folder. The Project Manager will review the files and distribute as needed.
2. Choose another file sharing service of your choice where you can upload a zip of the DICOM objects or the individual files. You would then share a link with the Project Manager who would download the files and manage the process from there. This does not need to be Dropbox.
3. Submit your DICOM objects directly to at least one Archive that is ready for both input and Query/Retrieve. You can use DICOM C-Store or DICOM STOW-RS.
   - If you start this path and see that there are delays, please switch to one of the methods described above.

## Methods for submiting DICOM Images and Annotation Objects to Archive Systems

1. The preferred method to submit DICOM objects to an Archive is to use DICOM C-Store or STOW-RS.
This is an aspect of testing we would like to perform.
2. You can submit the DICOM objects to the Archive using a non-DICOM method that you will negotiate with the Archive system. These options exist:
   - Point to a Dropbox folder that is hosted by the Project Manager.
   - Choose an alternate method of file sharing that you negotiate with the Archive system.

## Methods for submitting screen captures to the Project Manager
This will depend on the size and number of screen capture files that are included.
In all cases, name the individual files with some method that is meaningful to you and include a text index file that lists the individual files with a short description.

Please submit the screen captures in a zip file.
If you are creating multiple Annotation Objects, you will need to submit one set of screen captures for each Annotation Object.
You can submit individual zip files or a single zip file.

1. Upload the zip file(s) to Dropbox using this link (Dropbox upload link)[https://www.dropbox.com/request/uu3fuuPy9hzJUAELLiWy]. This is the preferred method.
2. Upload the zip file(s) to a file sharing service of your choice and send a link to the Project Manager.
3. Send the zip file(s) to the Project Manager using email.
You might have issues with the size of the zip files.