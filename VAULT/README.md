# ANSIBLE VAULT - Role VAULT

## ROLE DEFINITION
This role give the power to work with Hashicorp Vault API to get or update/create secret in Vault.

The first step of this role is to get a Vault Token with Username/Password. After getting a valid Token, the role is able to GET/UPDATE/ADD secret in Vault

### Examples

#### Generate a password with Vault API
```
- name: "Generate password for a user by Vault API and a Policy"
  ansible.builtin.include_role:
   name: VAULT
  vars:
   tmp_vault_method: "GENERATE"
   tmp_vault_gen_password_policy: "my_policy"
  no_log: "{{ ansible_no_log }}"
```

#### Add a secret in Vault by API
```
- name: "Add or Update a secret in Vault by API"
  ansible.builtin.include_role:
    name: VAULT
  vars:
    tmp_vault_path: "secret/data/linux/myserver"
    tmp_vault_user: root
    tmp_vault_password: "MY_PASSWORD"
    tmp_vault_method: "UPDATE"
  no_log: "{{ ansible_no_log }}"
```
#### Get a secret in Vault by API
```
- name: "Get Secret in Vault by API"
  ansible.builtin.include_role:
    name: VAULT
  vars:
    tmp_vault_path: "secret/data/linux/myserver"
    tmp_vault_user: "myuser"
    tmp_vault_method: "LIST"
- name: "Create variable for password get from Vault Api"
  ansible.builtin.set_fact: 
   tmp_myuser_pwd: "{{ tmp_vault_credential }}"
  no_log: "{{ ansible_no_log }}"
```