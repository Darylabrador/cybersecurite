## Les principaux fichiers et leurs emplacements.

Ci dessous on retrouve les principaux fichiers de logs d'un système Linux avec leur emplacement :


<table>
  <thead>
    <tr>
      <th>Nom du fichier</th>
      <th>Emplacement</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>syslog</td>
      <td>/var/log/syslog</td>
    </tr>
    <tr>
      <td>auth.log</td>
      <td>/var/log/auth.log</td>
    </tr>
    <tr>
      <td>kern.log</td>
      <td>/var/log/kern.log</td>
    </tr>
    <tr>
      <td>apache2 - access.log</td>
      <td>/var/log/apache2/access.log</td>
    </tr>
    <tr>
      <td>apache2 - error.log</td>
      <td>/var/log/apache2/error.log</td>
    </tr>
  </tbody>
</table>


## Les moyens de les parcourir efficacement.

En utilisant la commande :

- tail -f -n 5 "chemin_dacces" => live logs
- tail -n 5 "chemin_dacces" => logs
- grep -r "adresse ip" /var/log => affiche toutes nos traces dans les logs qu'importe le fichier
- grep -rl "adresse ip" /var/log => récupérer tous les noms de fichiers qui ont gardé nos traces
- grep -r -m 20 "adresse ip" /var/log => affichage d'un nombre limité de la sortie


### Chercher au moins 1 trace de vos attaques grâce aux logs concernant l'activité 'blog'

On retrouve aussi des traces de nos commandes en saisissant la commande 

- history

> L'utilisation du brutforce 

root@blog:/var/log# grep -i hydra apache2/access.log
grep -i hydra apache2/access.log
192.168.196.128 - - [26/May/2020:04:14:06 +0000] "GET /wp-login.php HTTP/1.0" 200 3602 "-" "Mozilla/5.0 (Hydra)"
192.168.196.128 - - [26/May/2020:04:14:06 +0000] "POST /wp-login.php HTTP/1.0" 302 1051 "-" "Mozilla/5.0 (Hydra)"
192.168.196.128 - - [26/May/2020:04:14:07 +0000] "GET /wp-admin/ HTTP/1.0" 200 46484 "-" "Mozilla/5.0 (Hydra)"
192.168.196.128 - - [26/May/2020:04:15:24 +0000] "GET /wp-login.php HTTP/1.0" 200 3602 "-" "Mozilla/5.0 (Hydra)"
192.168.196.128 - - [26/May/2020:04:15:24 +0000] "POST /wp-login.php HTTP/1.0" 302 1051 "-" "Mozilla/5.0 (Hydra)"
192.168.196.128 - - [26/May/2020:04:15:32 +0000] "GET /wp-login.php HTTP/1.0" 200 3602 "-" "Mozilla/5.0 (Hydra)"
192.168.196.128 - - [26/May/2020:04:15:32 +0000] "POST /wp-login.php HTTP/1.0" 200 4594 "-" "Mozilla/5.0 (Hydra)"
10.9.1.54 - - [19/Aug/2021:05:04:57 +0000] "GET /wp-login.php HTTP/1.0" 200 3460 "-" "Mozilla/5.0 (Hydra)"
10.9.1.54 - - [19/Aug/2021:05:04:57 +0000] "GET /wp-login.php HTTP/1.0" 200 3460 "-" "Mozilla/5.0 (Hydra)"
10.9.1.54 - - [19/Aug/2021:05:04:57 +0000] "GET /wp-login.php HTTP/1.0" 200 3460 "-" "Mozilla/5.0 (Hydra)"
10.9.1.54 - - [19/Aug/2021:05:04:57 +0000] "GET /wp-login.php HTTP/1.0" 200 3460 "-" "Mozilla/5.0 (Hydra)"
10.9.1.54 - - [19/Aug/2021:05:04:57 +0000] "GET /wp-login.php HTTP/1.0" 200 3460 "-" "Mozilla/5.0 (Hydra)"
10.9.1.54 - - [19/Aug/2021:05:04:57 +0000] "GET /wp-login.php HTTP/1.0" 200 3460 "-" "Mozilla/5.0 (Hydra)"
10.9.1.54 - - [19/Aug/2021:05:04:57 +0000] "GET /wp-login.php HTTP/1.0" 200 3460 "-" "Mozilla/5.0 (Hydra)"
10.9.1.54 - - [19/Aug/2021:05:04:57 +0000] "GET /wp-login.php HTTP/1.0" 200 3460 "-" "Mozilla/5.0 (Hydra)"
10.9.1.54 - - [19/Aug/2021:05:04:57 +0000] "GET /wp-login.php HTTP/1.0" 200 3460 "-" "Mozilla/5.0 (Hydra)"
10.9.1.54 - - [19/Aug/2021:05:04:57 +0000] "GET /wp-login.php HTTP/1.0" 200 3460 "-" "Mozilla/5.0 (Hydra)"
10.9.1.54 - - [19/Aug/2021:05:04:57 +0000] "GET /wp-login.php HTTP/1.0" 200 3460 "-" "Mozilla/5.0 (Hydra)"
10.9.1.54 - - [19/Aug/2021:05:04:57 +0000] "GET /wp-login.php HTTP/1.0" 200 3460 "-" "Mozilla/5.0 (Hydra)"


> Utilisation de metasploit lorsqu'il envoie l'image sur le serveur

10.9.1.54 - - [19/Aug/2021:05:31:24 +0000] "POST /wp-admin/post.php HTTP/1.1" 302 397 "-" "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)"
127.0.0.1 - - [19/Aug/2021:05:31:31 +0000] "GET /wp-content/uploads/2021/08/xJIkQiBXNL-e1629351070796.jpg?/../../../../themes/twentytwenty/DrHvnubtQZ HTTP/1.0" 200 3290 "-" "-"
127.0.0.1 - - [19/Aug/2021:05:31:31 +0000] "GET /wp-content/uploads/2021/08/xJIkQiBXNL-e1629351070796.jpg?/../../../../themes/twentytwenty/DrHvnubtQZ HTTP/1.0" 200 3290 "-" "-"

> escalade de privilège

tail -n 20 auth.log
Aug 19 04:57:10 blog sshd[1464]: Did not receive identification string from 10.9.1.54 port 37666
Aug 19 04:57:22 blog sshd[1473]: Protocol major versions differ for 10.9.1.54 port 37688: SSH-2.0-OpenSSH_7.6p1 Ubuntu-4ubuntu0.3 vs. SSH-1.5-Nmap-SSH1-Hostkey
Aug 19 04:57:22 blog sshd[1474]: Protocol major versions differ for 10.9.1.54 port 37698: SSH-2.0-OpenSSH_7.6p1 Ubuntu-4ubuntu0.3 vs. SSH-1.5-NmapNSE_1.0
Aug 19 04:57:23 blog smbd: pam_unix(samba:session): session closed for user nobody
Aug 19 04:57:23 blog sshd[1486]: Unable to negotiate with 10.9.1.54 port 37722: no matching host key type found. Their offer: ssh-dss [preauth]
Aug 19 04:57:24 blog smbd: pam_unix(samba:session): session closed for user nobody
Aug 19 04:57:24 blog smbd: pam_unix(samba:session): session closed for user nobody
Aug 19 04:57:24 blog sshd[1491]: Connection closed by 10.9.1.54 port 37732 [preauth]
Aug 19 04:57:25 blog sshd[1495]: Connection closed by 10.9.1.54 port 37746 [preauth]
Aug 19 04:57:26 blog sshd[1498]: Unable to negotiate with 10.9.1.54 port 37756: no matching host key type found. Their offer: ecdsa-sha2-nistp384 [preauth]
Aug 19 04:57:26 blog smbd: pam_unix(samba:session): session closed for user nobody
Aug 19 04:57:27 blog sshd[1500]: Unable to negotiate with 10.9.1.54 port 37760: no matching host key type found. Their offer: ecdsa-sha2-nistp521 [preauth]
Aug 19 04:57:28 blog sshd[1503]: Connection closed by 10.9.1.54 port 37766 [preauth]
Aug 19 04:57:28 blog smbd: pam_unix(samba:session): session closed for user nobody
Aug 19 05:09:01 blog CRON[3701]: pam_unix(cron:session): session opened for user root by (uid=0)
Aug 19 05:09:01 blog CRON[3701]: pam_unix(cron:session): session closed for user root
Aug 19 05:17:01 blog CRON[3801]: pam_unix(cron:session): session opened for user root by (uid=0)
Aug 19 05:17:01 blog CRON[3801]: pam_unix(cron:session): session closed for user root
Aug 19 05:39:02 blog CRON[3938]: pam_unix(cron:session): session opened for user root by (uid=0)
Aug 19 05:39:02 blog CRON[3938]: pam_unix(cron:session): session closed for user root

> tous les fichiers qui ont gardé nos traces :

root@blog:/var/log# grep -rl 10.9.1.54 /var/log
grep -rl 10.9.1.54 /var/log
/var/log/samba/log.10.9.1.54
/var/log/apache2/error.log
/var/log/apache2/access.log
/var/log/journal/a48aa1b7b471491790e2497ef04d3ae8/system.journal
/var/log/auth.log


### Sources :

- https://wiki.debian-fr.xyz/Consulter_les_logs_:_quoi,_o%C3%B9_et_comment_chercher_%3F