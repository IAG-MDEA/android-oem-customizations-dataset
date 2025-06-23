# Android OEM TLS Component Customization Dataset

This repository contains structured results from our differential analysis pipeline for TLS-related AOSP components. The analysis is part of our broader study on [Android OEM Customizations](https://github.com/IAG-MDEA/android-oem-customizations-pipeline), aimed at uncovering vendor-introduced changes to core Android libraries and their potential implications on security and interoperability.

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

## Contents

The dataset is organized as follows:

### 🔍 Function & Symbol-Level Diffs

These CSV files contain detailed results of function- and symbol-level differences between AOSP baseline libraries and their OEM-modified counterparts:

- `Conscrypt function level diff results.csv`  
- `JSSE function level diff results.csv`  
- `libcrypto symbol tree diff results.csv`  
- `libssl symbol tree diff results.csv`  

Each entry highlights added, removed, or modified elements and supports downstream inference of implementation purpose and potential security impacts.

### AOSP Evolution Timeline

The `tls-component-aosp-timeline/` directory provides AOSP-level evolution data (JSON) for each TLS-relevant library:

- `conscrypt_timeline.json`  
- `jsse_timeline.json`  
- `libcrypto_timeline.json`  
- `libssl_timeline.json`  

These timelines are useful for contextualizing when specific APIs were introduced or deprecated upstream, helping differentiate between legacy patches and novel OEM additions.

## Purpose

By analyzing OEM modifications to key TLS components—**Conscrypt**, **JSSE**, **libcrypto**, and **libssl**—we aim to:

- Understand **the intended functionality** of non-AOSP additions.
- Evaluate their **security implications** (e.g., bypasses, legacy fallbacks, weak crypto).
- Map **API implementation strategies** across vendors and Android versions.


## License

Licensed under the  [GNU GPLv3](LICENSE) license.

## Funding support

Part of this research was supported by the Spanish National Cybersecurity Institute (INCIBE) under <i>Proyectos Estratégicos de Ciberseguridad -- CIBERSEGURIDAD EINA UNIZAR</i> and by the Recovery, Transformation and Resilience Plan funds, financed by the European Union (Next Generation).

![Funding logo](misc/images/BandaLogos_INCIBE_es-100.jpg)
