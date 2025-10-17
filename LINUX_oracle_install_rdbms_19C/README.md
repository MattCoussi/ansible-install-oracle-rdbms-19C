# ORACLE / ANSIBLE - Role LINUX_oracle_install_rdbms_19C

## ROLE DEFINITION
This Ansible role deploy / patch with Combo Patch and Install Oracle RDBMS 19C on a Linux Server.



## VARIABLES NAME

```
# Setup Name DATABASE / OPATCH / PATCH - locate in folder {{ livrables_oracle_directory }}
livrables_oracle_name:
 database: "LINUX.X64_193000_db_home.zip"
 opatch: "p6880880_190000_Linux-x86-64.zip"
 patch: "p32218454_190000_Linux-x86-64_19.10.0.0.zip"

# --- Application du patch
custom_oracle_database_apply_patch: "true"

## ---------------------------------------------------------------
## - Oracle user account information
oracle_account: 
 name: "oracle"
 group_install: "oinstall"
 group_dba: "dba"
 home: "/home/oracle"
```





- 



