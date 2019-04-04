# AEM.Design - Ansible Roles

This repo aimed at testing Ansible Galaxy roles locally before publishing to Ansible Galaxy

## Testing

To run molecule tests enter role directory, switch to virtual env and run molecule test

```bash
cd roles/ansible-role-aem-security-test
workon aemdesign.3.7.2
molecule test
```