# Veille notion de Syslog sous Linux

### Qu’est ce que c’est que le syslog ?

Le syslog est le processus de journalisation qui enregistre les événements afin de permettre de localiser rapidement les défaillances d’un système. Chaque service possède son propre fichier de log qui sont tous stockés dans la partition /var/log.


### A quoi ressemble une ligne d’évènement ?

Dans chaque ligne d'évènement on distingue :

-	La date à laquelle l'évènement a été déclenché
-	Le processus déclencheur de l'évènement
-	Le processus ayant demandé l'ajout du message correspondant au log
-	Le niveau de gravité du message (priority)

Ci-dessous vous pouvez retrouvez les niveaux de gravité :

| Code numérique | Sévérité | Description                                   |
| :---           | :---     | :---                                          |
| 0              | emerg    | Système inutilisable (urgence)                |
| 1              | alert    | Intervention immédiate nécessaire (Alerte)    |
| 2              | crit     | Erreur système critique (Critique)            |
| 3              | err      | Erreur de fonctionnement (Erreur)             |
| 4              | warning  | Avertissement                                 |
| 5              | notice   | Evénement normal mais devant être signalé     |
| 6              | info     | Messages d'information                        |
| 7              | debug    | Message de débogage                           |


### Les types de messages :

Il existe 5 types de messages qui sont les suivantes :

| Info              | Description                                                                                                                           |
| :---              | :---                                                                                                                                  |
| /var/log/secure   | Syslog stocke dans le fichier de log « secure » tous les messages liés à la sécurité y compris ceux de l’authentification.            |
| /var/log/maillog  | Syslog stocke les messages liés aux messageries.                                                                                      |
| /var/log/cron     | Contient tous les messages liés au démarrage du système.                                                                              |
| /var/log/boot.log | Contient tous les messages liés au démarrage du système.                                                                              |
| /var/log/messages | La plupart des messages log sont enregistré dans le fichier /var/log/messages, sauf les types de messages qu’on a vus précédemment.   |





### Ressources :

- https://fr.wikibooks.org/wiki/Le_syst%C3%A8me_d%27exploitation_GNU-Linux/Les_fichiers_journaux_syslog 
- https://www.linuxtricks.fr/wiki/syslog-les-journaux-systeme-sous-linux
- https://sysreseau.net/syslog-la-journalisation-sous-linux/
- https://doc.ubuntu-fr.org/syslog-ng