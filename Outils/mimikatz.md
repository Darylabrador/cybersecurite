# Logiciel : mimikatz.exe

## Pourquoi l'utiliser ? 

On utilise mimikatz pour récupérer les mots de passent qui sont stockés sur la machine windows de la victime.

<br>

## Points positifs

- Il faut le mettre sur la machine de la victime et donc sans cette manipulation un attaquant ne peut rien faire
- Il nécessite d'être lancer en tant qu'administrateur


## Points négatifs

Du côté de la victime, mimikatz présente les points suivants :

<br>

- Pass-the-Hash : Windows avait pour habitude de conserver les données de mot de passe dans un hachage NTLM. Les hackers utilisent Mimikatz pour transmettre la chaîne de hachage exacte à l’ordinateur cible pour se connecter. Ils n’ont même pas besoin de craquer le mot de passe, il leur suffit d’utiliser la chaîne de hachage. C’est comme si l’on trouvait par terre le passe-partout d’un bâtiment. Une clé suffit pour ouvrir toutes les portes.
    
- Pass-the-Ticket : les versions plus récentes de Windows conservent les données de mot de passe dans un élément appelé « ticket ».  Mimikatz donne la possibilité à un utilisateur de transmettre un ticket kerberos à un autre ordinateur et de l’utiliser pour se connecter. Fondamentalement, c’est l’équivalent de pass-the-hash.
   
- Over-Pass the Hash (Pass the Key) : encore une autre variante de « pass-the-hash », mais cette technique transmet une clé unique obtenue auprès d’un contrôleur de domaine pour se faire passer pour un utilisateur.
   
- Kerberos Golden Ticket : il s’agit d’une attaque pass-the-ticket, à la différence près que ce ticket correspond à un compte masqué nommé KRBTGT, qui n’est autre que le compte qui chiffre tous les autres tickets. Un golden ticket vous accorde, pour tout ordinateur du réseau, des droits d’administrateur de domaine qui n’expirent pas.
    
- Kerberos Silver Ticket : une autre attaque pass-the-ticket, sauf qu’un silver ticket exploite une caractéristique de Windows qui vous permet d’utiliser facilement des services sur le réseau. Kerberos accorde un ticket TGS à un utilisateur et celui-ci peut l’utiliser pour se connecter à n’importe quel service du réseau. Microsoft ne contrôle pas toujours le TGS une fois qu’il a été émis, et il peut donc facilement passer entre les mailles de n’importe quelle protection.
    
- Pass-the-Cache : enfin une attaque qui n’exploite pas Windows ! Une attaque pass-the-cache est généralement équivalente à une attaque pass-the-ticket, à la différence près qu’elle utilise les données de connexion enregistrées et chiffrées d’un système Mac/UNIX/Linux.
