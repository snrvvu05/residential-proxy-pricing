# acheter proxy résidentiel : payer à l'IP ou au Go, éviter les pièges et choisir le bon forfait

Acheter un proxy résidentiel ressemble à une opération simple : on choisit un nombre d'IP ou une quantité de trafic, on paie, on récupère un identifiant. Le problème arrive après. Vous payez 20 $ pour 100 IP et vous découvrez que vos sessions tombent au bout d'une heure. Vous payez au Go et vous réalisez trois mois plus tard que vos gigas restants ont expiré. Dans les deux cas, l'argent est parti sans que le travail soit fait.

La vraie question n'est donc pas « quel fournisseur est le moins cher », mais « quel modèle de facturation correspond à ce que je vais réellement faire ». C'est là que 9Proxy, un fournisseur de proxys résidentiels qui a justement bâti son catalogue autour de deux modèles concurrents (à l'IP et au Go) plus des packs combinés, mérite qu'on regarde ses chiffres de près. Chiffres qu'il faut lire à jour : la grille à l'IP a changé le 1er juin 2026.

## Deux façons de payer, deux logiques opposées

### Le modèle à l'IP : bande passante illimitée

Vous achetez un stock d'adresses IP résidentielles. Chaque IP reste active de quelques heures à environ 24 heures, et pendant ce temps vous pouvez faire passer autant de trafic que vous voulez : pas de compteur de gigas, pas de dépassement facturé.

Conséquence pratique : un scraping lourd en JavaScript, où une page pèse 2 à 5 Mo, ne coûte pas plus cher qu'un scraping léger. Ce qui coûte, c'est le nombre de sessions distinctes que vous voulez maintenir en parallèle.

Chez 9Proxy, les IP non utilisées n'expirent pas : le solde reste dans le compte jusqu'à consommation. Côté mise en place, ce modèle passe par une application de bureau (Windows/macOS) qui fait du transfert de port local, avec une authentification par utilisateur/mot de passe en option.

### Le modèle au Go : vous payez le trafic, pas les adresses

Ici, pas de stock d'IP à gérer : vous générez autant d'endpoints que nécessaire depuis le tableau de bord, et seule la bande passante consommée est déduite de votre solde. Deux modes de session sont disponibles, rotation à chaque requête ou session collante, et le ciblage descend au pays, État, ville, code postal et FAI.

La contrepartie : la validité. Les forfaits au Go sont valables 180 jours, sauf en formule Enterprise où le trafic n'expire plus. Si vous achetez 200 Go pour un projet qui traîne, mieux vaut savoir compter.

Si vous hésitez encore entre les deux logiques, 👉 [comparez les modèles de facturation résidentielle de 9Proxy](https://bit.ly/9-Proxy) avant de choisir un volume.

## Ce que 9Proxy vend concrètement

La plateforme annonce un pool de plus de 20 millions d'IP résidentielles réparties sur 90+ pays, avec prise en charge de HTTP, HTTPS et SOCKS5. Le ciblage géographique va jusqu'à la ville et au FAI, ce qui sert surtout à deux choses : voir une page localisée exactement comme un habitant la voit, et éviter les incohérences entre fuseau horaire du navigateur et adresse réseau.

L'outillage se répartit en quatre blocs :

- **Proxy Program** : client de bureau qui route le trafic au niveau du système, utile pour les logiciels sans prise en charge native des proxys.
- **Proxy2Web** : accès navigateur sans installation, via identifiants classiques.
- **ProxyHub** : gestion d'appareils mobiles, en version Lite sur un appareil ou Pro avec pilotage centralisé.
- **API publique** : contrôle des sessions et lecture des statistiques depuis vos propres scripts.

Deux fonctions reviennent dans la documentation et changent le calcul économique. La **Today List** permet de réutiliser gratuitement des IP déjà consommées dans les 24 heures précédentes, ce que le fournisseur chiffre à 20-30 % d'économie sur les tâches répétitives. L'**auto-refresh** détecte et remplace une IP hors ligne en une soixantaine de secondes, ce qui évite les cascades de « connection refused » au milieu d'un job long.

## Les prix et forfaits actuels

Attention à une chose avant de lire les tableaux : 9Proxy a annoncé le 18 mai 2026 sa première hausse de prix, appliquée au 1er juin 2026. Elle concerne uniquement les forfaits à l'IP et les packs combinés. Les forfaits au Go n'ont pas bougé. Beaucoup de comparatifs en ligne affichent encore les tarifs d'avant, notamment 0,20 $ par IP sur le palier d'entrée.

### Forfaits à l'IP (bande passante illimitée)

Le prix par IP ci-dessous est le prix effectif, calculé sur le total réellement facturé.

| Forfait | Prix effectif par IP | Total | Validité des IP |
| --- | --- | --- | --- |
| 100 IP | 0,24 $ | 24 $ | aucune expiration |
| 500 IP | 0,144 $ | 72 $ | aucune expiration |
| 1 000 IP + 500 offertes | 0,084 $ | 126 $ | aucune expiration |
| 2 500 IP | 0,084 $ | 210 $ | aucune expiration |
| 5 000 IP | 0,072 $ | 360 $ | aucune expiration |
| 15 000 IP | 0,048 $ | 720 $ | aucune expiration |
| 25 000 IP | 0,035 $ | 863 $ | aucune expiration |
| 50 000 IP | 0,029 $ | 1 438 $ | aucune expiration |
| 100 000 IP (Business) | 0,023 $ | 2 300 $ | aucune expiration |
| 200 000 IP (Business) | 0,021 $ | 4 140 $ | aucune expiration |
| 500 000 IP (Business) | 0,018 $ | 8 625 $ | aucune expiration |

👉 [Acheter un forfait résidentiel à l'IP avec le lien d'inscription 9Proxy](https://bit.ly/9-Proxy)

### Forfaits au Go

| Forfait | Prix par Go | Total | Validité |
| --- | --- | --- | --- |
| 5 Go | 3,00 $ | 15 $ | 180 jours |
| 50 Go + 5 Go offerts | 2,10 $ | 105 $ | 180 jours |
| 100 Go | 1,50 $ | 150 $ | 180 jours |
| 200 Go | 1,00 $ | 200 $ | 180 jours |
| 1 000 Go | 0,80 $ | 800 $ | 180 jours |
| 2 000 Go | 0,75 $ | 1 500 $ | 180 jours |
| 3 000 Go (Enterprise) | 0,72 $ | 2 160 $ | illimitée |
| 10 000 Go et plus | 0,68 $ | sur devis | illimitée |

### Packs combinés IP + Go

| Pack | Contenu | Prix | Remise affichée au paiement |
| --- | --- | --- | --- |
| Starter | 100 IP + 5 Go | 30 $ | remise par rapport au prix catalogue |
| Popular | 1 500 IP + 50 Go | 180 $ | remise par rapport au prix catalogue |
| Pro | 5 000 IP + 500 Go | 720 $ | 860 $ barrés, soit 16,28 % de remise |

Le trafic inclus dans un pack suit la validité de 180 jours, tandis que les IP suivent leur propre règle. La formule Enterprise, elle, ouvre un mode équipe (1 propriétaire + 5 membres), avec partage de bande passante sans expiration entre membres, contrôle du trafic par membre et journaux d'activité.

👉 [Voir les packs combinés IP + Go et les remises en cours](https://bit.ly/9-Proxy)

## Quel forfait choisir selon votre usage réel

Les scénarios ci-dessous ne demandent pas la même structure de coûts. C'est le point que la plupart des comparatifs ratent : ils classent les fournisseurs au prix d'entrée, alors que le prix d'entrée n'est presque jamais le bon achat.

**Collecte de données à volume élevé, pages lourdes.** Le modèle à l'IP gagne. Une page de 3 Mo multipliée par 100 000 requêtes, ce sont 300 Go que vous ne paierez jamais, quelle que soit la taille réelle de votre pipeline.

**Vérification d'annonces, contrôle de géolocalisation, test de prix, surveillance SERP.** Chaque requête consomme très peu de données mais demande une IP différente. Le modèle au Go est plus rationnel : 5 Go à 15 $ couvrent énormément de vérifications ponctuelles.

**Gestion de plusieurs comptes sur un même réseau.** Une IP propre par profil, tenue sur la durée de la session. Le forfait à l'IP est adapté, à condition d'accepter la durée de vie naturelle de chaque adresse et de prévoir le remplacement.

**Projets ponctuels ou travail par lots.** Le risque principal est l'expiration. Un forfait au Go garde 180 jours de marge ; un forfait à l'IP ne perd rien puisque les IP inutilisées restent au compte. Un pack combiné évite de jongler entre deux achats quand un projet change de nature en cours de route.

**Équipe ou agence avec plusieurs clients.** Le mode Enterprise avec membres et quotas individuels évite de partager un compte principal, avec les dérapages que ça implique.

## Acheter et payer : le déroulé concret

Le parcours d'achat est standard, mais deux détails méritent d'être connus avant de valider.

1. Choisissez le type de forfait et le palier, puis cliquez sur la commande.
2. À l'étape de paiement, sélectionnez le moyen de paiement : carte bancaire, Google Pay, Alipay, cryptomonnaie, paiement local selon votre pays, ou le portefeuille interne 9Proxy.
3. Saisissez un code promo dans le champ prévu si vous en avez un. Les achats de pack affichent parfois une remise automatique : l'exemple officiel du pack 5 000 IP + 500 Go montre 860 $ ramenés à 720 $.
4. Validez et le forfait s'active immédiatement après confirmation.

Sur le plan des économies ponctuelles : 9Proxy fait tourner des campagnes où un coupon personnel (format X9_…) apparaît dans « My Coupons » après une première commande au Go, appliqué automatiquement au paiement suivant, sans cumul possible avec d'autres codes. Le calendrier change ; ce n'est pas une remise permanente.

Le lien d'inscription affiché dans cet article contient un code d'invitation. Le programme d'affiliation de 9Proxy prévoit, d'après les conditions publiées par la société, une remise pour l'utilisateur parrainé au moment de la commande. Le montant exact apparaît dans le récapitulatif avant paiement, il n'y a rien à deviner.

À noter aussi : pour les forfaits à l'IP, l'achat se fait en solde prépayé. Les IP non consommées ne disparaissent pas à la fin du mois, contrairement aux abonnements mensuels classiques.

## Les limites à connaître avant de payer

Un proxy résidentiel n'est pas un serveur. Chaque adresse appartient à un particulier ; quand ce particulier éteint sa box, l'IP disparaît. Ce n'est pas un défaut de 9Proxy en particulier, c'est la nature du produit, et la documentation de la plateforme le dit noir sur blanc : une IP tient de quelques heures à environ 24 heures, rarement plus.

Un avis publié sur la page Trustpilot française le 17 janvier 2026 décrit exactement ce désagrément : des IP qui cessent de fonctionner au bout d'une heure environ, provoquant selon l'auteur des blocages de sécurité sur ses comptes. La réponse de l'équipe support est instructive, et plutôt honnête : elle rappelle que cette instabilité est inhérente aux proxys résidentiels dynamiques, qu'aucune durée de vie fixe ne peut être garantie, et oriente ce type de besoin vers des proxys statiques (ISP) quand une session longue est critique.

> Avant d'acheter, sachez ce que vous achetez : une IP résidentielle tourne autour d'elle-même pendant quelques heures. Si votre workflow exige la même adresse pendant des jours, ce n'est pas un problème de fournisseur, c'est un mauvais type de proxy.

Trois autres points à intégrer dans votre budget :

- **Les forfaits au Go expirent à 180 jours.** Le trafic non consommé est perdu, sauf formule Enterprise.
- **Le modèle à l'IP suppose une application de bureau.** Sur serveur ou conteneur, passez plutôt par les connexions directes HTTP/SOCKS5 du tableau de bord.
- **La réputation est clivée et dépend de la source.** Les notes publiques de 9Proxy divergent fortement selon la page consultée, de 2/5 sur une page Trustpilot à 4,6/5 sur une autre, ce qui signale surtout un échantillon réduit. Un annuaire tiers (ProxyLook) le classe à 3,9/5 avec un taux de réussite annoncé autour de 97 % et une latence moyenne d'environ 1 300 ms, chiffres à prendre comme des ordres de grandeur déclarés, pas comme un protocole de test.

## Questions fréquentes

**Y a-t-il un essai gratuit ?** Il n'existe pas de palier gratuit permanent affiché. 9Proxy indique proposer un essai limité aux nouveaux utilisateurs, sur demande et selon les disponibilités, en précisant si vous voulez tester des IP ou des gigas. Les quantités évoquées dans les échanges publics varient, ne comptez pas dessus comme d'un droit acquis.

**Combien d'IP pour commencer ?** Le palier 100 IP à 24 $ sert à valider un pipeline : taux de réussite sur vos cibles, vitesse, taux de blocage. C'est aussi le moyen le plus honnête de vérifier si vos cibles tolèrent des IP résidentielles.

**Le ciblage ville et FAI est-il disponible partout ?** La profondeur de ciblage dépend de la zone. Le ciblage pays est large ; les niveaux État, ville, code postal et FAI dépendent de la couverture réelle du pool sur le pays visé. À vérifier sur votre marché avant de commander un gros volume.

**Peut-on revendre les IP achetées ?** La revente est interdite par les conditions d'utilisation. Le partage en équipe passe par les listes blanches d'IP ou les sous-comptes.

**Que se passe-t-il si une IP ne fonctionne pas ?** La plateforme met en avant une politique de remplacement des proxys défaillants, et signale automatiquement les IP inutilisables pour éviter qu'elles soient réattribuées. C'est ce mécanisme, plus que le prix affiché, qui détermine votre coût réel par IP utile.

## Le récapitulatif en une ligne

Si vous achetez des proxys résidentiels pour du volume avec des pages lourdes, prenez de l'IP, sans compteur de gigas. Si vous alternez les adresses pour du contrôle de contenu ou des vérifications, prenez du Go. Et si vous ne savez pas encore où votre projet va atterrir, un pack combiné évite de repayer une deuxième fois dans trois semaines.

Le reste se joue sur des détails qui ne se voient pas dans un tableau : la durée de vie des IP, la remise affichée au checkout, la validité de 180 jours. 👉 [Commencez par le palier d'entrée chez 9Proxy](https://bit.ly/9-Proxy), mesurez ce que vos cibles acceptent réellement, puis dimensionnez le forfait suivant sur vos chiffres à vous plutôt que sur ceux d'une page comparative.
