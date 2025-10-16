# ORACLE / ANSIBLE - Rôle LINUX_oracle_install_rdbms_19C

## Définition du rôle
Ce rôle permet de déployer d'instaler et de patcher une version Oracle Database 19C


## Dépendances

#### _Liste des rôles nécessaire (précédent) pour l'execution de ce rôle_
- livrables_oracle_name.database : Nom du livrable Oracle Database 19C à décompresser et installer
- livrables_oracle_name.opatch : Nom du livrable Oracle OPatch à décompresser et installer
- livrables_oracle_name.patch : Nom du livrable Oracle Database 19C [PATCH] à décompresser et installer



#### _Liste des variables_
##### Dans le rôle
- oracle_rpm_preinstall: Nom du RPM pour les prérequis Oracle 19C
- rdbms_19C_space : Espace nécessaire en Ko pour le kernel 19C
- livrables_temp.fs : FS ou copier et décompresser les livrables en local sur le serveur Linux
- livrables_temp.folder : Dossier ou copier et décompresser les livrables en local sur le serveur Linux

- livrables_temp.space : Espace nécessaire en local sur le serveur pour les livrables
- root_directory : Localisation du point de montage racine des installations
- oracle_home : Localisation des la ORACLE_HOME Oracle Database 19C
- oracle_base: Localisation du point de montage ou se trouve les produits Oracle

##### Dans le group vars
- oracle_account.name : Nom de l'utilsisateur Oracle
- oracle_account.group_install : Nom du groupe d'installation
- oracle_account.dba : Nom du groupe dba


##### Dans le scénario
- 



