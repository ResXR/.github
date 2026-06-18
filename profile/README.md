<div align="center">

# ResXR

**Research with XR**

Open-source infrastructure for reproducible, standardized XR behavioral research.

[![License](https://img.shields.io/badge/License-Apache_2.0-475569?style=flat-square)](https://www.apache.org/licenses/LICENSE-2.0)
[![Status](https://img.shields.io/badge/Status-Pre--release-64748b?style=flat-square)](https://resxr.org)
[![Docs](https://img.shields.io/badge/docs-docs.resxr.org-047857?style=flat-square)](https://docs.resxr.org)
[![IEEE VR 2026](https://img.shields.io/badge/IEEE_VR_2026-Research_Demo-4338ca?style=flat-square)](https://doi.org/10.1109/VRW70859.2026.00377)


</div>

---

While XR research has grown quickly, the field lacks shared conventions for collecting, organizing, and validating experimental data. Custom-built experiments often produce highly specific output formats, making it difficult for other labs to combine or reanalyze datasets. 

**ResXR** solves this by providing a transparent path from an immersive experiment on a standalone Meta Quest headset to an analysis-ready, [Motion-BIDS](https://bids.neuroimaging.io/)-formatted dataset. Inspired by [fMRIPrep](https://fmriprep.org/), ResXR standardizes data organization and validation while granting researchers complete freedom over their experimental design.

<br>

## Two Independent Components

ResXR consists of two components that share no code, imports, or build system. They are connected strictly by a data contract (CSV and JSON files). You can adopt either component independently.

### 🎮 [Unity Template](https://github.com/ResXR/resxr-unity-research-template)
> A glass-box Unity experiment scaffold for Meta Quest standalone headsets (Quest 2, 3, and Pro). It streams multimodal tracking data (head, hands, eyes, face) and ships with three ready-to-run paradigms: Binary Choice, Maze Navigation, and Museum Viewing.

### 🐍 [Python Pipeline](https://github.com/ResXR/resxr-python-pipeline)
> Post-experiment processing that transforms recorded sessions into Motion-BIDS datasets. Includes automated validation, quality-flag-based preprocessing, standardized export, and a self-contained HTML quality report.

<br>

## How It Works

ResXR is organized into four functional stages. The glass-box architecture allows researchers to inspect or extend every part of the data-collection logic and validation procedures.

| Stage | Description | Component |
|:---|:---|:---|
| **1. Base Template** | A reproducible experiment scaffold continuously streaming multimodal data to persistent storage. | Unity Template |
| **2. Validation** | Automated integrity checks that raise quality flags. | Python Pipeline |
| **3. Preprocessing** | Quality-flag-based masking that produces clean derivative datasets. | Python Pipeline |
| **4. Standardization** | Motion-BIDS export alongside a visual HTML quality report. | Python Pipeline |

<br>

## Getting Started
You can find complete setup, usage, and developer guides at our documentation hub:
*   **📖 Read the Documentation:** https://docs.resxr.org

Each repository contains its own installation and usage instructions:
*   **Build and run experiments:** [resxr-unity-research-template](https://github.com/ResXR/resxr-unity-research-template)
*   **Process recorded sessions:** [resxr-python-pipeline](https://github.com/ResXR/resxr-python-pipeline)

<br>

## Project Status

A manuscript detailing the ResXR toolkit is currently in preparation for publication. A research demonstration of this pipeline was presented at IEEE VR 2026 ([DOI: 10.1109/VRW70859.2026.00377](https://doi.org/10.1109/VRW70859.2026.00377)). *Please note that APIs may change prior to a stable, tagged release.*

<br>

## License & Contributing

Released under **Apache 2.0** with a Contributor License Agreement to keep academic reuse open while preserving a clear contribution path. Contributions are welcome; please see the contributing guide in each respective repository.

<br>

<div align="center">

## Contact & Support
For inquiries, collaborations, or support, reach out via email:<br>
📧 **resxr.toolkit@gmail.com**

<br>

<sub>
Developed by the <a href="https://schonberglab.tau.ac.il/">Schonberg Lab</a>, Tel Aviv University.
</sub>

</div>
