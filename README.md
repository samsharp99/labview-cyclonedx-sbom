# LabVIEW CycloneDX SBOM Toolkit

## Introduction

A LabVIEW package (VIP) for generating CycloneDX SBOMs (Software Bill of Materials) from LabVIEW source code in JSON format. SBOMs are an important part of Cybersecurity requirements to understand the 3rd party components used in a software application or system and discover and track vulnerabilities as part of an ongoing cybersecurity vulnerability assessment.

## What is CycloneDX?

CycloneDX is an international format of SBOM representation. The standard is defined in JSON, XML and Protocol Buffers. [CycloneDX Homepage](https://cyclonedx.org/)
The use of standard formats allows the SBOM to be ingested by 3rd party tools and cybersecurity scanners to detect/analyse for vulnerabilities.

## Capabilities

* LabVIEW API/Toolkit for generating a V1.5 CycloneDX JSON SBOM from a LabVIEW project
* Provide software metadata (author, description, CPE)
* Extract license information from toolkits for software license compliance
* Create/add manual components and licenses (e.g. non-LabVIEW dependencies/components)
* Support for VI Packages (VIPs) - add components from VIPC file or LabVIEW project scan (using the VIPM API)
* Support for NI Packages (NIPKG) - add components from a list of NIPKG (using the NIPM API)
* Support for Installer Build Specification Additional Installers - add components from project & build specification name
* Package built in LabVIEW 2017

## Current Limitations

* NIPKG:
    * As of LabVIEW 2017, there is no way to scan a LabVIEW project for NIPKG dependencies
    * There is no license information available for NIPKG dependencies
    * For now, the list of NIPKGs to be included in the BOM must be manually defined
* pURL:
    * NIPKG and VIP pURL standard/format has been suggested but not incorporated into the pURL specification [see issue https://github.com/package-url/purl-spec/issues/202]

## Examples

See the examples folder after installing the package.

## License

The source code and package is distributed under the MIT license © Agilent Technologies LDA UK Ltd. See LICENSE.md for more information.
