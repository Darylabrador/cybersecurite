## Permission spécial

Les autorisations spéciales constituent un quatrième niveau d'accès en plus de l'utilisateur, du groupe et des autres. Les autorisations spéciales permettent des privilèges supplémentaires sur les ensembles d'autorisations standard (comme son nom l'indique). Il existe une option d'autorisation spéciale pour chaque niveau d'accès discuté précédemment. 

## SUID précision

Communément appelée SUID, l'autorisation spéciale pour le niveau d'accès utilisateur a une seule fonction : un fichier avec SUID s'exécute toujours en tant qu'utilisateur propriétaire du fichier, quel que soit l'utilisateur qui passe la commande. Si le propriétaire du fichier n'a pas d'autorisations d'exécution, utilisez un S majuscule ici.

Maintenant, pour voir cela sous un angle pratique, regardons la commande /usr/bin/passwd. Cette commande, par défaut, a l'autorisation SUID définie :

[user@server ~]$ ls -l /usr/bin/passwd
-rwsr-xr-x. 1 racine racine 33544 13 décembre 2021 /usr/bin/passwd

Notez le s où x indique généralement les autorisations d'exécution pour l'utilisateur.


## Sources :

- <a href="https://www.redhat.com/sysadmin/suid-sgid-sticky-bit"> redhat.com : suid </a>
- <a href="https://linux.goffinet.org/administration/securite-locale/permissions-linux/"> linux.goffinet.org : suid</a>
- <a href="https://www.linuxpedia.fr/doku.php/droits_et_permissions_sous_linux"> linuxpedia.fr : suid </a>