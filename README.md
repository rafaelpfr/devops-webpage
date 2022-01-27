# DevOps to Automate the Deployment of Web Pages

## Objectives
* Serve a static website on a Kubernetes cluster.
* For each commit in the website's repository, automatically a new image is built and pushed to DockerHub, then a container with this latest image should be deployed replacing the container with the old website on the cluster.

## Tools used

<p align="center">
  <img src="https://img.shields.io/badge/Ansible-000000?style=for-the-badge&logo=ansible&logoColor=white"/>
  <img src="https://img.shields.io/badge/kubernetes-326ce5.svg?&style=for-the-badge&logo=kubernetes&logoColor=white"/>
  <img src="https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white"/>
  <img src="https://img.shields.io/badge/Jenkins-D24939?style=for-the-badge&logo=Jenkins&logoColor=white"/>  
</p>


## Solution
A CentOS machine with Jenkins and Ansible configures a Kubernetes Cluster to run the latest version of the website in a Nginx container.

<Imagem com fluxograma das ferramentas usadas>


## Usage
- Jenkins needs to be configured to access: 
1) Your GitHub Repository
2) Your Docker Hub
3) The Kubernetes Cluster Machine
- After the first commit to the repository, it's necessary to do a manual Scan on Jenkins so it can obtain the configuration files and perform the build. Subsequent commits will be automatically recognized by Jenkins.

## Result
<Imagem com página estática>


## The static website is available at:
* https://onepagelove.com/avilon
