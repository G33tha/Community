#### Prerequisites to install coKreat <a href="#recommended-permissions-and-experience" id="recommended-permissions-and-experience"></a>

Sunbirded Setup 

#### Infra Requirements <a href="#infra-requirements" id="infra-requirements"></a>

* Kubernetes Cluster 
* Private GitHub repository to store ansible inventory
* Fully Qualified Domain Name (FQDN) with SSL
* Azure Storage account
* Docker hub account
* Public IP
* Vm's

#### Copy coKreat jenkins jobs <a href="#infra-requirements" id="infra-requirements"></a>

Copy cokreat jenkins jobs [coKreat-jobs](https://github.com/project-sunbird/sunbird-devops/tree/vdn-config/deploy/jenkins/jobs) to /varl/ib/jenkins/jobs folder in jenkins machine and restart jenkins service

#### update inventory <a href="#infra-requirements" id="infra-requirements"></a>

Use the following git commands sequentially to clone and update your private GitHub repository -

```bash
git clone https://github.com/project-sunbird/sunbird-devops
cd sunbird-devops
git checkout tags/release-5.1.0-vdn -b release-5.1.0-vdn
```

* Copy the directory `sunbird-devops/private_repo/ansible/inventory` to your private repo/ansible/inventory/env
* Update the files **common.yml**, **hosts**, and **secrets.yml** under **DockDev** directories. After updating, push them to your private repo branch

