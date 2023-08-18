    # # # Distribution Statement A. Approved for public release. Distribution unlimited.
    # # #
    # # # Author:
    # # # Naval Research Laboratory, Marine Meteorology Division
    # # #
    # # # This program is free software: you can redistribute it and/or modify it under
    # # # the terms of the NRLMMD License included with this program. This program is
    # # # distributed WITHOUT ANY WARRANTY; without even the implied warranty of
    # # # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the included license
    # # # for more details. If you did not receive the license, for more information see:
    # # # https://github.com/U-S-NRL-Marine-Meteorology-Division/

Data Fusion GeoIPS Plugin Template
============================================

This template repository contains everything necessary to create a fully compatible
GeoIPS Plugin Package, with a focus on creating products using the data_fusion package.
Currently, only the "layered" image functionality is templated, but in the future we
will add templates for pure data fusion products (ie, algorithms that take in more
than one data type), stitched imagery products, as well as layered imagery.

Each file within this repository contains appropriate modification instructions.

To create your own functional data fusion plugin for GeoIPS, follow the
[step by step instructions](./docs/template_instructions.rst) for
modifying the template files within this repo.

@ Once this repository has been set up properly, you can remove this "Data Fusion
GeoIPS Plugin Template" section in the README.md, leaving the appropriate
content for your package's README file.

@package@ GeoIPS Plugin
==========================

The @package@ package is a GeoIPS-compatible plugin, intended to be used within
the GeoIPS ecosystem.  Please see the
[GeoIPS Documentation](https://github.com/NRLMMD-GEOIPS/geoips#readme)
for more information on the GeoIPS plugin architecture and base infrastructure.

Package Overview
-----------------

The @package@ plugin provides the capability for

@ Please include a brief description of what capability this package provides.

@ This section should be no more than 1-2 paragraphs, if you have additional
@ information to include, please include in a "docs" subdirectory.

@ Example overview:

@ The template_fusion_plugin package provides template files which can be used to
@ create a fully compatible GeoIPS plugin which creates arbitrarily layered imagery,
@ using the data_fusion plugin package for the layering functionality.
@ Future updates to the template_fusion_plugin package will provide additional
@ templates for fusion algorithms and stitched imagery.

System Requirements
---------------------

* geoips >= 1.10.0
* data_fusion >= 1.10.0
* Test data repos contained in $GEOIPS_TESTDATA_DIR for tests to pass.
* @ Add any additional system requirements, such as gfortran, etc

IF REQUIRED: Install base geoips package
------------------------------------------------------------
SKIP IF YOU HAVE ALREADY INSTALLED BASE GEOIPS ENVIRONMENT AND DATA_FUSION PLUGIN

If GeoIPS Base and the data_fusion packages are not yet installed, follow the
[installation instructions](https://github.com/NRLMMD-GEOIPS/data_fusion#readme)
within the data_fusion source repo for installing both the
GeoIPS base package, and the data_fusion plugin.

Install @package@ package
----------------------------
```bash

    # Ensure GeoIPS Python environment is enabled.

    git clone https://github.com/NRLMMD-GEOIPS/@package@ $GEOIPS_PACKAGES_DIR/@package@

    pip install -e $GEOIPS_PACKAGES_DIR/@package@
```

Test @package@ installation
-----------------------------
```bash

    # Ensure GeoIPS Python environment is enabled.

    # This script will run ALL tests within this package
    # @ You can add additional individual test calls if desired
    # @  (rather than forcing the user to run the full test)
    $GEOIPS_PACKAGES_DIR/@package@/tests/test_all.sh
```
