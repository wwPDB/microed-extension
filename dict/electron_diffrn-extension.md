# Electron Diffraction Dictionary Update Documentation

---
Title: Electron Diffraction Dictionary Extension  
Author: C. Shao, E. Peisach  
Date: 11-Jun-2025  
email: chenghua.shao@rcsb.org  
---

This document provides an overview of extensions to support metadata collection and annotation of PDB structures resolved by Electron Diffraction methods, especially the Microcrystal Electron Diffraction (MicroED) method. Listed below are dictionary content of the new data categories designed for Electron Diffraction methods.

## pdbx_exptl_subtype
Data items in PDBX_EXPTL_SUBTYPE describes specific details about the experiments in the EXPTL category.


* **_pdbx_exptl_subtype.exptl_method**
: This data item is a pointer to _exptl.method in the EXPTL category.


* **_pdbx_exptl_subtype.method_type**
: The subtype of the method used in the experiment. The subtype should be a variance
of the primary method recorded in the the _exptl.method item, with distinctive
	       technical applications and significant scientific impacts.

    *Enumeration:*

      * Microcrystal Electron Diffraction
      * 2-Dimensional Electron Crystallography


* **_pdbx_exptl_subtype.details**
: Details about the method subtype.


## pdbx_electron_diffrn
Data items in the PDBX_ELECTRON_DIFFRN describes individual diffraction processes


* **_pdbx_electron_diffrn.id**
: This data item uniquely identifies the collection process of a set
of diffraction data


* **_pdbx_electron_diffrn.entry_id**
: This data is a pointer to _entry.id in the ENTRY category.


* **_pdbx_electron_diffrn.crystal_id**
: This data item is a pointer to the EXPTL_CRYSTAL category.


* **_pdbx_electron_diffrn.detector_distance**
: Also called the camera length (in millimeters). The camera length
is the product of the objective focal length and the combined
magnification of the intermediate and projector lenses when the
microscope is operated in the diffraction mode.


* **_pdbx_electron_diffrn.temperature**
: The mean temperature in kelvins at which the data collection
was performed on the sample


* **_pdbx_electron_diffrn.tilt_method**
: The way the sample and/or beam were tilted during the data collection

    *Enumeration:*

      * continuous rotation
      * discrete angles
      * none


* **_pdbx_electron_diffrn.collection_date**
: The date of the start of data collection


* **_pdbx_electron_diffrn.total_images**
: The number of diffraction images collected


* **_pdbx_electron_diffrn.details**
: Details of the electron diffraction process


## pdbx_electron_diffrn_crystal_prep
Describes microcrystal preparation.


* **_pdbx_electron_diffrn_crystal_prep.id**
: The ordinal identifier for the category


* **_pdbx_electron_diffrn_crystal_prep.electron_diffrn_id**
: This data item is a pointer to the pdbx_electron_diffrn category


* **_pdbx_electron_diffrn_crystal_prep.crystal_id**
: This data item is a pointer to the EXPTL_CRYSTAL category.


* **_pdbx_electron_diffrn_crystal_prep.grid**
: The type of grid that holds the sample


* **_pdbx_electron_diffrn_crystal_prep.grid_film**
: The film of the grid if applicable

    *Enumeration:*

      * FORMVAR PLUS CARBON
      * CARBON
      * SILICON DIOXIDEz
      * CELLULOSE ACETATE PLUS CARBON
      * HOLEY CARBON
      * PARLODION PLUS CARBON


* **_pdbx_electron_diffrn_crystal_prep.vitrification_method**
: The procedure for vitrification


* **_pdbx_electron_diffrn_crystal_prep.vitrification_cryogen**
: The name of cryogen used for vitrification

    *Enumeration:*

      * OTHER
      * NITROGEN
      * ETHANE


* **_pdbx_electron_diffrn_crystal_prep.microcrystal_method**
: The method used to produce microcrystal for the experiments, if applicable.

    *Enumeration:*

      * Sonication
      * FIB milling
      * Other
      * Vortexing
      * Naturally grown


* **_pdbx_electron_diffrn_crystal_prep.microcrystal_instrument**
: The instrument used to produce microcrystal for the experiments, if applicable.


* **_pdbx_electron_diffrn_crystal_prep.microcrystal_min_dim**
: The minimal dimension of the final crystal ready for diffraction experiments measured
in micrometres. For example, for microcrystal processed by FIB milling, this item refers
to the thickness of the thin lamella, which is the deciding factor whether quality
electron diffraction patterns can be achieved. Submicrometer is usually desired.


* **_pdbx_electron_diffrn_crystal_prep.microcrystal_max_dim**
: The maximal dimension of the final crystal ready for diffraction experiments measured
in micrometres. For example, for microcrystal processed by FIB milling, this item
refers to the length of the thin lamella.


* **_pdbx_electron_diffrn_crystal_prep.microcrystal_description**
: The shape or state of the final crystal ready for diffraction


* **_pdbx_electron_diffrn_crystal_prep.details**
: The details about the crystal preparation for electron diffraction


## pdbx_electron_diffrn_source
Describe the electron source


* **_pdbx_electron_diffrn_source.id**
: The ordinal identifier for the category


* **_pdbx_electron_diffrn_source.electron_diffrn_id**
: This data item is a pointer to the pdbx_electron_diffrn category


* **_pdbx_electron_diffrn_source.instrument_model**
: Name of the instrument for electron generation and diffraction,
e.g. the model of microscope

    *Enumeration:*

      * FEI/PHILIPS CM300FEG/ST
      * JEOL KYOTO-3000SFF
      * FEI/PHILIPS CM300FEG/T
      * JEOL 100B
      * FEI/PHILIPS CM12
      * JEOL 2100
      * TFS TALOS
      * FEI TECNAI 20
      * TFS TALOS F200C
      * HITACHI HF3000
      * FEI TECNAI F20
      * JEOL 2100F
      * FEI TECNAI 12
      * FEI TITAN
      * FEI TECNAI F30
      * SIEMENS SULEIKA
      * ZEISS LIBRA120PLUS
      * TFS GLACIOS
      * FEI TALOS ARCTICA
      * TFS KRIOS
      * HITACHI EF3000
      * JEOL CRYO ARM 300
      * JEOL 4000
      * FEI/PHILIPS CM200FEG
      * JEOL 2010F
      * FEI POLARA 300
      * FEI/PHILIPS EM420
      * FEI TITAN KRIOS
      * JEOL 3000SFF
      * JEOL 4000EX


* **_pdbx_electron_diffrn_source.dose_rate**
: The electron dose rate in the unit of electron per square angstrom per second


* **_pdbx_electron_diffrn_source.dose_accumulated**
: The accumulated dose during the collection of the diffraction data
set indicated by _pdbx_electron_diffrn_source.electron_diffrn_id,
in the unit of electron per square angstrom


* **_pdbx_electron_diffrn_source.accelerating_voltage**
: A value of accelerating voltage (in kV) used for the electron microscopy diffraction


* **_pdbx_electron_diffrn_source.electron_source**
: The source of electrons, i.e. the electron gun


* **_pdbx_electron_diffrn_source.details**
: The details of the electron microscope and the electron source


## pdbx_electron_diffrn_detector
Describes the detector/camera


* **_pdbx_electron_diffrn_detector.id**
: The ordinal identifier for this category


* **_pdbx_electron_diffrn_detector.electron_diffrn_id**
: This data item is a pointer to the pdbx_electron_diffrn category


* **_pdbx_electron_diffrn_detector.detector_camera**
: The detector/camera used for recording diffraction images.


* **_pdbx_electron_diffrn_detector.detector_sensor**
: The general class of the electron sensor used for the detector.

    *Enumeration:*

      * PIXEL
      * CCD
      * CMOS
      * FILM


* **_pdbx_electron_diffrn_detector.mode**
: The mode of the detector for electron diffraction recording

    *Enumeration:*

      * Other
      * Integrating
      * Counting


* **_pdbx_electron_diffrn_detector.details**
: The details about the electron microscope detector and camera


## pdbx_electron_diffrn_continuous_rotation
Describes continuous rotation data collection


* **_pdbx_electron_diffrn_continuous_rotation.id**
: The ordinal identifier for the category


* **_pdbx_electron_diffrn_continuous_rotation.electron_diffrn_id**
: This data item is a pointer to the pdbx_electron_diffrn category


* **_pdbx_electron_diffrn_continuous_rotation.angle_start**
: The starting tilt angle in degrees for continuous rotation data collection.


* **_pdbx_electron_diffrn_continuous_rotation.angle_end**
: The ending tilt angle in degrees for continuous rotation data collection.


* **_pdbx_electron_diffrn_continuous_rotation.rotation_rate**
: The speed of continuous rotation measured in degrees/second


* **_pdbx_electron_diffrn_continuous_rotation.exposure_time_per_image**
: The exposure time of the rolling shutter model of the detector/camera
measured in seconds.


* **_pdbx_electron_diffrn_continuous_rotation.angle_per_image**
: Approximate angles covered by each image for continuous rotation data collection.


* **_pdbx_electron_diffrn_continuous_rotation.details**
: Additional details about the continuous rotation data collection


## pdbx_electron_diffrn_discrete_angle
Describes data collection at still discrete angles


* **_pdbx_electron_diffrn_discrete_angle.id**
: The ordinal identifier for the category


* **_pdbx_electron_diffrn_discrete_angle.electron_diffrn_id**
: This data item is a pointer to the pdbx_electron_diffrn category


* **_pdbx_electron_diffrn_discrete_angle.angle_start**
: The starting tilt angle as measured in degrees for data collection at the discrete
angles. If both crystal and beam are tilted, record the combination results of
relative angles.


* **_pdbx_electron_diffrn_discrete_angle.angle_end**
: The ending tilt angle for data collection at the discrete angles
measured in degrees. If both crystal and beam are tilted, record
the combination results of relative angles.


* **_pdbx_electron_diffrn_discrete_angle.angle_increment**
: The tilt angle increment for data collection at the discrete angles.
If both crystal and beam are tilted, record the change of the combinational
relative angles.


* **_pdbx_electron_diffrn_discrete_angle.tilt_angle_lists**
: The comma-separated complete tilt angle list for data collection at the discrete angles.
If both crystal and beam are tilted, record the combination results of relative angles.


* **_pdbx_electron_diffrn_discrete_angle.exposure_time_per_image**
: The exposure time of the rolling shutter model of the detector/camera
measured in seconds.


* **_pdbx_electron_diffrn_discrete_angle.details**
: Additional details about the continuous rotation data collection






