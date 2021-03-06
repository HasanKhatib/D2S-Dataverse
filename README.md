# Design to Software - Dataverse Project
This repository contains an instance of Dataverse Project for that works as research data repository. It was cloned and configured from the [Dataverse-Docker](https://github.com/IQSS/dataverse-docker) repository from IQSS.

## Getting Started
In order to work with this repository, you will have to follow the next prerequisite to prepare the environment.
### Prerequisites
* Linux based operating system (Ubuntu)
* Check if Java 8.0 is installed to the environment, if not use this command:
`sudo apt install openjdk-8-jdk`
* Start by cloning dataverse-docker (from IQSS) to `~/` directory using this command: `https://github.com/IQSS/dataverse-docker.git`
* Then, execute the `initial.bash` file from the new cloned repository using this command `sudo ./initial.bash`.

> stick to the directory preferences if you want to benefit from `.bash` file that I will add to facilitate build and deployment, and to get the best of below instructions
* Install Docker using this command: `sudo apt install docker.io`
* Install Docker-Compose (follow the steps in [this article](https://linuxize.com/post/how-to-install-and-use-docker-compose-on-ubuntu-18-04/) to do so
* Go to the cloned directory (`~/dataverse-docker`) and perform the next commands to build and start the dataverse instance:
  * sudo docker-compose build
  * sudo docker-compose up

Now you can go to [localhost:8085](http://localhost:8085) and start your instance of dataverse.

### Development Environment
Want to configure this installed and running instance? follow the next steps to install the preferred IDE and to deploy new instances according to your configuration:
* Install [intellij Ultimate](https://www.jetbrains.com/idea/download/#section=linux) on your environment (you can use your students' email to get a license for one year)
* Clone D2S-Dataverse repository to home directory using this command `https://github.com/samihabakri/D2S-Dataverse.git` , which will generate new folder named `D2S-Dataverse`
* Import D2S-Dataverse project to intellij
* Import maven dependencies from the pom.xml file then generate sources
* Edit and code whatever you need, then execute install command in the Maven command line
* Copy the *.war file to `~/dataverse-docker/dataversedock/dv/deps/`
* Perform build and up commands again to re-deploy dataverse with the new war file

## License
This repository follows the license used in the original repository from IQSS.

Copyright 2019 TUWien D2S Group

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
