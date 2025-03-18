## FIDOpower Overview

FIDOpower is a proposed rebrand and update of OpenFIDO, a CEC-funded project which was adopted by LF Energy as an open-source project. The original abstract for OpenFIDO is as follows:

<I>
California utilities, customers, consulting engineers and regulators need to exchange power system data, yet this can be cumbersome and error prone, raising barriers to effective resource integration, curbing growth of these resources, and limiting how quickly California can reach its climate change mitigation goals. 

OpenFIDO provides a framework for interorganizational data exchange, data and model synthesis, and system performance analysis across multiple power systems tools. OpenFIDO is used to (1) collect data from a wide variety of sources, (2) transfer model and telemetry data between tools, and (3) enable creation of permanently available reproducible results. 

OpenFIDO allows utility planners and grid researchers to move data quickly between applications. OpenFIDO supports emerging user groups including system integrators and aggregators who use multiple tools to analyze distributed energy resource grid impacts, and governments and agencies using models for oversight and planning clean energy deployments. 

Project results included (1) identifying data analysis requirements needed to support critical electricity use-cases, (2) delivering a new open-source utility data interoperability and analytics workflow management platform at Southern California Edison, and (3) delivering an open source analytic tool delivery environment for workstation, on-premises server, and cloud infrastructure to enable key utility use-cases for commercialization by Linux Foundation Energy.
</I>

The technology on which OpenFIDO was built is fast becoming obsolete and difficult to maintain. The framework for development is over 10 years old and the workflow methodology lacks the formal development now available in modern tools such as Marimo. Marimo was developed over the last few years with funding in part from SLAC National Accelerator Laboratory as a solution to many of the problems and challenges uncovered during the development of OpenFIDO.

## About Marimo

We propose to redeploy all the OpenFIDO pipelines as Marimo notebooks and brand this new version of OpenFIDO under the name FIDOpower. This approach has the following advantages over the existing OpenFIDO deployment:

* Eliminates the need to develop and deploy a UI framework. The existing OpenFIDO implementation has a custom UI that must be maintained and deployed on an AWS platform. These cost LF Energy and the project contributors time and money that is better focused on the development and validation of workflows and pipelines.

* Solves the workflow problem using formal methods. The current version of OpenFIDO has a very limited implementation of the workflow solution. Marimo dynamically executes code in a deterministic order to ensure that there are no hidden states or orphan results.

* Introduces advanced UI elements. OpenFIDO has very few UI elements for data entry by the user. Marimo notebooks come with a very large collection of advanced UI elements for complex data input and viewing.

* Standardizes pipeline code in Python. OpenFIDO deployments do not use Python as the native language for implementing pipelines (although it does support Python). Marimo is a pure Python notebook environment.

* Uses reactive UI and data inputs. Marimo can automatically update results when inputs from the user or data sources change. This is not available in OpenFIDO, where the user must always request a new run of a pipeline, even when doing basic exploration and analysis where such a feature is intuitively obvious and highly valuable.

* Marimo supports the most important functional requirements in OpenFIDO, specifically

* Marimo supports local, hosted, and browser-based deployment models. 

* Marimo automatically manages required packages and modules. 

* Marimo supports large-scale data processing and data-sharing. 

* Marimo notebooks enable highly reproducible results. 

* Marimo notebooks are compatible with git to enable collaboration and histories.

* Marimo notebooks can be deployed as either scripts or apps.

* Marimo is used by a large community ensuring long-term support and maintenance.

* Marimo notebooks provide a fast and easy path from development to deployment.

## Work Plan

1. Branding

- [x] Adopt new project name.

- [x] Complete new project webpage form for LF Energy (submitted)

- [x] Complete new project logo form for LF Energy (submitted)

1. Github

- [x] Create new organization

- [ ] Update project documents to use new name

- [x] Update project description to introduce Marimo

1. Pipelines

- [ ] Refactor python pipelines as a Python package

- [ ] Convert pipelines in other languages to Python package

- [ ] Convert UI manifests to Marimo notebooks

- [ ] Update pipeline validation process

1. Deployment

- [ ] Convert AWS deployment to Marimo deployment

- [ ] Write How-To guides to local and hosted deployments

1. Community

- [ ] Engage with Marimo team to disseminate FIDOpower notebooks

- [ ] Work with Marimo team to build energy-centric community of FIDOpower users and developers

