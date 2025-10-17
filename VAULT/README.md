# ERA / ANSIBLE - Rôle VAULT

## Définition du rôle
Ce rôle permet de traiter des éléments dans VAULT CHU. Il permet aussi bien au travers de la méthode LIST de récupérer des crédentials ou bien au travers de la méthode UPDATE d'ajouter ou mettre a jour des credentials.
Le rôle est appelé avec des variables en arguments pour traiter les credentials les uns aprés les autres.

#### _Liste des rôles nécessaire (précédent) pour l'execution de ce rôle_
- ERA_API_ORA_DBSERVER_get_info : pour récupérer les informations sur le dbserver pour faire les modifications
ou
- ERA_API_ORA_DATABASE_create : Fait au moment du provisionnement d'une base de données


#### _Liste des variables_

##### En entrée du rôle
- tmp_vault_path: Chemin dans Vault
- tmp_vault_user: Utilisateur a get/ajouter/maj dans VAULT
- tmp_vault_password: Mot de passe de l'utilisateur a ajouter/maj dans VAULT
- tmp_vault_method: Méthode de traitement du rôle update ou liste de crédentials (4 valeurs possibles LIST, UPDATE,GENERATE)
- tmp_vault_gen_password_lenght:  longueur du mot de passe que l'on souhaite générer
- tmp_vault_gen_password_digits:  Nombre de digit que l'on souhaite dans le mot de passe
- tmp_vault_gen_password_symbols:  Nombre de symbole que l'on souhaite dans le mot de passe
- tmp_vault_gen_password_policy: Nom de la policy pour générer une mot de passe

##### En sortie du rôle
- tmp_list_vault_credential : Lorsqu'on utilise l'ancienne méthode LIST, les credentials sont transmis au travers de cette variable.
- tmp_vault_credential : Lorsqu'on utilise la méthode LIST_NEW_VAULT, le mot de passe du compte est transmis au travers de cette variable.
##### Dans le rôle
- tmp_vault_token : Récupération d'un token VAULT
- vault_maj_credential : Formattage du body json pour ajout/update de credentials

##### Dans le group vars
- vault_info.url: URL du VAULT CHU
- vault_info.version: Version API VAULT CHU
- vault_path.* : Chemin suivant la données a créer/maj


##### Dans le scénario
- dbserver_name : Nom du dbserver ou il faut réaliser les modifications
- tmp_admin_vault_user : Compte pour ajout credentials dans VAULT
- tmp_admin_vault_password : Mot de passe du compte pour ajout credentials dans VAULT



