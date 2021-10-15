# Activité TryHackMe

<br>

> MITRE

> https://tryhackme.com/room/mitre

<br>

## Qu'est ce que le MITRE ?

<br>

MITRE peut être associer à la liste des CVE (vulnérabilités et expositions communes), qui est une ressource que nous vérifions lors de la recherche d'un exploit pour une vulnérabilité donnée. Mais MITRE effectue des recherches dans de nombreux domaines, en dehors de la cybersécurité, pour « la sécurité, la stabilité et le bien-être de notre nation ». Ces domaines comprennent l'intelligence artificielle, l'informatique de santé, la sécurité spatiale, pour n'en nommer que quelques-uns.

<br>

De Mitre.org : 

<br>

"Chez MITRE, nous résolvons les problèmes pour un monde plus sûr. Grâce à nos centres de R&D financés par le gouvernement fédéral et à nos partenariats public-privé, nous travaillons à travers le gouvernement pour relever les défis de la sécurité, de la stabilité et du bien-être de notre nation. "

<br>

## ATT&CK Framework


<br>

MITRE ATT&CK® est une base de connaissances accessible à l'échelle mondiale sur les tactiques et techniques de l'adversaire, basée sur des observations du monde réel.

<br>

Le cadre ATT&CK® s'est développé et étendu au fil des ans. Une expansion notable était que le cadre se concentrait uniquement sur la plate-forme Windows mais s'est étendu pour couvrir d'autres plates-formes, telles que macOS et Linux. Le cadre est largement contribué par de nombreuses sources, telles que les chercheurs en sécurité et les rapports de renseignements sur les menaces. Notez que ce n'est pas seulement un outil pour les équipes bleues. L'outil est également utile pour un testeur d'intrusion et/ou un red teamer.

<img src="https://github.com/Darylabrador/cybersecurite/blob/Excels/MITRE/images/ATT_CK.PNG">

<br>

- <a href="https://attack.mitre.org/"> https://attack.mitre.org/ </a>
- <a href="https://mitre-attack.github.io/attack-navigator//#layerURL=https%3A%2F%2Fattack.mitre.org%2Fgroups%2FG0008%2FG0008-enterprise-layer.json"> https://mitre-attack.github.io/attack-navigator/ </a>

<br>

## CAR Knowledge Base ?

<br>

Le MITRE Cyber ​​Analytics Repository (CAR) est une base de connaissances d'analyse développée par MITRE sur la base du modèle d'adversaire MITRE ATT&CK®. CAR définit un modèle de données qui est exploité dans ses représentations de pseudocode, mais inclut également des implémentations directement ciblées sur des outils spécifiques (par exemple, Splunk, EQL) dans ses analyses. En ce qui concerne la couverture, CAR se concentre sur la fourniture d'un ensemble d'analyses validées et bien expliquées, en particulier en ce qui concerne leur théorie et leur justification de fonctionnement.

<img src="https://github.com/Darylabrador/cybersecurite/blob/Excels/MITRE/images/CAR.PNG">

<br>

- <a href="https://car.mitre.org/analytics/CAR-2020-09-001/"> Exemple : CAR-2020-09-001 </a>
- <a href="https://car.mitre.org/analytics/CAR-2014-11-004/"> Exemple : CAR-2014-11-004 </a>
- <a href="https://car.mitre.org/analytics/"> https://car.mitre.org/analytics/ </a>
- <a href="https://eql.readthedocs.io/en/latest/"> https://eql.readthedocs.io/en/latest/</a>
- <a href="https://mitre-attack.github.io/attack-navigator/beta/enterprise/#layerURL=https%3A%2F%2Fraw.githubusercontent.com%2Fmitre-attack%2Fcar%2Fmaster%2Fdocs%2Fcar_attack%2Fcar_attack.json"> https://mitre-attack.github.io/attack-navigator/beta/enterprise </a>

<br>

Pour résumer, CAR est un endroit idéal pour trouver des analyses qui nous emmènent plus loin que les résumés d'atténuation et de détection dans le cadre ATT&CK®. Cet outil n'est pas un remplacement pour ATT&CK® mais une ressource supplémentaire.

<br>

## Sheild Active Defense

<br>

Shield est une base de connaissances de défense active que MITRE développe pour capturer et organiser ce que nous apprenons sur la défense active et l'engagement de l'adversaire. Dérivé de plus de 10 ans d'expérience dans l'engagement de l'adversaire, il couvre la gamme des considérations d'opportunités et d'objectifs de haut niveau, prêtes pour le CISO, aux discussions conviviales pour les praticiens sur les TTP disponibles pour les défenseurs.

<br>

Shield Active Defense est similaire à la matrice ATT&CK®, mais les tactiques et techniques qui nous sont fournies nous permettent de piéger et/ou d'engager (avec) un adversaire actif au sein du réseau. Par exemple, nous pouvons planter des informations d'identification leurres sur une ressource et surveiller si/quand les informations d'identification du compte sont utilisées ailleurs dans le réseau. En faisant cela, nous sommes alertés de la présence de l'adversaire et offre l'opportunité de se renseigner sur ses outils et tactiques. Les informations recueillies peuvent être classées comme des renseignements sur les menaces.

<img src="https://github.com/Darylabrador/cybersecurite/blob/Excels/MITRE/images/shield_active_defense.PNG">

<br>

- <a href="https://shield.mitre.org/"> https://shield.mitre.org/ </a>
- <a href="https://shield.mitre.org/techniques/DTE0012/"> Exemple : DTE0012 </a>

<br>

## ATT&CK® Emulation Plans

<br>

Les plans d'émulation sont un guide étape par étape sur la façon d'imiter le groupe de menaces spécifique. Si l'un des membres de la C-Suite demandait : « comment nous en sortirions-nous si APT29 nous frappait ? » On peut facilement y répondre en se référant aux résultats de l'exécution du plan d'émulation.

<img src="https://github.com/Darylabrador/cybersecurite/blob/Excels/MITRE/images/emulations_plan.PNG">

<br>

- <a href="https://mitre-engenuity.org/"> https://mitre-engenuity.org/ </a>
- <a href="https://medium.com/mitre-engenuity/introducing-the-all-new-adversary-emulation-plan-library-234b1d543f6b"> https://medium.com/mitre-engenuity/introducing-the-all-new-adversary-emulation-plan-library-234b1d543f6b </a>
- <a href="https://mitre-engenuity.org/attackevaluations/"> https://mitre-engenuity.org/attackevaluations/ </a>
- <a href="https://attack.mitre.org/resources/adversary-emulation-plans/"> https://attack.mitre.org/resources/adversary-emulation-plans/ </a>
- <a href="https://github.com/center-for-threat-informed-defense/adversary_emulation_library/tree/master/apt29"> https://github.com/center-for-threat-informed-defense/adversary_emulation_library/tree/master/apt29 </a>
- <a href="https://github.com/center-for-threat-informed-defense/adversary_emulation_library/tree/master/fin6">  https://github.com/center-for-threat-informed-defense/adversary_emulation_library/tree/master/fin6 </a>

<br>

## ATT&CK® and Threat Intelligence

<br>

Threat Intelligence (TI) ou Cyber ​​Threat Intelligence (CTI) est l'information, ou TTP, attribuée à l'adversaire. En utilisant les renseignements sur les menaces, en tant que défenseurs, nous pouvons prendre de meilleures décisions concernant la stratégie défensive. Les grandes entreprises peuvent avoir une équipe interne dont l'objectif principal est de collecter des informations sur les menaces pour d'autres équipes au sein de l'organisation, en plus d'utiliser des informations sur les menaces déjà disponibles. 

Certaines de ces informations sur les menaces peuvent être open source ou via un abonnement auprès d'un fournisseur, tel que CrowdStrike. En revanche, de nombreux défenseurs portent plusieurs chapeaux (rôles) au sein de certaines organisations, et ils doivent consacrer du temps à leurs autres tâches pour se concentrer sur les renseignements sur les menaces. Pour répondre à ces derniers, nous travaillerons sur un scénario d'utilisation d'ATT&CK® pour la veille sur les menaces. L'objectif du renseignement sur les menaces est de rendre l'information exploitable.

<img src="https://github.com/Darylabrador/cybersecurite/blob/Excels/MITRE/images/threat_intelligence.PNG">

<br>

- <a href="https://www.crowdstrike.com/"> https://www.crowdstrike.com/ </a>

