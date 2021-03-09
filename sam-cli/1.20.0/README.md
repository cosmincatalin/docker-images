# SAM-CLI 1.20.0

Base Image: Ubuntu 20.04 LTS (FOcal Fossa)

## Installed aptitude repositories

| Repo       | URL                                                   |
|:-----------|:------------------------------------------------------|
| deadsnakes | https://launchpad.net/~deadsnakes/+archive/ubuntu/ppa |
| Docker     | https://download.docker.com/linux/ubuntu              |

## Installed aptitude packages

| Package                    | Version                     | Description                                            |
|:---------------------------|:----------------------------|:-------------------------------------------------------|
| software-properties-common | 0.98.9.4                    | Manage the repositories that you install software from |
| apt-transport-https        | 2.0.4                       | Transitional package for https support                 |
| python3-pip                | 20.0.2-5ubuntu1             | Manages Python packages                                |
| ca-certificates            | 20210119~20.04.1            | Common CA certificates                                 |
| curl                       | 7.68.0-1ubuntu2.4           | Data transfer tool                                     |
| docker-ce                  | 5:19.03.13~3-0~ubuntu-focal | Docker Community Edition                               |

## Installed pip packages

| Package     | Version  | Description                           |
|:------------|:---------|:--------------------------------------|
| pip         | 20.2.3   | Manages Python packages               |
| setuptools  | 50.3.0   | Used for compiling python packages    |
| aws-sam-cli | 1.20.0   | Serverless Application Model cli      |
| awscli      | 1.19.23  | The AWS CLI for working with services |
| six         | 1.15.0   | Python 2 and 3 compatibility library  |


## Build and Push

* `docker build -t cosmincatalin/sam-cli:1.20.0 .`
* `docker push cosmincatalin/sam-cli:1.20.0`
