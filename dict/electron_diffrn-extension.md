# Electron Diffraction Dictionary Update Documentation

---
Title: Electron Diffraction Dictionary Extension  
Author: C. Shao, E. Peisach  
Date: 21-Oct-2025  
email: chenghua.shao@rcsb.org  
---

This document provides an overview of extensions to support metadata collection and annotation of PDB structures resolved by Electron Diffraction methods, especially by 3D ED/MicroED method. Listed below are the NEW data items designed for Electron Diffraction methods.

## pdbx_exptl_subtype
Data items in the PDBX_EXPTL_SUBTYPE category record
details about the method subtype under the primary
method recorded in _exptl.method


* **_pdbx_exptl_subtype.exptl_method**
: This data item is a pointer to _exptl.method in the EXPTL category.


* **_pdbx_exptl_subtype.method_type**
: The subtype of the method used in the experiment. The
subtype should be a variance of the primary method
recorded in the _exptl.method item, with distinctive
technical applications and significant scientific
impacts.

    *Enumeration:*

      * Microcrystal Electron Diffraction
      * 2-Dimensional Electron Crystallography


* **_pdbx_exptl_subtype.details**
: Details about the method subtype.


## pdbx_exptl_crystal_process
Data items in the pdbx_exptl_crystal_process category
record details of the post-crystallization process to
prepare specific crystal samples such as microcrystals
for subsequent diffraction experiments.


* **_pdbx_exptl_crystal_process.id**
: The ordinal identifier for the category


* **_pdbx_exptl_crystal_process.crystal_id**
: This data item is a pointer to the _exptl_crystal.id


* **_pdbx_exptl_crystal_process.microcrystal_method**
: The method used to produce microcrystals for
diffraction experiments, if applicable.

    *Enumeration:*

      * Vortexing
      * Other
      * FIB milling
      * Naturally grown
      * Sonication


* **_pdbx_exptl_crystal_process.microcrystal_instrument**
: The instrument used to produce microcrystals for the experiments, if applicable.


* **_pdbx_exptl_crystal_process.microcrystal_min_dim**
: The minimal dimension of the final crystal ready for
diffraction experiments. For example, for
microcrystals processed by FIB milling, this item
refers to the thickness of the thin lamella.


* **_pdbx_exptl_crystal_process.microcrystal_max_dim**
: The maximal dimension of the final crystal ready for
diffraction experiments. For example, for
microcrystals processed by FIB milling, this item
refers to the length of the thin lamella.


* **_pdbx_exptl_crystal_process.microcrystal_description**
: Characteristics of the final crystal ready for diffraction experiments, e.g. shape.


* **_pdbx_exptl_crystal_process.details**
: The details about the crystal process.


## pdbx_exptl_crystal_cryo_treatment
Data items in the PDBX_EXPTL_CRYSTAL_CRYO_TREATMENT category
record details cryogenic treatments applied to this crystal.


* **_pdbx_exptl_crystal_cryo_treatment.cryogen**
: The name of cryogen used for vitrification

    *Enumeration:*

      * ETHANE
      * NITROGEN
      * OTHER


## diffrn_measurement
Data items in the DIFFRN_MEASUREMENT category record details
about the device used to orient and/or position the crystal
during data measurement and the manner in which the diffraction
data were measured.


* **_diffrn_measurement.pdbx_angle_start**
: The starting angle for crystal rotation.


* **_diffrn_measurement.pdbx_angle_end**
: The ending angle for crystal rotation.


* **_diffrn_measurement.pdbx_rotation_rate**
: The speed of crystal rotation.


* **_diffrn_measurement.pdbx_exposure_time_per_image**
: The exposure time per image for the crystal and
detector/camera.


* **_diffrn_measurement.rotation_mode**
: Originated from IUCr Electron Diffraction CIF
extension. Code describing the technique used to
sample as completely as possible the accessible range
of reciprocal space. Rotation mode indicates the
detector records diffracted intensities continuously
while the sample is rotated. Stepwise model indicates
the detector records diffracted intensities while the
sample is stationary.

    *Enumeration:*

      * rotation
      * stepwise


* **_diffrn_measurement.method_precession**
: Originated from IUCr Electron Diffraction CIF
extension. Flag indicating if the radiation beam
illuminates the sample at an angle that is rotated
about a precession axis.

    *Enumeration:*

      * N
      * Y


* **_diffrn_measurement.sample_tracking**
: Originated from IUCr Electron Diffraction CIF
extension. Flag indicating if a tracking method to
follow the crystal was used in the data
acquisition. Typically used to track very small
crystals in electron diffraction experiments.

    *Enumeration:*

      * N
      * Y


* **_diffrn_measurement.sample_tracking_method**
: Originated from IUCr Electron Diffraction CIF
extension. Description of the method used to follow
the crystal during data collection.


## pdbx_diffrn_ed
Data items in the PDBX_DIFFRN_ED record details specific to electron diffraction method.


* **_pdbx_diffrn_ed.id**
: This ordinal identifier for the category


* **_pdbx_diffrn_ed.diffrn_id**
: This data item is a pointer to the _diffrn.id


* **_pdbx_diffrn_ed.electron_source**
: The source of electrons, i.e. the electron gun

    *Enumeration:*

      * OTHER
      * FIELD EMISSION GUN
      * LAB6


* **_pdbx_diffrn_ed.beam_diameter_sample_plane**
: The electron beam diameter at the sample plane


* **_pdbx_diffrn_ed.camera_length**
: The product of the objective focal length and the
combined magnification of the intermediate and projector
lenses when the microscope is operated in the
diffraction mode.


* **_pdbx_diffrn_ed.recording_mode**
: The mode of the detector for electron diffraction recording, e.g.
Electron Counting (Event) mode, Linear (Integrating) mode

    *Enumeration:*

      * Other
      * Integrating
      * Electron Counting


* **_pdbx_diffrn_ed.fluence_rate**
: Fluence rate, or flux density at the sample plane


* **_pdbx_diffrn_ed.fluence_accumulated**
: Total fluence at the sample plane


* **_pdbx_diffrn_ed.c2_aperture_diameter**
: C2 aperture diameter


* **_pdbx_diffrn_ed.sa_aperture_diameter**
: Select Area aperture diameter


* **_pdbx_diffrn_ed.energyfilter_name**
: The name of the energy filter


* **_pdbx_diffrn_ed.energyfilter_upper**
: The energy filter range upper value in electron volts (eV)
set by the specrometer


* **_pdbx_diffrn_ed.energyfilter_lower**
: The energy filter range lower value in electron volts (eV)
set by the specrometer


* **_pdbx_diffrn_ed.details**
: Details of the electron diffration process






