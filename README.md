# ansible-install-oracle-rdbms-19C
Anisble projet to install and update Oracle 19C RDBMS



# LISTE DES VARIABLES POUR LE MODELE

```
##################################################################
## -- NOM DES LIVRABLES A UTILISER

# Nom du livrable DATABASE / OPATCH / PATCH - localiser dans le dossier {{ livrables_oracle_directory }}
livrables_oracle_name:
 database: "LINUX.X64_193000_db_home.zip"
 opatch: "p6880880_190000_Linux-x86-64.zip"
 patch: "p32218454_190000_Linux-x86-64_19.10.0.0.zip"

##################################################################
## -- PERSONNALISATION DES CHOIX [TRUE/FALSE]
# VALEURS POSSIBLES:
#      custom_[value]]: "true" --> L'opération sera réalisée
#      custom_[value]]: "false" --> L'opération ne sera pas réalisée 

# --- Application du patch
custom_oracle_database_apply_patch: "true" 
```