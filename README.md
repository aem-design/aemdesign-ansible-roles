# AEM.Design - Ansible Roles

[![build_status](https://travis-ci.org/aem-design/aemdesign-ansible-roles.svg?branch=master)](https://travis-ci.org/aem-design/aemdesign-ansible-roles) 
[![github license](https://img.shields.io/github/license/aem-design/aemdesign-ansible-roles)](https://github.com/aem-design/aemdesign-ansible-roles) 
[![github issues](https://img.shields.io/github/issues/aem-design/aemdesign-ansible-roles)](https://github.com/aem-design/aemdesign-ansible-roles) 
[![github last commit](https://img.shields.io/github/last-commit/aem-design/aemdesign-ansible-roles)](https://github.com/aem-design/aemdesign-ansible-roles) 
[![github repo size](https://img.shields.io/github/repo-size/aem-design/aemdesign-ansible-roles)](https://github.com/aem-design/aemdesign-ansible-roles) 


This repo aimed at testing Ansible Galaxy roles locally before publishing to Ansible Galaxy

## Cloning

This repo links all roles using git submodules. When cloning this repo you need to use the `--recursive` flag to tell git to pull all the submodules.

`git clone --recursive git@github.com:aem-design/aemdesign-ansible-roles.git`

## Migrating old module to Molecule v2

0. Before you start please read these 
    - [Testing Ansible automation with molecule](https://redhatnordicssa.github.io/how-we-test-our-roles)
    - [Moelcule Configuration](https://molecule.readthedocs.io/en/stable/configuration.html#) 

1. Create a new repo with README in github

2. add new repo as submodule to the project

```bash
git submodule add git@github.com:aem-design/ansible-role-aem-toughday.git roles/ansible-role-aem-toughday
```

3. Use molecule to init the new module

```
cd roles/tmp
workon aemdesign.3.7.4
pip install molecule
molecule init role -r ansible-role-aem-toughday
```

4. Update role config in temp folder

5. Run `molecule converge` while you are developing the role

```
molecule converge
<do some work on the role>
molecule converge
<see that some changes didn't work>
molecule lint
<fix all the typos>
molecule converge
<see everything working well, commit my changes>
molecule test
<see everything working well, commit my changes>
molecule converge
<idempotence check - make sure Ansible doesn't report any changes on a second run>
molecule destroy
```

6. Manually move updated molecule config into the sumbodule and commit 

7. Run `molecule test` to full process works, if it does not don't bother committing.

Sub folder with your new role will be created.

## Testing

To run molecule tests enter role directory, switch to virtual env and run molecule test

```bash
cd roles/ansible-role-aem-verify
workon aemdesign.3.7.2
molecule test
```
