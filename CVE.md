## Définition

Common Vulnerabilities and Exposures (CVE) est une liste publique de failles de sécurité informatique. Les avis de sécurité publiés par les fournisseurs et chercheurs mentionnent presque toujours au moins un identifiant CVE.

Les CVE aident les professionnels à coordonner leurs efforts visant à hiérarchiser et résoudre les vulnérabilités, et ainsi renforcer la sécurité des systèmes informatiques.

## Format

La liste CVE est supervisée par l'organisme MITRE et subventionnée par la CISA (Cybersecurity and Infrastructure Security Agency), qui fait partie du Département de la Sécurité intérieure des États-Unis.

Les identifiants CVE sont attribués par des autorités déléguées, les CNA (CVE Numbering Authority). Elles sont sous la forme CVE-AAAA-NNNN :

- AAAA : est l'année de publication
- NNNN : est un numéro identifiant

## Exemple : CVE-2021-36934 (20 juillet 2021)

Le CVE-2021-36934 est un bulletin de sécurité affectant plusieurs version du sytèmes d'exploitation Window. Cette vulnérabilité est liée à une mauvaise configuration des droits d'accès pour les fichiers présents dans le dossier %windir%\system32\config\.

L'attaquant peut aux fichiers des ruches du Registre, en particulier celui de la base SAM contenant les utilisateurs et les empreintes des mots de passe des comptes locaux ainsi qu’aux fichiers des ruches « SYSTEM » et « SECURITY » (qui contient le mot de passe de la machine si cette dernière est membre d’un domaine Active Directory).

Malgré que les droits d’accès soient erronés, ces fichiers sont verrouillés et donc inaccessibles à l’utilisateur. Cependant, les clichés instantanés de ces fichiers, réalisés par le mécanisme Volume Shadow Copy (VSS), conservent les droits d’accès configurés, il est donc possible d’accéder en lecture au contenu de ces fichiers via les copies de sauvegarde. Un utilisateur non privilégié est alors en mesure de récupérer les secrets d’authentification, en particulier ceux des comptes locaux comme le compte d’administrateur local ainsi que le compte de l’ordinateur, lui permettant donc d’élever ses privilèges.

> Résumé :

Un attaquant peut récupérer le secret d'authentification en exploitatant la mauvaise configuration des droits d'accès pour les fichiers %windir%\system32\config\. Grâce à cette mauvaise configuration, il peut avoir accès à la base SAM contenant les utilisateurs et les mots de passe. Ensuite, il pourra récupérer des informations concernant le compte administrateur local et élever ses privilèges.

## Sources 

- <a href="https://fr.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures"> Définition générale </a>
- <a href="https://www.redhat.com/fr/topics/security/what-is-cve"> Précision </a>
- <a href="https://cve.mitre.org/cve/"> Liste des CVE </a>
- <a href="https://www.cert.ssi.gouv.fr/actualite/CERTFR-2021-ACT-031/"> Exemple : CVE-2021-36934 </a>