# industrial-automation-frameworks
# NetCICD #
## About ##

NetCICD is an ansible based toolset to facilitate continuous  (...) for infrastructure.

We think practices used in DevOps and CI/CD can be adapted for infrastructure and add significant value. NETCICD is our attempt to make these practices accessible for infrastructure, and networking in particular.

NETCICD takes an industrial automation approach to network development and service deployment, with as ultimate goal: to be able to do CI/CD:

- Continuous Integration of new functionality, including automated testing
- Continuous Delivery of new, tested functionality for deployment to production
- Continuous Deployment: all new templates and workflows are automatically deployed to production

## Use ##

There are two ways of using NetCICD:

* Within the [CICD Toolbox](https://github.com/Devoteam/CICD-toolbox)
* Locally with CML

### Within the [CICD Toolbox](https://github.com/Devoteam/CICD-toolbox) ###
To use NETCICD within the toolbox, just install the toolbox as per the installation instructions and you are good to go.

### Locally ### 
If you do not want to install the local toolset and just want to play with NetCICD and CML, you can import the labs in the cml2 directory tp play with. The labs all have a desktop configured as jumpshot.

### More info ###
For more detailed info, see the [wiki](https://github.com/Devoteam/NetCICD/wiki). I put weird things in [Observations](https://github.com/Devoteam/NetCICD/wiki/Observations)

## Background ##
The first implementation was made in 2018 and was presented at [Cisco Live 2018 in Barcelona](https://www.ciscolive.com/c/dam/r/ciscolive/emea/docs/2019/pdf/BRKSDN-2158.pdf). The video of the session can be seen after logging in.

Since then, we used the toolchain, but in that process we experienced that maintaining a tool chain supporting NetCICD remains a challenge. As a result, the [CICD Toolbox](https://github.com/Devoteam/CICD-toolbox) was created, which is being developed by DevOps Engineers within Devoteam. It contains all tools required (git, Jenkins, Nexus and Keycloak for SSO) to make the NetCICD environment run locally (a supported commercial version is available too, contact networkautomation at devoteam.nl for more information). The tools are configured for NetCICD.

We are working to include [Argos](https://www.argosnotary.com/) to include a continuous auditing mechnism so that it becomes possible to prove that the deployment (git commit) you are running operationally is actually the version tested and for which the test report can be found in your Nexus repo.

Both NetCICD and the NetCICD Developer Toolbox are aimed towards local deployment, for example on your laptop or within the walled garden of your operations environment.

If you feel you can add to the framework, please do so.

#### License #### 
This source Code Form is subject to the terms of the Mozilla Public License, V2.0. If a a copy ofthe MPL was not distributed with this file, you can obtain one at https://mozilla.org/MPL/2.0/.

#### Copyright ####
(c) Software Association

## Installation ##
Installation should be done by installing the [CICD Toolbox](https://github.com/Devoteam/CICD-toolbox). This repo can be found in the Git environment under the organisation Infraautomator.

## Environment ##
NetCICD is developed on a Ubuntu 20.04.1 Desktop laptop with CML Personal edition version 2.1.

CML can be stock install with refplat_p-20201110-fcs.iso. CML is not down/upward compatible for reference platforms ([see the CML documentation, question 7](https://developer.cisco.com/docs/modeling-labs/#!faq/installation-questions)).

I use one additional network for compatibility with the DevNet sandboxes: 10.10.20.0/24. The host running VMWare must have IPaddress 10.10.20.50, [see the VMWare documentation.](https://www.vmware.com/support/ws55/doc/ws_net_advanced_ipaddress.html)

For more information see the wiki attached to this repo.

































































