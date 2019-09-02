# AEM.Design - Ansible Roles

[![build_status](https://travis-ci.org/aem-design/aemdesign-ansible-roles.svg?branch=master)](https://travis-ci.org/aem-design/aemdesign-ansible-roles) 
[![github license](https://img.shields.io/github/license/aem-design/aemdesign-ansible-roles)](https://github.com/aem-design/aemdesign-ansible-roles) 
[![github issues](https://img.shields.io/github/issues/aem-design/aemdesign-ansible-roles)](https://github.com/aem-design/aemdesign-ansible-roles) 
[![github last commit](https://img.shields.io/github/last-commit/aem-design/aemdesign-ansible-roles)](https://github.com/aem-design/aemdesign-ansible-roles) 
[![github repo size](https://img.shields.io/github/repo-size/aem-design/aemdesign-ansible-roles)](https://github.com/aem-design/aemdesign-ansible-roles) 
[![docker stars](https://img.shields.io/docker/stars/aemdesign/aemdesign-ansible-roles)](https://hub.docker.com/r/aemdesign/aemdesign-ansible-roles) 
[![docker pulls](https://img.shields.io/docker/pulls/aemdesign/aemdesign-ansible-roles)](https://hub.docker.com/r/aemdesign/aemdesign-ansible-roles) 
[![github release](https://img.shields.io/github/release/aem-design/aemdesign-ansible-roles)](https://github.com/aem-design/aemdesign-ansible-roles)


This repo aimed at testing Ansible Galaxy roles locally before publishing to Ansible Galaxy

## Testing

To run molecule tests enter role directory, switch to virtual env and run molecule test

```bash
cd roles/ansible-role-aem-security-test
workon aemdesign.3.7.2
molecule test
```
