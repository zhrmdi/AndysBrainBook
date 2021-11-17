.. _BIDS_Overview:

=============
BIDS Overview
=============

-------------

.. note::

  This article was contributed by `Daniel Levitas <https://perceptionandneuroimaging.psych.indiana.edu/people/daniellevitas.html>`__ of the Perception and Neuroimaging Lab at Indiana University.
  
.. note::

  The Stanford Center for Reproducible Neuroscience (which created BIDS) has their own tutorial `here <http://reproducibility.stanford.edu/bids-tutorial-series-part-1a/>`__.

What is BIDS?
*************

BIDS (Brain Imaging Data Structure) is a standarized format for the organization and description of neuroimaging and corresponding behavioral data, which has been largely lacking within the neuroimaging community. More specifically, data that come off the scanner are converted to NIFTI and JSON files, organized into a specific directory schema, and labeled following a precise naming convention. The result is an organized dataset that can be easily shared and understood by other researchers.

Benefits of BIDS
****************

1. Reproducibility and Data Sharing: One of the more common issues that can arise for imaging researchers is receiving data from a colleague and not being able to make heads or tails of it: how the data are named and organized do not make intuitive sense to you, finding pertinent information (e.g. Repetition Time) is time-consuming, etc. What transpires is time wasted trying to make sense of the data, leading to needless back and forth with colleague(s). Thanks to the standarized format of BIDS however, the hassles of data sharing are largely alleviated. By extension, improved data sharing allows researchers to better assess and reproduce others’ experimental findings.

2. Access to “BIDS-apps”: Once converted to BIDS format, data can be applied to software packages that take BIDS-formatted datasets as their input, colloquially referred to as “BIDS-apps”. Two of the most common and used apps are MRIQC (a quality control pipeline that generates metrics of your data), and fMRIPrep (a standarized pre-processing pipeline). Having access to fMRIPrep is incredibly useful, as labs (and even individuals within a single lab) typically have their own idiosyncratic pre-processing pipelines, which can influence findings in subsequent analyses, and create confusion for others when attempting to re-process the data. By having a standarized pipeline such as fMRIPrep, which incorporates different sofware packages (such as FSL, AFNI, ANTs, FreeSurfer, and nipype), datasets across labs/institutions can be pre-processed in a highly reproducible and transparent manner.

3. Share your own BIDS-app(s): It is not uncommon for researchers to develop a novel analysis tool or technique that languishes on their Github or some other repository, unable to gain exposure in the neuroimaging community. As BIDS becomes increasingly popular however, dataset organization and pre-processing is becoming more standardized, which can be used by various BIDS-apps. By developing a tool that accepts BIDS-formatted data, you have created a BIDS-app that is potentially applicable to a large range of users.


Okay, I’m sold. How do I convert my data to BIDS?
**********************************************

You will need to have access to your or others' raw data (e.g. dicoms) in order to perform the conversion. There are several tools that can accomplish this, see `here <https://github.com/rordenlab/dcm2niix#links>`__ for a thorough list of tools. Admittingly, most BIDS converters require a bit of user input and work. Two BIDS conversion tool demos are provided; the first is with `dcm2bids <https://github.com/UNFmontreal/Dcm2Bids>`__ (programmatic demo), and the other is with `ezBIDS <https://github.com/brainlife/ezbids>`__ (non-programmatic).
