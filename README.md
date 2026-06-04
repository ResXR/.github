<div align="center">

# ResXR

**Research with XR**

Open-source infrastructure for reproducible, standardized XR behavioral research.

[![License](https://img.shields.io/badge/License-Apache_2.0-475569?style=flat-square)](https://www.apache.org/licenses/LICENSE-2.0)
[![Status](https://img.shields.io/badge/Status-Pre--release-64748b?style=flat-square)](https://resxr.org)
[![IEEE VR 2026](https://img.shields.io/badge/IEEE_VR_2026-Research_Demo-4338ca?style=flat-square)](https://doi.org/10.1109/VRW70859.2026.00377)

[Website](https://resxr.org) &nbsp;·&nbsp; [Unity Template](https://github.com/ResXR/resxr-unity-research-template) &nbsp;·&nbsp; [Python Pipeline](https://github.com/ResXR/resxr-python-pipeline)

</div>

---

XR research has grown quickly, but the field has not converged on shared conventions for how experimental data is collected, organized, and validated. Custom-built experiments produce custom-formatted output, so two studies on identical hardware can yield datasets that another lab cannot easily combine or reanalyze. ResXR provides a complete, transparent path from an immersive experiment on a standalone Meta Quest headset to an analysis-ready, [Motion-BIDS](https://bids.neuroimaging.io/)-formatted dataset with an accompanying quality report.

The design takes inspiration from [BIDS](https://bids.neuroimaging.io/) and [fMRIPrep](https://fmriprep.org/) in neuroimaging: standardize how data is organized and validated, while leaving researchers full freedom over how they design their experiments.

<br>

## Two independent components

ResXR is **two components that share no code, imports, or build system.** Their only connection is a data contract: the CSV and JSON files the template writes and the pipeline reads. Either component can be adopted on its own.

<table>
<tr>
<td width="50%" valign="top">

#### Unity Template
[resxr-unity-research-template](https://github.com/ResXR/resxr-unity-research-template)

A glass-box Unity experiment scaffold for Meta Quest standalone headsets (Quest 2, Quest 3, Quest Pro). Streams multimodal tracking data (head, hands, eyes, face) and ships with three ready-to-run paradigms: Binary Choice, Maze Navigation, and Museum Viewing.

</td>
<td width="50%" valign="top">

#### Python Pipeline
[resxr-python-pipeline](https://github.com/ResXR/resxr-python-pipeline)

Post-experiment processing that turns recorded sessions into Motion-BIDS datasets, with validation, quality-flag-based preprocessing, standardized export, and a self-contained HTML quality report.

</td>
</tr>
</table>

<br>

## What it produces

ResXR is organized into four functional stages:

| Stage | Description | Component |
|:--|:--|:--|
| **1. Base Template** | A reproducible experiment scaffold that continuously streams multimodal tracking data to persistent storage. | Unity Template |
| **2. Validation** | Automated integrity checks that raise quality flags. | Python Pipeline |
| **3. Preprocessing** | Quality-flag-based masking that produces clean derivative datasets. | Python Pipeline |
| **4. Standardization and reporting** | Motion-BIDS export alongside a visual quality report. | Python Pipeline |

The glass-box design means researchers own and can inspect every part of the experiment and the data-collection logic. The architecture exposes explicit extension points for new sensor modalities and validation procedures.

<br>

## Getting started

Each repository has its own README with installation and usage:

- **Build and run experiments:** [resxr-unity-research-template](https://github.com/ResXR/resxr-unity-research-template)
- **Process recorded sessions:** [resxr-python-pipeline](https://github.com/ResXR/resxr-python-pipeline)

<br>

## Project status

A manuscript describing ResXR is in preparation. A research demonstration was published at IEEE VR 2026 ([DOI: 10.1109/VRW70859.2026.00377](https://doi.org/10.1109/VRW70859.2026.00377)). APIs may change ahead of a tagged release.

<br>

## License and contributing

Released under **Apache 2.0** with a Contributor License Agreement, keeping academic and downstream reuse open while preserving a clear contribution path. Contributions are welcome; see each repository's contributing guide.

<br>

<div align="center">
<sub>

Developed at the [Schonberg Lab](https://schonberglab.tau.ac.il/), Tel Aviv University &nbsp;·&nbsp; resxr.toolkit@gmail.com

</sub>
</div>