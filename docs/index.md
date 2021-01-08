ZTF Schedule Reporting Service
=============================

This page provides basic documentation for the public schedule reporting service deployed by the [Zwicky Transient Facility](http://ztf.caltech.edu).

## Purpose

This service provides advanced notification of the planned observations for ZTF’s public surveys, enabling coordinated observing by other facilities.

## Location

The schedule plans are available for download at `http://schedule.ztf.uw.edu/ZTF_ObsLoc_YYYY-MM-DD.json` (json) and `http://schedule.ztf.uw.edu/ZTF_ObsLoc_YYYY-MM-DD.xml` (VOTable).

Typically the schedule will be available at 00:30 UTC.

## Format

Planned observations are reported using a format recommended in the IVOA [ObsLocTAP](https://www.ivoa.net/documents/ObsLocTAP/index.html) standard (v1.0).

The IVOA recommendation calls for a queryable TAP service that is updated dynamically with the results of the observations.
While we may implement such a service in the future, at this time we are providing a single static report of each night's observing plan for the public surveys.

Information on the completed observations can be obtained [here](http://skyvision.caltech.edu/ztf/msip/nightly_summary).

The filters of the planned observation are encoded using the `em_*` parameters as follows:

| ZTF Filter | `em_min` | `em_max` | `em_res_power` |
|:-----------|:---------|:---------|:---------------|
| ZTF g | 416.700e-9 | 542.756e-9 | 3.8 |
| ZTF r | 568.941e-9 | 717.164e-9 | 4.3 |
| ZTF i | 722.536e-9 | 869.910e-9 | 5.4 |
