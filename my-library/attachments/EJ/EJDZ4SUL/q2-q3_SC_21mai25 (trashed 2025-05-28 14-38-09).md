### Tableau 1 : Synthèse des "Dark Patterns" et Logiques Prédatrices

| Type de Dark Pattern / Logique Prédatrice                 | Description du mécanisme                                             | Exemple dans un algorithme de personnalisation                                                                    | Impact psychologique / éthique sur l'utilisateur                      | Principe violé (Déclaration de Montréal)                      |
| --------------------------------------------------------- | -------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------- | ------------------------------------------------------------- |
| Roach Motel                                               | Facile d'entrer, difficile de sortir                                 | Offres d'essai avec désabonnement caché et complexe selon le profil d'engagement                                  | Frustration, sentiment d'emprisonnement, perte financière             | Respect de l'autonomie, Bien-être                             |
| Confirmshaming                                            | Culpabiliser pour obtenir un consentement involontaire               | Message comme « Non merci, je ne veux pas de recommandations pertinentes » basé sur les intérêts de l'utilisateur | Culpabilité, manipulation émotionnelle                                | Respect de l'autonomie, Bien-être                             |
| Hidden Costs                                              | Ajouter des frais tard dans le processus                             | Coûts révélés à la fin du parcours personnalisé basé sur probabilité d'abandon                                    | Frustration, tromperie, perte financière                              | Bien-être, Équité                                             |
| Forced Action                                             | Obliger une action non souhaitée pour accéder à un service           | Fonctionnalités conditionnées à la création de compte ou partage de données selon le profil utilisateur           | Perte de contrôle, violation de la vie privée, frustration            | Respect de l'autonomie, Protection de l'intimité              |
| Privacy Zuckering                                         | Tromper l'utilisateur pour qu’il partage trop                        | Consentement biaisé ou options présélectionnées selon la littératie numérique de l'utilisateur                    | Perte de contrôle, violation de la vie privée, abus de données        | Protection de l'intimité, Respect de l'autonomie              |
| Personalized Filter Bubbles / Echo Chambers               | Renforcer les croyances existantes, réduire la diversité             | Recommandation de contenus qui confortent uniquement les opinions existantes (actualités, réseaux sociaux)        | Polarisation, réduction de la pensée critique, désinformation         | Inclusion, Participation démocratique, Respect de l'autonomie |
| Exploitation de la Vulnérabilité (addiction, impulsivité) | Cibler les utilisateurs fragiles avec des incitations personnalisées | Détection des comportements compulsifs (jeux, achats) et envoi de promotions ciblées                              | Préjudice financier, détresse psychologique, aggravation des troubles | Bien-être, Équité, Prudence                                   |

---

### Tableau 2 : Principes de la Déclaration de Montréal et Stratégies de Correction

| Principe de la Déclaration de Montréal | Manifestation de la logique prédatrice violant ce principe | Étape / Stratégie de modification proposée                                                                     |
| -------------------------------------- | ---------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| Bien-être                              | Exploitation de vulnérabilités, génération de stress       | Audit XAI ; redéfinir objectifs pour inclure bien-être ; limiter la fréquence des sollicitations               |
| Respect de l'autonomie                 | Création de dépendance, prescription de comportements      | Ajouter contrôles utilisateur ; options claires de désengagement ; contre-explications pour éclairer les choix |
| Protection de l’intimité et vie privée | Profilage invasif sans consentement                        | Audit des données ; minimisation ; consentement renforcé ; techniques de ML préservant la vie privée           |
| Équité                                 | Discriminations ou ciblage injuste                         | Audit de biais avec XAI ; techniques FAML ; diversification des jeux de données                                |
| Inclusion de la diversité              | Bulles de filtres, chambres d’écho                         | Objectifs de diversité dans les algos ; exploration de contenus hors-profil                                    |
| Prudence                               | Déploiement sans évaluation suffisante                     | Évaluations d'impact (AIA) avant/après ; tests en conditions variées ; monitoring post-déploiement             |
| Participation démocratique             | Opacité algorithmique, absence de justification            | XAI explicatif ; consultation des usagers ; rapports de transparence                                           |
| Responsabilité                         | Absence de recours, attribution floue des responsabilités  | Chaîne de responsabilité claire ; mécanismes de signalement ; supervision humaine pour les décisions critiques |
### | Principe Proposé pour le Nouveau Code                | Inspiration Principale                                                             | Justification/Adaptation pour la Personnalisation                                                                                          | Implication Pratique pour le Codeur                                                                 |

| Principe Proposé pour le Nouveau Code                       | Inspiration Principale                                                                     | Justification/Adaptation pour la Personnalisation                                                                                 | Implication Pratique pour le Codeur                                                                        |
| ----------------------------------------------------------- | ------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 1. Primauté du Bien-être et de l'Autonomie de l'Utilisateur | Déclaration de Montréal (Bien-être, Autonomie) ; ACM (1.1, 1.2)                            | La personnalisation doit servir l'utilisateur, pas le manipuler ou nuire à son bien-être psychologique ou à sa capacité de choix. | Éviter les "dark patterns", concevoir pour le contrôle utilisateur, évaluer l'impact sur la santé mentale. |
| 2. Responsabilité des Impacts Algorithmiques                | Biosphere Code (P1) ; Déclaration de Montréal (Responsabilité) ; IEEE-CS/ACM (P1)          | Les codeurs sont co-responsables des effets de leurs algorithmes, même non intentionnels.                                         | Participer aux AIA, monitorer les effets post-déploiement, documenter les risques.                         |
| 3. Justice, Équité et Non-Discrimination Algorithmique      | Biosphere Code (P3) ; Déclaration de Montréal (Équité, Inclusion) ; ACM (1.4)              | La personnalisation ne doit pas discriminer ni exacerber les inégalités existantes.                                               | Utiliser FAML, auditer les biais, tester sur des groupes diversifiés, concevoir pour l'accessibilité.      |
| 4. Transparence et Explicabilité des Processus              | Biosphere Code (P6) ; Déclaration de Montréal (Participation démocratique) ; UNESCO (T\&E) | Les utilisateurs doivent pouvoir comprendre les bases de la personnalisation à laquelle ils sont soumis.                          | Documenter la logique algorithmique, fournir des explications (XAI), être clair sur l'usage des données.   |
| 5. Protection Renforcée de la Vie Privée et des Données     | Déclaration de Montréal (Intimité) ; ACM (1.6) ; GDPR                                      | La personnalisation est gourmande en données ; une protection maximale est requise. "Privacy by Design/Default".                  | Minimisation des données, consentement éclairé, anonymisation/pseudonymisation, sécurité des données.      |
| 6. Intégrité Professionnelle, Compétence et Prudence        | ACM (1.3, 2.1, 2.2, 2.6) ; IEEE-CS/ACM (P4, P8) ; Déclaration de Montréal (Prudence)       | Maintenir un haut niveau de savoir-faire technique et éthique, anticiper les risques.                                             | Formation continue (technique et éthique), honnêteté sur les limites, conception robuste et sécurisée.     |
| 7. Conception Adaptative et Ouverte à la Correction         | Biosphere Code (P4)                                                                        | Les algorithmes et leurs impacts évoluent ; la conception doit permettre des ajustements éthiques.                                | Modularité, maintenabilité, mécanismes de feedback, documentation des changements.                         |
| 8. Collaboration Multidisciplinaire et Dialogue             | Déclaration de Montréal (Participation démocratique) ; UNESCO (Gouvernance multipartite)   | Les défis éthiques de la personnalisation sont complexes et nécessitent des perspectives variées.                                 | Travailler avec des éthiciens, designers UX, juristes, utilisateurs ; culture de débat éthique.            |




Encadrer l'Ère de la Personnalisation Algorithmique : De la Modification Éthique à la Déontologie des Codeurs
Résumé (Abstract)
L'omniprésence des algorithmes de personnalisation dans l'écosystème numérique contemporain soulève des questions éthiques cruciales, notamment lorsque leurs mécanismes de fonctionnement engendrent des logiques prédatrices. Ces logiques, souvent dissimulées derrière des interfaces utilisateur conçues pour manipuler ("dark patterns"), exploitent les vulnérabilités des utilisateurs, menaçant leur autonomie, leur bien-être et leur vie privée. Ce rapport aborde cette problématique en poursuivant un double objectif. Premièrement, il propose une série d'étapes concrètes, ancrées dans les principes de la Déclaration de Montréal pour un développement responsable de l'intelligence artificielle , visant à modifier les modalités de fonctionnement de ces algorithmes prédateurs. Deuxièmement, en s'inspirant de l'esprit et des principes du Biosphere Code , il esquisse les fondations d'un code de déontologie spécifiquement destiné aux codeurs d'algorithmes de personnalisation. Les conclusions de cette étude soulignent que la mitigation des dérives prédatrices de la personnalisation ne peut se limiter à des ajustements techniques ; elle requiert une refonte systémique intégrant des considérations éthiques à chaque étape du cycle de vie algorithmique et une responsabilisation accrue des concepteurs. La tension inhérente entre les bénéfices potentiels de la personnalisation et ses capacités d'exploitation nécessite une vigilance constante et l'établissement de garde-fous éthiques et déontologiques robustes pour orienter l'innovation vers le service du bien-être humain.   

Mots-clés : algorithmes de personnalisation, logiques prédatrices, éthique de l'IA, Déclaration de Montréal, Biosphere Code, déontologie des codeurs, dark patterns, responsabilité algorithmique.

1. Introduction
Les algorithmes de personnalisation sont devenus une composante quasi invisible mais déterminante de notre expérience numérique quotidienne. Des flux d'actualités aux recommandations de produits, en passant par les suggestions de contenu sur les plateformes de streaming, ces systèmes façonnent une part croissante des informations que nous consommons et des décisions que nous prenons. Leur promesse est celle d'une expérience utilisateur optimisée, plus pertinente et plus engageante. Cependant, cette médaille a un revers préoccupant : la montée en puissance de ce que l'on peut qualifier de "logiques prédatrices". Ces logiques se manifestent par des systèmes conçus, intentionnellement ou non, pour exploiter les vulnérabilités cognitives, émotionnelles ou informationnelles des utilisateurs à des fins souvent commerciales. Elles sont fréquemment mises en œuvre par le biais de "dark patterns" , des interfaces utilisateur trompeuses ou manipulatrices qui incitent les individus à des actions contraires à leurs intérêts réels.   

L'opacité et la complexité inhérentes à de nombreux algorithmes de personnalisation constituent un terreau fertile pour l'émergence de ces dérives. Lorsque l'optimisation algorithmique est principalement, voire exclusivement, axée sur des métriques telles que le temps d'engagement, le taux de clics ou la conversion, sans contrepoids éthique suffisant, le risque est grand de voir la personnalisation glisser insidieusement vers la manipulation. En effet, la frontière entre une personnalisation utile, qui anticipe un besoin légitime, et une influence subtile qui exploite un biais cognitif pour orienter un choix, est ténue. Poussée à l'extrême et dépourvue de garde-fous éthiques, la personnalisation peut devenir intrinsèquement prédatrice, limitant l'autonomie de l'utilisateur et exploitant ses faiblesses, même en l'absence d'une intention malveillante explicite au départ. Ce glissement peut être une conséquence systémique d'une logique d'optimisation non questionnée.

Face à ces enjeux, des cadres éthiques émergent pour guider un développement technologique plus responsable. La Déclaration de Montréal pour un développement responsable de l'intelligence artificielle  se distingue par son approche fondée sur dix principes clés, allant du bien-être à la responsabilité, en passant par le respect de l'autonomie et la protection de la vie privée. Elle offre un socle pertinent pour repenser les algorithmes de personnalisation. Parallèlement, des initiatives comme le Biosphere Code , bien que centrées initialement sur les impacts environnementaux des algorithmes, proposent une vision holistique de la responsabilité qui peut inspirer une déontologie pour les acteurs de la conception algorithmique.   

Ce rapport se propose d'explorer deux questions fondamentales. D'une part (Question 2), il s'agira de déterminer quelles étapes, fondées sur les principes de la Déclaration de Montréal, pourraient être mises en œuvre pour modifier les modalités de fonctionnement des algorithmes de personnalisation qui génèrent des logiques prédatrices. D'autre part (Question 3), en s'inspirant du cas réel du Biosphere Code, il s'agira de formuler les bases d'un code de déontologie pour les codeurs qui travaillent spécifiquement sur la formulation d'algorithmes de personnalisation.

Pour ce faire, le rapport s'articulera comme suit : une analyse de la problématique des logiques prédatrices et de leurs impacts ; un état de l'art des cadres éthiques, des mécanismes de manipulation et des approches de mitigation existantes ; une présentation de la méthodologie adoptée pour répondre aux questions de recherche ; une discussion des résultats, incluant des propositions concrètes pour la modification des algorithmes et l'esquisse d'un code de déontologie ; une exploration des travaux futurs et des perspectives ; et enfin, une conclusion synthétisant les apports de cette recherche.

2. Problématique et Découverte
2.1. Définition et Caractérisation des Logiques Prédatrices Algorithmiques

Le concept de "logiques prédatrices" dans le contexte algorithmique fait référence à des systèmes d'intelligence artificielle, en particulier ceux de personnalisation, qui sont conçus ou qui évoluent de manière à identifier et exploiter activement les vulnérabilités des utilisateurs. Ces vulnérabilités peuvent être d'ordre psychologique (biais cognitifs, états émotionnels), informationnel (asymétrie d'information, manque de littératie numérique) ou financier (précarité, impulsivité). L'objectif de ces logiques est souvent d'inciter les utilisateurs à des comportements spécifiques – achat impulsif, partage excessif de données, engagement prolongé sur une plateforme – qui servent les intérêts de l'opérateur du système, parfois au détriment direct du bien-être de l'utilisateur.   

Ces logiques prédatrices trouvent une expression concrète et visible dans les "dark patterns". Il s'agit de tactiques de conception d'interfaces utilisateur (UI) et d'expériences utilisateur (UX) qui ont pour but de tromper, de contraindre ou de manipuler les utilisateurs pour qu'ils prennent des décisions qu'ils n'auraient pas prises autrement, ou qu'ils auraient prises différemment s'ils avaient été pleinement informés et libres de leurs choix. Des exemples courants incluent le "confirmshaming" (culpabiliser l'utilisateur pour qu'il accepte une offre), les "hidden costs" (révéler des coûts supplémentaires tardivement dans le processus d'achat), ou le "roach motel" (rendre l'inscription facile mais la désinscription délibérément complexe). La personnalisation joue un rôle d'amplificateur redoutable pour ces logiques : en analysant finement les données comportementales, les préférences et les caractéristiques individuelles, les algorithmes peuvent adapter les "dark patterns" pour cibler avec une précision accrue les failles spécifiques de chaque utilisateur, rendant la manipulation d'autant plus efficace et difficile à déceler.   

Il est crucial de distinguer les logiques prédatrices des simples erreurs de conception ou des biais involontaires. Si ces derniers peuvent également avoir des conséquences négatives, les logiques prédatrices impliquent souvent un degré d'intentionnalité, qu'elle soit explicite dans la conception ou implicite dans la définition des objectifs d'optimisation. En effet, lorsque les algorithmes de personnalisation sont optimisés de manière agressive pour des métriques court-termistes telles que le taux d'engagement, le temps passé sur la plateforme, ou le taux de conversion, sans considération éthique pour le bien-être de l'utilisateur, ils peuvent systémiquement converger vers des stratégies qui s'avèrent prédatrices. La pression concurrentielle et la recherche de maximisation des profits peuvent ainsi conduire à l'intégration de ces logiques, même si elles ne sont pas explicitement étiquetées comme "prédatrices" en interne.

2.2. Impacts Sociétaux et Éthiques

Les conséquences des logiques prédatrices algorithmiques sont multiples et touchent tant les individus que la société dans son ensemble. Pour les individus, l'exposition continue à ces mécanismes peut entraîner une perte significative d'autonomie, les choix étant subtilement orientés voire dictés par des systèmes opaques. Cela peut engendrer du stress, de l'anxiété, et un sentiment de harcèlement numérique, comme le souligne la Déclaration de Montréal. La création de dépendances, notamment aux réseaux sociaux ou aux jeux, est une autre conséquence grave, les algorithmes étant souvent conçus pour maximiser la rétention par des techniques de captation de l'attention. Sur le plan financier, les incitations à l'achat impulsif ou les abonnements cachés peuvent conduire à un endettement ou à des dépenses non souhaitées. De plus, la personnalisation extrême peut faciliter l'exposition ciblée à la désinformation ou à des contenus manipulant l'opinion, avec des risques pour la prise de décision éclairée.   

Au niveau sociétal, l'omniprésence de ces logiques érode la confiance des utilisateurs envers les services numériques et les entreprises qui les opèrent. Elle peut également contribuer à une fragmentation sociale accrue. Les algorithmes de personnalisation, en optimisant le contenu pour l'engagement individuel, peuvent créer des "bulles de filtres" ou des "chambres d'écho" , où les utilisateurs sont de moins en moins exposés à des perspectives diversifiées, ce qui peut polariser les opinions et nuire à la cohésion sociale. À terme, la manipulation algorithmique et la désinformation ciblée représentent des risques non négligeables pour le fonctionnement démocratique, en entravant la formation d'une opinion publique éclairée et en facilitant l'ingérence dans les processus électoraux.   

Il est fondamental de reconnaître que les impacts de ces logiques prédatrices ne sont pas distribués uniformément au sein de la population. Les individus ou groupes en situation de vulnérabilité sont souvent plus exposés et plus sévèrement affectés. Par exemple, les mineurs, de par leur moindre maturité cognitive et leur sensibilité accrue aux influences sociales, peuvent être des cibles privilégiées. De même, les personnes âgées, les individus en situation de handicap cognitif, ou ceux confrontés à des difficultés socio-économiques peuvent disposer de moins de ressources (cognitives, financières, informationnelles) pour identifier et résister à ces manipulations. Ainsi, une personnalisation qui se voudrait "également prédatrice" pour tous aurait en réalité des effets disproportionnés, exacerbant les inégalités existantes et marginalisant davantage les plus fragiles.   

2.3. La Nécessité d'un Encadrement Éthique et d'une Responsabilisation des Acteurs

Face à l'ampleur des impacts négatifs potentiels, il apparaît clairement que les approches purement techniques ou strictement légales sont insuffisantes pour encadrer les logiques prédatrices des algorithmes de personnalisation. Les lois, bien que nécessaires, peinent souvent à suivre le rythme effréné de l'innovation technologique, et l'autorégulation par l'industrie a montré ses limites, comme le suggère la critique de Sara M. Watson sur l'inefficacité de l'autorégulation dans le secteur technologique. Un simple "patch" technique ne suffit pas à corriger une logique fondamentalement orientée vers l'exploitation si les incitations économiques et les objectifs d'optimisation sous-jacents ne sont pas remis en question.   

C'est ici qu'intervient l'impératif d'un encadrement éthique robuste. Des cadres comme la Déclaration de Montréal  offrent des principes directeurs essentiels pour orienter le développement et le déploiement de l'IA vers des finalités bénéfiques pour l'humanité. En mettant l'accent sur le bien-être, l'autonomie, l'équité et la responsabilité, de tels cadres fournissent une boussole morale pour évaluer et réorienter les algorithmes de personnalisation.   

Au-delà des principes généraux, il existe un besoin criant d'une déontologie spécifique pour les professionnels qui sont en première ligne de la conception et du développement de ces algorithmes : les codeurs. Ce sont eux qui traduisent les objectifs (parfois ambigus ou purement commerciaux) en instructions exécutables par la machine. Une déontologie adaptée pourrait les outiller pour identifier les dérives potentielles, pour résister aux pressions visant à implémenter des fonctionnalités prédatrices, et pour intégrer des considérations éthiques "by design".

Cependant, la responsabilité ne saurait être uniquement individuelle, reposant sur les seuls épaules des codeurs, ni exclusivement organisationnelle. Les pressions du marché, la culture d'entreprise et les dynamiques de pouvoir internes jouent un rôle considérable dans les choix de conception. Par conséquent, un code de déontologie pour les codeurs, pour être efficace, doit s'inscrire dans une démarche plus large de gouvernance algorithmique et être soutenu par des structures organisationnelles qui valorisent et récompensent les comportements éthiques. Il s'agit donc de promouvoir une responsabilité partagée et systémique, qui engage à la fois les développeurs, les entreprises, les régulateurs et la société civile dans la construction d'un environnement numérique plus respectueux des droits et du bien-être de chacun. Cette interconnexion entre la modification des algorithmes (Question 2) et la formulation d'une déontologie pour ceux qui les créent (Question 3) est au cœur de la présente étude.   

3. État de l'Art
3.1. Cadres Éthiques pour une IA Responsable

La prise de conscience des impacts sociétaux de l'intelligence artificielle a conduit à l'élaboration de nombreux cadres éthiques visant à orienter son développement et son déploiement de manière responsable. Ces cadres, bien que variés dans leur origine et leur portée, convergent souvent sur des principes fondamentaux.

La Déclaration de Montréal pour un développement responsable de l'IA  constitue une référence centrale pour cette étude. Élaborée à travers un processus délibératif inclusif, elle énonce dix principes clés : le bien-être, le respect de l'autonomie, la protection de l'intimité et de la vie privée, la solidarité, la participation démocratique, l'équité, l'inclusion de la diversité, la prudence, la responsabilité et le développement soutenable. Chacun de ces principes offre des orientations précieuses pour analyser et contrer les logiques prédatrices des algorithmes de personnalisation. Par exemple, le principe de "respect de l'autonomie" s'oppose directement aux manipulations qui entravent le libre arbitre de l'utilisateur, tandis que celui de "bien-être" questionne les algorithmes générant du stress ou de la dépendance.   

Le Biosphere Code , bien qu'initialement axé sur les impacts écologiques des algorithmes, propose une approche holistique de la responsabilité qui s'avère inspirante pour une déontologie des codeurs. Ses sept principes – (1) un grand pouvoir algorithmique implique de grandes responsabilités ; (2) les algorithmes doivent servir l'humanité et la biosphère au sens large ; (3) les bénéfices et les risques des algorithmes doivent être distribués équitablement ; (4) les algorithmes doivent être flexibles, adaptatifs et conscients du contexte ; (5) les algorithmes doivent nous aider à anticiper l'inattendu ; (6) la collecte de données algorithmiques doit être ouverte et significative ; (7) les algorithmes doivent être inspirants, ludiques et beaux – transcendent leur application écologique initiale. La notion de responsabilité élargie (Principe 1), d'équité dans la distribution des impacts (Principe 3) et de transparence dans la collecte des données (Principe 6) sont directement transposables aux enjeux des algorithmes de personnalisation.   

D'autres cadres internationaux et nationaux enrichissent cette réflexion. La Recommandation de l'UNESCO sur l'éthique de l'IA  s'articule autour de quatre valeurs fondamentales (droits de l'homme et dignité humaine, vivre dans des sociétés pacifiques, justes et interdépendantes, assurer la diversité et l'inclusion, un environnement et des écosystèmes qui prospèrent) et de dix principes, dont la proportionnalité et l'innocuité, la sûreté et la sécurité, le droit au respect de la vie privée, la gouvernance multipartite, la responsabilité et la redevabilité, la transparence et l'explicabilité, la surveillance et la décision humaines, la durabilité, la sensibilisation et l'éducation, et l'équité et la non-discrimination. Ces principes renforcent l'idée d'une IA au service de l'humain et respectueuse de ses droits fondamentaux.   

Au niveau européen, l'AI Act et les lignes directrices de l'OCDE  mettent l'accent sur une approche basée sur les risques, avec des exigences accrues pour les systèmes d'IA à haut risque, notamment en termes de transparence, de robustesse, de surveillance humaine et de qualité des données. Ces cadres insistent sur la nécessité de mécanismes de redevabilité et de gestion des risques tout au long du cycle de vie de l'IA.   

Aux États-Unis, le Federal Data Ethics Framework  propose dix engagements pour guider l'utilisation éthique des données par le gouvernement fédéral, incluant le respect des lois, le respect du public, des individus et des communautés, le respect de la vie privée et de la confidentialité, l'honnêteté, l'intégrité et l'humilité, la redevabilité, la promotion de la transparence et la veille continue des développements technologiques. Ces engagements soulignent l'importance de la confiance du public et de la gestion responsable des données.   

Enfin, les Irish Guidelines for Trustworthy AI , alignées sur les travaux européens, identifient sept principes pour une IA digne de confiance : l'agentivité humaine et la surveillance, la robustesse technique et la sécurité, la vie privée et la gouvernance des données, la transparence, la diversité, la non-discrimination et l'équité, le bien-être sociétal et environnemental, et la redevabilité.   

Une analyse comparative de ces différents cadres révèle une convergence significative autour de principes clés tels que la transparence, l'équité, la responsabilité, le respect de la vie privée et la primauté du bien-être humain. Cependant, l'un des défis majeurs réside dans l'opérationnalisation de ces principes de haut niveau et leur application concrète aux spécificités techniques et contextuelles des algorithmes de personnalisation, notamment ceux qui manifestent des logiques prédatrices. Si le "quoi faire" éthique est de plus en plus consensuel, le "comment faire" pratique reste une question ouverte que ce rapport ambitionne d'explorer.

3.2. "Dark Patterns" et Mécanismes de Manipulation Algorithmique

Les "dark patterns" sont des éléments de conception d'interface utilisateur (UI) ou d'expérience utilisateur (UX) qui exploitent les biais cognitifs humains pour inciter les utilisateurs à effectuer des actions qu'ils n'auraient pas entreprises autrement, ou qui sont contraires à leurs intérêts. Ils représentent la manifestation la plus tangible des logiques prédatrices dans les environnements numériques. Une taxonomie de ces pratiques a été développée, identifiant plusieurs catégories récurrentes. Le site darkpatterns.org  et les travaux de chercheurs comme Brignull, Gray et al.  ont permis de les cataloguer. Parmi les plus courants, on trouve :   

Nagging (Harcèlement) : Interruptions persistantes ou demandes répétées pour une action (ex: activer les notifications, s'inscrire à une newsletter).   
Obstruction (Obstruction) : Rendre une action souhaitée par l'utilisateur (ex: se désabonner, supprimer un compte) délibérément difficile et fastidieuse. L'exemple type est le "Roach Motel" : facile d'entrer, difficile de sortir.   
Sneaking (Furtivité) : Cacher des informations importantes ou des coûts supplémentaires jusqu'à un stade avancé de l'interaction, ou inscrire l'utilisateur à des services sans consentement clair. Les "Hidden Costs" (coûts cachés) en sont une illustration.   
Interface Interference (Interférence d'Interface) : Manipuler l'interface pour attirer l'attention sur certaines options au détriment d'autres, ou rendre certaines options moins visibles ou plus difficiles d'accès. La "Preselection" (présélection d'options coûteuses ou moins respectueuses de la vie privée) est une tactique courante.   
Forced Action (Action Forcée) : Obliger l'utilisateur à effectuer une action non désirée pour accéder à une fonctionnalité ou un contenu souhaité.   
Confirmshaming (Culpabilisation) : Utiliser un langage qui culpabilise l'utilisateur s'il refuse une option ou une offre.   
Disguised Ads (Publicités Déguisées) : Présenter des publicités comme du contenu natif ou des éléments d'interface pour tromper l'utilisateur et l'inciter à cliquer.   
Trick Wording (Formulation Trompeuse) : Utiliser un langage ambigu ou déroutant pour que l'utilisateur consente à quelque chose qu'il ne comprend pas pleinement.   
Fake Scarcity/Urgency (Fausse Rareté/Urgence) : Créer une fausse impression de stock limité ou de temps limité pour une offre afin de précipiter la décision de l'utilisateur.   
Fake Social Proof (Fausse Preuve Sociale) : Afficher de faux témoignages, de fausses évaluations ou de faux indicateurs de popularité pour augmenter artificiellement la crédibilité d'un produit ou service.   
La personnalisation algorithmique exacerbe l'efficacité de ces "dark patterns" de manière significative. En analysant les comportements passés, les préférences, voire les traits de personnalité inférés, les algorithmes peuvent :

Cibler les "dark patterns" : Sélectionner le type de "dark pattern" le plus susceptible d'influencer un utilisateur spécifique en fonction de son profil psychologique.
Adapter l'intensité : Moduler l'agressivité ou la subtilité du "dark pattern" en fonction de la résistance perçue de l'utilisateur.
Dynamiser la manipulation : Modifier les "dark patterns" en temps réel en fonction des réactions de l'utilisateur, créant ainsi des boucles de manipulation adaptatives. Par exemple, un algorithme de recommandation peut exploiter le biais de confirmation en présentant de manière répétée des produits similaires à ceux déjà consultés, tout en utilisant des tactiques de fausse urgence ("Plus que 2 articles en stock!") pour pousser à l'achat. De même, les systèmes de recommandation de contenu sur les réseaux sociaux peuvent créer des "bulles de filtres" en personnalisant les flux d'information, ce qui, combiné à des "dark patterns" de type "nagging" pour maintenir l'engagement, peut isoler l'utilisateur et le rendre plus vulnérable à la désinformation ciblée.   
Ces mécanismes ne sont pas des incidents isolés, mais constituent souvent des "architectures de choix" délibérément conçues pour orienter le comportement de l'utilisateur. La personnalisation, dans ce contexte, devient un outil puissant pour affiner et individualiser la manipulation, rendant la détection et la résistance d'autant plus ardues pour l'utilisateur moyen. Le tableau ci-dessous synthétise quelques "dark patterns" courants, leur lien avec la personnalisation et les principes de la Déclaration de Montréal qu'ils peuvent violer.

Tableau 1 : Tableau Synthétique des "Dark Patterns" et Logiques Prédatrices Courantes

Type de "Dark Pattern"/Logique Prédatrice	Description du mécanisme	Exemple dans un algorithme de personnalisation	Impact psychologique/éthique sur l'utilisateur	Principe de la Déclaration de Montréal potentiellement violé 
Roach Motel 	Facile d'entrer dans une situation (ex: abonnement), mais très difficile d'en sortir.	Personnalisation des offres d'essai gratuit avec processus de désabonnement complexe et peu visible, adapté pour décourager l'utilisateur en fonction de son profil d'engagement.	Frustration, sentiment d'être piégé, perte financière.	Respect de l'autonomie, Bien-être.
Confirmshaming	Culpabiliser l'utilisateur pour qu'il accepte une option qu'il ne souhaite pas.	Messages personnalisés utilisant des informations sur les intérêts de l'utilisateur pour le faire douter de son refus (ex: "Non merci, je ne veux pas de recommandations pertinentes pour mes passions").	Culpabilité, pression psychologique, manipulation émotionnelle.	Respect de l'autonomie, Bien-être.
Hidden Costs 	Révéler des frais supplémentaires (livraison, taxes, options) tardivement dans le processus d'achat.	Personnalisation du parcours d'achat pour maximiser l'engagement avant de révéler les coûts finaux, en se basant sur la probabilité que l'utilisateur abandonne.	Frustration, sentiment de tromperie, perte financière.	Bien-être, Équité.
Forced Action 	Obliger l'utilisateur à effectuer une action non désirée (ex: créer un compte, partager des données) pour accéder à un service.	Personnalisation de l'accès à certaines fonctionnalités en fonction du profil de l'utilisateur, exigeant plus de données ou d'engagement de la part de ceux jugés "moins précieux" ou plus enclins à céder.	Perte de contrôle, violation de la vie privée, frustration.	Respect de l'autonomie, Protection de l'intimité.
Privacy Zuckering  (une forme de Sneaking)	Tromper l'utilisateur pour qu'il partage plus d'informations personnelles qu'il ne le souhaiterait.	Interfaces de consentement à la collecte de données personnalisées pour être délibérément confuses ou pour présélectionner des options de partage maximal, en fonction du niveau de littératie numérique inféré de l'utilisateur.	Violation de la vie privée, perte de contrôle sur les données personnelles, risque de réutilisation abusive.	Protection de l'intimité, Respect de l'autonomie.
Personalized Filter Bubbles / Echo Chambers 	Présenter un flux d'informations et d'opinions qui renforce les croyances existantes de l'utilisateur, limitant l'exposition à la diversité.	Algorithmes de recommandation de contenu (actualités, réseaux sociaux) optimisés pour l'engagement, qui apprennent à ne montrer que ce qui conforte l'utilisateur, basé sur son historique d'interaction.	Polarisation, réduction de la pensée critique, isolement informationnel, vulnérabilité à la désinformation.	Inclusion de la diversité, Participation démocratique, Respect de l'autonomie.
Exploitation de la Vulnérabilité (ex: addiction au jeu, achats compulsifs)	Identifier et cibler les utilisateurs ayant des comportements addictifs ou impulsifs avec des offres personnalisées qui exacerbent ces tendances.	Algorithmes de plateformes de jeux d'argent ou de e-commerce qui détectent des schémas de comportement vulnérable et envoient des notifications ou des promotions personnalisées pour inciter à la dépense ou au jeu.	Préjudice financier, détresse psychologique, aggravation de troubles comportementaux.	Bien-être, Équité, Prudence.
  
3.3. Approches pour l'Audit et la Modification Éthique des Algorithmes

Face aux risques posés par les logiques prédatrices et les "dark patterns" amplifiés par la personnalisation, plusieurs approches techniques et méthodologiques ont été développées pour auditer, comprendre et modifier les algorithmes dans une perspective éthique.

L'Intelligence Artificielle Explicable (Explainable AI - XAI)  regroupe un ensemble de techniques visant à rendre les décisions des modèles d'apprentissage automatique plus transparentes et interprétables. Des méthodes comme SHAP (SHapley Additive exPlanations) ou LIME (Local Interpretable Model-agnostic Explanations) permettent d'identifier les caractéristiques (features) qui influencent le plus une prédiction ou une recommandation spécifique. Dans le contexte des algorithmes de personnalisation, XAI peut être crucial pour :   

Identifier les biais : Détecter si des attributs sensibles (genre, origine ethnique, etc.) influencent indûment les recommandations.
Comprendre les logiques sous-jacentes : Révéler si un algorithme favorise des contenus spécifiques qui pourraient conduire à des bulles de filtres ou à la manipulation.
Auditer les "dark patterns" codés : Mettre en lumière comment certaines combinaisons de données utilisateur mènent à des recommandations ou des interfaces manipulatrices. L'intégration de XAI peut se faire à différentes étapes : en pré-traitement pour analyser les données d'entraînement, durant l'entraînement pour guider la conception du modèle, et en post-déploiement pour un monitoring continu et des audits. Cependant, les méthodes XAI ont des limitations, notamment en termes de scalabilité pour des systèmes très complexes et leur sensibilité au contexte spécifique d'application.   
L'Apprentissage Automatique Conscient de l'Équité (Fairness-Aware Machine Learning - FAML)  vise à concevoir des algorithmes qui ne discriminent pas injustement certains groupes d'individus. Cela implique d'abord de définir mathématiquement ce que l'on entend par "équité". Plusieurs définitions existent, souvent regroupées en trois catégories  :   

Indépendance (ou parité démographique/statistique) : La décision de l'algorithme doit être indépendante de l'appartenance à un groupe sensible.
Séparation (ou égalité des chances/égalité des faux positifs/négatifs) : La décision de l'algorithme, conditionnée par le résultat réel (la "vérité terrain"), doit être indépendante de l'appartenance à un groupe sensible.
Suffisance (ou calibration) : Le résultat réel, conditionné par le score de prédiction de l'algorithme, doit être indépendant de l'appartenance à un groupe sensible. Une fois une ou plusieurs métriques d'équité choisies, des techniques de mitigation des biais peuvent être appliquées  :   
Pré-processing : Modifier les données d'entraînement pour éliminer les biais (ex: ré-échantillonnage, re-pondération des instances, transformation des données).
In-processing : Modifier l'algorithme d'apprentissage lui-même en ajoutant des contraintes d'équité dans la fonction d'optimisation (ex: régularisation, optimisation sous contraintes).
Post-processing : Ajuster les prédictions du modèle une fois qu'il a été entraîné pour satisfaire les critères d'équité (ex: calibration des scores, modification des seuils de décision). Les techniques FAML sont essentielles pour corriger les discriminations, mais leur application à des logiques prédatrices délibérées pose un défi : si l'objectif fondamental de l'algorithme reste l'exploitation, le FAML pourrait être utilisé pour rendre cette exploitation "équitablement distribuée" plutôt que de l'éliminer. L'efficacité de FAML dépend donc crucialement de la volonté de redéfinir les objectifs d'optimisation au-delà des métriques purement commerciales.
L'Évaluation de l'Impact Algorithmique (Algorithmic Impact Assessment - AIA)  est un processus structuré, souvent sous forme de questionnaire, visant à identifier, évaluer et atténuer les risques potentiels associés à un système de décision automatisé avant et après son déploiement. Le cadre canadien  est un exemple notable, évaluant les impacts sur les droits des individus, leur santé, leurs intérêts économiques, et l'écosystème. L'AIA constitue un outil de gouvernance important pour s'assurer que les considérations éthiques sont prises en compte de manière proactive.   

Les Contre-explications (Counterfactual Explanations)  offrent une autre approche pour l'explicabilité et le recours. Elles visent à expliquer à un utilisateur "quelle est la plus petite modification à apporter à ses données d'entrée pour obtenir un résultat souhaité différent". Pour les algorithmes de personnalisation, cela pourrait aider un utilisateur à comprendre pourquoi il ne voit pas certains types de contenu et comment il pourrait modifier son profil ou ses interactions pour y accéder, renforçant ainsi son autonomie.   

Ces approches techniques et méthodologiques sont prometteuses. Néanmoins, leur efficacité contre les logiques délibérément prédatrices, par opposition aux biais involontaires, est conditionnée par la volonté organisationnelle de les mettre en œuvre et, plus fondamentalement, de réévaluer les objectifs d'optimisation des algorithmes. Si la finalité première demeure une extraction de valeur agressive au détriment de l'utilisateur, ces outils, aussi sophistiqués soient-ils, risquent d'être contournés, sous-utilisés, ou leurs conclusions ignorées. Cela souligne l'importance des dynamiques de pouvoir et des pressions du marché au sein des organisations développant ces technologies.   

3.4. Codes de Déontologie pour les Professionnels de la Tech et de l'IA

Les codes de déontologie professionnelle jouent un rôle crucial en établissant des normes de conduite, en guidant la prise de décision éthique et en renforçant la confiance du public envers une profession. Dans le domaine du numérique et de l'IA, plusieurs codes font autorité.

Le Code d'Éthique et de Conduite Professionnelle de l'ACM (Association for Computing Machinery)  est l'un des plus reconnus. Il s'articule autour de principes éthiques généraux (contribuer à la société et au bien-être humain, éviter de nuire, être honnête et digne de confiance, être juste et ne pas discriminer, respecter le travail intellectuel, respecter la vie privée, honorer la confidentialité) et de responsabilités professionnelles plus spécifiques (atteindre une haute qualité, maintenir la compétence, connaître et respecter les règles, accepter l'évaluation professionnelle, évaluer les systèmes et leurs impacts y compris les risques, travailler dans ses domaines de compétence, favoriser la sensibilisation du public, accéder aux ressources de manière autorisée, concevoir des systèmes robustes et sécurisés). Ces principes fournissent une base solide pour aborder de nombreuses questions éthiques soulevées par les algorithmes de personnalisation.   

Le Code d'Éthique en Ingénierie Logicielle (Software Engineering Code of Ethics and Professional Practice), conjointement développé par l'IEEE-Computer Society et l'ACM , est structuré autour de huit principes fondamentaux : Public, Client et Employeur, Produit, Jugement, Management, Profession, Collègues, et Soi. Ce code met un accent particulier sur l'intérêt public comme considération primordiale, la nécessité de fournir des produits de la plus haute qualité possible, et l'importance de maintenir l'intégrité et l'indépendance du jugement professionnel. Ses clauses détaillées offrent des directives concrètes pour les ingénieurs logiciels.   

Bien que ces codes existants offrent des cadres éthiques robustes et largement applicables, leur généralité peut parfois limiter leur pertinence directe face aux défis très spécifiques posés par les algorithmes de personnalisation et leurs potentielles dérives prédatrices. Par exemple, si le principe "éviter de nuire" est central, un code destiné spécifiquement aux codeurs d'algorithmes de personnalisation devrait peut-être insister davantage sur une obligation proactive d'identifier les vulnérabilités spécifiques des utilisateurs et sur la responsabilité inhérente à la conception des "architectures de choix" numériques qui façonnent quotidiennement l'expérience en ligne. Il ne s'agit plus seulement de "ne pas nuire", mais de "concevoir activement pour le bien-être et l'autonomie de l'utilisateur", étant donné le pouvoir d'influence considérable que confère la personnalisation. Un code plus ciblé pourrait ainsi mieux équiper les codeurs pour naviguer les dilemmes éthiques propres à leur domaine d'activité.

4. Méthodologie
La présente étude adopte une approche méthodologique mixte, combinant l'analyse normative de cadres éthiques, l'étude comparative de codes de déontologie existants, et une démarche constructive pour l'élaboration de propositions concrètes.

4.1. Approche pour la Question 2 (Modification des Algorithmes)

Pour répondre à la question des étapes à envisager pour modifier les modalités de fonctionnement des algorithmes de personnalisation générant des logiques prédatrices, la méthodologie s'appuie principalement sur une analyse normative des principes de la Déclaration de Montréal pour un développement responsable de l'IA. Cette analyse a consisté à :   

Identifier les dix principes de la Déclaration et à évaluer leur pertinence spécifique pour contrer les caractéristiques des logiques prédatrices (manipulation, exploitation de vulnérabilités, atteinte à l'autonomie, etc.). Une attention particulière a été portée aux principes tels que le bien-être, le respect de l'autonomie, la protection de l'intimité et de la vie privée, l'équité, et la prudence, qui sont directement interpellés par les dérives de la personnalisation.   
Adopter une démarche déductive où ces principes éthiques de haut niveau sont traduits en impératifs concrets pour la conception et le fonctionnement des algorithmes. Il s'agit de passer du "pourquoi" éthique au "comment" technique et organisationnel.
Intégrer des outils et techniques d'audit et de mitigation identifiés dans l'état de l'art comme moyens d'opérationnaliser ces principes. Cela inclut l'utilisation de l'Évaluation de l'Impact Algorithmique (AIA)  pour le diagnostic et l'évaluation des risques, ainsi que les méthodes d'Intelligence Artificielle Explicable (XAI)  et d'Apprentissage Automatique Conscient de l'Équité (FAML)  pour l'identification des biais, la compréhension des mécanismes et la correction technique des algorithmes.   
Cette approche vise à garantir que les étapes de modification proposées ne soient pas seulement techniquement réalisables, mais aussi et surtout éthiquement fondées et alignées sur un cadre de valeurs reconnu internationalement.

4.2. Approche pour la Question 3 (Code de Déontologie)

La formulation d'un code de déontologie pour les codeurs d'algorithmes de personnalisation a mobilisé une approche multi-facettes :

Une analyse thématique des sept principes du Biosphere Code  a été menée pour en extraire l'essence philosophique et les orientations fondamentales (responsabilité élargie, service à l'humain, équité, transparence, adaptabilité) qui pourraient être transposées et adaptées au contexte spécifique des algorithmes de personnalisation.   
Une étude comparative approfondie a été réalisée avec des codes de déontologie établis dans les domaines du génie logiciel et de l'informatique, notamment le Code d'Éthique de l'ACM  et le Code d'Éthique en Ingénierie Logicielle de l'IEEE-CS/ACM. D'autres cadres éthiques pertinents, tels que les principes de l'UNESCO pour l'éthique de l'IA , le Federal Data Ethics Framework (US) , et les Irish Guidelines for Trustworthy AI , ont également été examinés pour identifier les meilleures pratiques, les convergences, ainsi que les éventuelles lacunes par rapport aux enjeux spécifiques de la personnalisation.   
Une approche constructive a été adoptée pour proposer une structure et un contenu pour un nouveau code de déontologie. Cette démarche s'est appuyée sur les principes directeurs d'élaboration d'un code de déontologie efficace, tels que l'utilité (le code doit être pratique et applicable), la pluralité (le processus d'élaboration doit être inclusif), l'impartialité et l'intégrité (le code doit être exempt de biais indus), et la transparence (tant dans son élaboration que dans son contenu).   
L'objectif était de ne pas réinventer la roue, mais de s'appuyer sur la sagesse collective incarnée dans les cadres existants, tout en adaptant et en enrichissant ces fondations pour répondre aux défis uniques posés par la puissance et l'omniprésence des algorithmes de personnalisation.

4.3. Sélection et Analyse des Sources

La sélection des sources a été guidée par la requête initiale de l'utilisateur, qui a spécifiquement désigné la Déclaration de Montréal et le Biosphere Code comme références principales pour les questions 2 et 3 respectivement. Ces documents ont donc bénéficié d'une attention prioritaire.

Les autres sources et documents de recherche ont été utilisés pour :

Contextualiser la problématique : Définir et illustrer les concepts de logiques prédatrices  et de "dark patterns".   
Identifier les outils techniques et méthodologiques : Explorer les approches d'audit (AIA ), d'explicabilité (XAI ), et de mitigation des biais (FAML ).   
Fournir des cadres comparatifs : Analyser d'autres codes de déontologie  et principes éthiques  pour enrichir la réflexion.   
Explorer les dynamiques organisationnelles et sociétales : Comprendre les pressions et les défis liés à l'implémentation de l'éthique dans les entreprises technologiques.   
Une limitation reconnue de cette étude est l'inaccessibilité de certains documents Google Drive relatifs au Biosphere Code. L'analyse de ce dernier s'est donc appuyée sur les informations publiques disponibles (articles de blog, résumés ). De plus, la nature des "snippets" de recherche fournis implique parfois un caractère généraliste qui a nécessité une interprétation et une application prudente au contexte spécifique des algorithmes de personnalisation.   

La méthodologie adoptée vise à assurer la rigueur académique tout en produisant des résultats actionnables. L'enjeu n'est pas seulement de critiquer ou d'analyser, mais de proposer des pistes de solutions concrètes et éthiquement fondées pour encadrer le développement des algorithmes de personnalisation. La traduction des principes éthiques de haut niveau en recommandations pratiques pour les codeurs et les organisations est un fil conducteur de cette démarche, cherchant à éviter l'écueil d'une réflexion purement théorique déconnectée des réalités du développement logiciel.

5. Résultats et Limitations
Cette section présente les résultats de l'analyse menée pour répondre aux deux questions de recherche. La première partie détaille les étapes proposées pour modifier les algorithmes de personnalisation générant des logiques prédatrices, en s'appuyant sur la Déclaration de Montréal. La seconde partie esquisse les fondements d'un code de déontologie pour les codeurs de ces algorithmes, inspiré par le Biosphere Code et d'autres cadres éthiques.

5.1. Partie 1 : Étapes pour Modifier les Algorithmes de Personnalisation Prédateurs (Réponse à Q2)

La modification des algorithmes de personnalisation qui engendrent des logiques prédatrices ne peut se résumer à une simple correction technique. Elle exige une démarche systémique et itérative, ancrée dans des principes éthiques solides. La Déclaration de Montréal  offre un cadre directeur pour cette transformation. Les étapes suivantes, intégrant diagnostic, redéfinition, modification technique et gouvernance continue, visent à opérationnaliser ces principes. Ce processus doit être envisagé non comme une intervention ponctuelle, mais comme l'instauration d'une boucle de rétroaction éthique continue au sein du cycle de vie de l'algorithme, transformant la "conformité éthique" en une pratique dynamique.   

5.1.1. Phase 1 : Diagnostic Éthique et Identification des Logiques Prédatrices

Avant toute modification, un diagnostic approfondi s'impose pour identifier précisément où et comment l'algorithme de personnalisation dévie vers des logiques prédatrices. Cette phase s'appuie sur l'application directe des principes de la Déclaration de Montréal  et l'utilisation d'outils d'audit.   

Application des principes de la Déclaration de Montréal :

Principe de Bien-être : L'algorithme est-il une source de mal-être pour l'utilisateur? Contribue-t-il à augmenter le stress, l'anxiété ou le sentiment de harcèlement? Exploite-t-il des vulnérabilités psychologiques (ex: tendance à l'addiction, impulsivité) pour atteindre ses objectifs?   
Principe de Respect de l'autonomie : L'algorithme réduit-il la capacité de l'utilisateur à faire des choix éclairés et à contrôler son environnement numérique? Crée-t-il des dépendances par des techniques de captation de l'attention? Prescrit-il, directement ou indirectement, un mode de vie ou des comportements spécifiques par des mécanismes de surveillance ou d'incitation contraignants?   
Principe de Protection de l'intimité et de la vie privée : Y a-t-il une collecte de données personnelles allant au-delà de ce qui est strictement nécessaire et consenti? Les profils d'utilisateurs sont-ils construits et utilisés pour influencer le comportement sans un consentement libre et éclairé, voire à des fins manipulatrices?   
Principe d'Équité : L'algorithme engendre-t-il ou renforce-t-il des discriminations fondées sur des caractéristiques sociales, ethniques, de genre, etc.? Cible-t-il de manière disproportionnée et injuste certains groupes, notamment les plus vulnérables?   
Principe d'Inclusion de la diversité : La personnalisation conduit-elle à un appauvrissement de l'information reçue par l'utilisateur, en l'enfermant dans des "bulles de filtres" ou des "chambres d'écho" qui limitent son exposition à la diversité des opinions et des expériences?   
Outils d'audit et d'analyse :

Évaluation de l'Impact Algorithmique (AIA) : Mettre en œuvre une AIA, inspirée de cadres comme celui du Canada , pour évaluer systématiquement les risques potentiels de l'algorithme sur les droits des individus, leur santé, leurs intérêts économiques et leur environnement informationnel.   
Techniques d'Intelligence Artificielle Explicable (XAI) : Utiliser des méthodes XAI (telles que SHAP ou LIME) pour "ouvrir la boîte noire" de l'algorithme. L'objectif est de comprendre quels facteurs (données d'entrée, paramètres du modèle) conduisent à des recommandations ou des comportements potentiellement prédateurs. Par exemple, XAI peut révéler si un algorithme de recommandation de produits financiers cible agressivement des profils surendettés avec des offres de crédit à haut risque.   
5.1.2. Phase 2 : Redéfinition des Objectifs et Conception Éthique ("Ethics by Design")

Une fois les logiques prédatrices identifiées, il est crucial de ne pas se contenter de les "corriger" en surface. Il faut souvent redéfinir les objectifs mêmes de l'algorithme de personnalisation pour les aligner sur des valeurs éthiques.

Alignement avec la Déclaration de Montréal : Les objectifs de l'algorithme doivent être explicitement reformulés pour promouvoir activement le bien-être de l'utilisateur, son autonomie décisionnelle, l'équité des résultats et l'inclusion de la diversité, conformément aux principes de la Déclaration. Cela peut signifier, par exemple, qu'un algorithme de recommandation de contenu ne vise plus seulement à maximiser le temps passé, mais aussi à favoriser la découverte de perspectives variées ou à proposer des pauses.   
Application du Principe de Prudence : La conception (ou la reconception) de l'algorithme doit intégrer une anticipation rigoureuse des conséquences néfastes potentielles et prévoir des mesures préventives dès les premières étapes. Cela inclut la considération des "pires scénarios" et la mise en place de garde-fous.   
Mise en œuvre du Principe de Participation démocratique : Impliquer un éventail de parties prenantes – utilisateurs finaux (notamment issus de groupes divers et potentiellement vulnérables), experts en éthique, psychologues, sociologues – dans la discussion et la redéfinition des fonctionnalités, des limites et des indicateurs de succès de la personnalisation. L'objectif est de s'assurer que l'algorithme sert des intérêts légitimes et socialement acceptables.   
Cette phase de redéfinition est fondamentale car elle vise à déplacer le locus de contrôle de la personnalisation. Plutôt que d'être un processus entièrement déterminé par les concepteurs et les objectifs de la plateforme, la personnalisation doit évoluer vers un système où l'utilisateur dispose d'outils significatifs pour comprendre, façonner et contrôler son expérience personnalisée, en accord avec le principe de respect de l'autonomie de la Déclaration de Montréal.   

5.1.3. Phase 3 : Modification Technique des Algorithmes

Sur la base du diagnostic et des objectifs redéfinis, des modifications techniques concrètes doivent être apportées à l'algorithme.

Application des techniques FAML (Fairness-Aware Machine Learning)  :   

Pré-processing : Analyser et corriger les biais présents dans les données d'entraînement. Si, par exemple, les données historiques révèlent qu'un "dark pattern" a été particulièrement "efficace" (c'est-à-dire manipulateur) sur un groupe d'utilisateurs vulnérables, ces données doivent être nettoyées, re-pondérées ou complétées pour ne pas que l'algorithme apprenne à reproduire cette exploitation.
In-processing : Modifier l'algorithme d'apprentissage lui-même. Cela peut impliquer d'introduire des contraintes d'équité, de bien-être ou de diversité directement dans la fonction objectif que l'algorithme cherche à optimiser. Par exemple, on pourrait pénaliser les séquences de recommandations qui mènent à une surexposition à des contenus addictifs ou qui réduisent excessivement la diversité des informations présentées.
Post-processing : Intervenir sur les sorties de l'algorithme. Cela peut consister à filtrer ou à réorganiser les recommandations pour garantir une certaine diversité, à limiter la fréquence de certaines sollicitations, ou à intégrer des options claires de "désengagement" ou de "voir moins de contenu similaire", en lien avec le droit à la déconnexion et au contrôle de l'utilisateur.   
Intégration de la Transparence et du Contrôle Utilisateur  :   

Explicabilité : Fournir aux utilisateurs des explications intelligibles sur les raisons pour lesquelles certaines recommandations leur sont faites. Les techniques XAI (comme LIME pour des explications locales) ou les contre-explications  ("Pour voir plus de contenu X, vous pourriez interagir avec Y") peuvent être mobilisées.   
Tableaux de bord de personnalisation : Développer des interfaces permettant aux utilisateurs de visualiser les principales données utilisées pour leur profilage, de comprendre comment leurs actions influencent la personnalisation, de modifier leurs préférences, de demander la correction ou la suppression de certaines données, et d'ajuster le niveau ou le type de personnalisation souhaité.
5.1.4. Phase 4 : Évaluation Continue et Gouvernance

La modification d'un algorithme n'est pas une fin en soi. Une vigilance et une gouvernance continues sont indispensables.

Application du Principe de Responsabilité  : Mettre en place des mécanismes de surveillance continue (monitoring) pour détecter l'émergence de nouvelles logiques prédatrices, d'effets indésirables non anticipés, ou de dérives du modèle ("model drift"). Il est crucial de maintenir une supervision humaine significative : la décision finale dans des contextes critiques ou à fort impact sur l'individu devrait toujours impliquer un jugement humain.   
Audits Éthiques Réguliers : Faire réaliser des audits éthiques par des entités internes dédiées (ex: comité d'éthique) et/ou par des tiers indépendants pour évaluer périodiquement la conformité de l'algorithme aux principes éthiques et aux objectifs redéfinis. L'AIA  devrait être revue et mise à jour, notamment avant toute modification substantielle du système ou en cas de changement de contexte d'utilisation.   
Canaux de Signalement et de Recours : Établir des canaux clairs, accessibles et efficaces permettant aux utilisateurs de signaler des problèmes, des recommandations inappropriées, ou des comportements perçus comme prédateurs. Des mécanismes de recours et de remédiation doivent être prévus. Des canaux similaires devraient exister pour les développeurs et autres employés afin qu'ils puissent alerter sur des dérives éthiques potentielles (mécanismes de "whistleblowing" protégés).
Le tableau suivant illustre la correspondance entre certains principes de la Déclaration de Montréal et des stratégies de modification des algorithmes de personnalisation prédateurs.

Tableau 2 : Correspondance entre Principes de la Déclaration de Montréal et Stratégies de Modification des Algorithmes de Personnalisation Prédateurs

Principe de la Déclaration de Montréal 	Manifestation de la logique prédatrice violant ce principe	Étape/Stratégie de modification proposée
Bien-être	Exploitation de vulnérabilités (ex: addiction, anxiété), génération de stress.	Audit XAI pour identifier les facteurs de manipulation ; Redéfinition de l'objectif de l'algorithme pour inclure des métriques de bien-être utilisateur ; Limitation de la fréquence/intensité des sollicitations.
Respect de l'autonomie	Création de dépendance, limitation du contrôle utilisateur, prescription de comportements.	Intégration de mécanismes de contrôle utilisateur (tableaux de bord) ; Offre d'options de désengagement claires ; Contre-explications pour éclairer les choix.
Protection de l'intimité et de la vie privée	Collecte excessive de données, profilage invasif sans consentement éclairé pour manipulation.	Audit des flux de données ; Application stricte de la minimisation des données ; Renforcement des mécanismes de consentement ; Techniques de "Privacy-Preserving Machine Learning".
Équité	Création ou renforcement de discriminations, ciblage injuste de groupes vulnérables.	Audit de biais avec XAI ; Application de techniques FAML (pré-, in-, ou post-processing) pour assurer la parité statistique ou l'égalité des chances ; Diversification des données d'entraînement.
Inclusion de la diversité	Création de bulles de filtres ou de chambres d'écho, appauvrissement informationnel.	Modification des algorithmes de recommandation pour inclure des objectifs de diversité et de sérendipité ; Offre d'options pour explorer des contenus hors profil.
Prudence	Déploiement d'algorithmes sans évaluation suffisante des risques de conséquences néfastes.	Réalisation systématique d'AIA avant et après modification ; Tests rigoureux en conditions variées ; Mise en place de systèmes de monitoring des impacts.
Participation démocratique	Opacité du fonctionnement algorithmique, absence de justification des recommandations.	Implémentation de XAI pour fournir des explications intelligibles ; Consultation des utilisateurs et parties prenantes dans la (re)conception ; Publication de rapports de transparence sur le fonctionnement général de la personnalisation.
Responsabilité	Difficulté d'attribuer la responsabilité en cas de dommage, absence de recours.	Établissement de chaînes de responsabilité claires pour la conception, le déploiement et la surveillance ; Mise en place de mécanismes de signalement et de recours effectifs pour les utilisateurs ; Maintien d'une supervision humaine pour les décisions critiques.
  
5.2. Partie 2 : Formulation d'un Code de Déontologie pour les Codeurs d'Algorithmes de Personnalisation (Réponse à Q3)

La création d'un code de déontologie spécifique pour les codeurs d'algorithmes de personnalisation répond à un besoin d'encadrement éthique au plus près des pratiques de conception et de développement. S'inspirer du Biosphere Code  et d'autres cadres pertinents permet de jeter les bases d'un tel code, en l'ancrant dans une vision de responsabilité élargie et systémique. L'enjeu est de transcender la simple conformité technique pour embrasser une responsabilité que l'on pourrait qualifier d'"écologique" vis-à-vis du "paysage informationnel et décisionnel" de l'utilisateur. Tout comme le Biosphere Code envisage l'impact des algorithmes sur l'écosystème planétaire , un code pour les codeurs de personnalisation doit considérer les effets systémiques de leurs créations sur l'autonomie, la perception du monde et le bien-être psychologique des individus. Les "dark patterns" et les bulles de filtres peuvent être vus comme des formes de "pollution" de cet écosystème informationnel personnel.   

5.2.1. Inspiration du Biosphere Code et Adaptation

Plusieurs principes du Biosphere Code  peuvent être adaptés pour fonder un code de déontologie pour les codeurs d'algorithmes de personnalisation :   

Principe 1 du Biosphere Code (Avec de grands pouvoirs algorithmiques viennent de grandes responsabilités) : Adapté, cela signifie que les codeurs, en façonnant les expériences personnalisées, détiennent un pouvoir significatif sur les utilisateurs. Ils doivent donc assumer une responsabilité explicite des impacts de leurs algorithmes sur le bien-être, l'autonomie et la vie privée des utilisateurs, ainsi que sur des enjeux sociétaux plus larges comme l'équité et la diversité informationnelle.
Principe 2 (Les algorithmes devraient servir l'humanité et la biosphère au sens large) : Transposé, ce principe exige que les algorithmes de personnalisation soient conçus pour servir prioritairement les intérêts légitimes et le développement positif des utilisateurs, et non pour les exploiter à des fins purement commerciales ou manipulatrices. L'objectif doit être une "personnalisation responsable" qui améliore la vie sans dégrader l'autonomie ou le bien-être.
Principe 3 (Les bénéfices et les risques des algorithmes devraient être distribués équitablement) : Ce principe est directement pertinent. Les codeurs doivent activement s'efforcer de concevoir des systèmes de personnalisation qui ne créent pas ou n'exacerbent pas les inégalités, les biais ou les discriminations. Les risques (ex: manipulation, exclusion) et les bénéfices (ex: pertinence, découverte) de la personnalisation doivent être considérés pour tous les groupes d'utilisateurs, avec une attention particulière pour les plus vulnérables.   
Principe 4 (Les algorithmes devraient être flexibles, adaptatifs et conscients du contexte) : Les algorithmes de personnalisation doivent être conçus de manière à pouvoir être modifiés ou corrigés si des effets néfastes ou inattendus émergent. Ils doivent être développés avec une conscience aiguë du contexte d'utilisation et des vulnérabilités potentielles des différents profils d'utilisateurs. La maintenabilité et la capacité d'intégrer des considérations éthiques évolutives sont essentielles.   
Principe 6 (La collecte de données algorithmiques devrait être ouverte et significative) : Ce principe appelle à la transparence concernant les données collectées pour la personnalisation, leur finalité, et la manière dont elles sont utilisées. Les utilisateurs doivent pouvoir comprendre pourquoi leurs données sont nécessaires et comment elles façonnent leur expérience. Les jeux de données utilisés pour l'entraînement doivent être validés pour éviter les biais cachés.
5.2.2. Structure et Principes Fondamentaux Proposés pour le Code de Déontologie

En s'inspirant de ces adaptations et en intégrant les apports d'autres codes (ACM , IEEE-CS/ACM ) et cadres éthiques (Déclaration de Montréal , UNESCO , Federal Data Ethics Framework , Irish Guidelines ), la structure suivante est proposée pour le code de déontologie des codeurs d'algorithmes de personnalisation :   

Préambule :

Reconnaissance du rôle et de l'impact significatifs des algorithmes de personnalisation.
Affirmation de l'engagement des codeurs envers des pratiques éthiques et responsables.
Soulignement de la nécessité de protéger les utilisateurs contre les logiques prédatrices et manipulatrices.
Principes Fondamentaux :

Primauté du Bien-être et de l'Autonomie de l'Utilisateur :

Inspiration : Déclaration de Montréal (Bien-être, Respect de l'autonomie), ACM (1.1, 1.2).
Justification/Adaptation : La personnalisation doit viser à enrichir l'expérience utilisateur et à renforcer sa capacité à faire des choix éclairés, et non à le manipuler, le contraindre ou exploiter ses vulnérabilités.
Implication Pratique : Concevoir des interfaces et des logiques qui offrent un contrôle réel à l'utilisateur sur son expérience personnalisée ; éviter les "dark patterns" ; évaluer l'impact sur la santé mentale et l'autonomie.
Responsabilité des Impacts Algorithmiques :

Inspiration : Biosphere Code (P1), Déclaration de Montréal (Responsabilité), ACM (1.2), IEEE-CS/ACM (P1 : Public).
Justification/Adaptation : Les codeurs doivent prendre conscience et assumer la responsabilité des conséquences directes et indirectes, prévues et imprévues, de leurs algorithmes sur les individus et la société.
Implication Pratique : Mener des évaluations d'impact (AIA) ; mettre en place un monitoring des effets ; être prêt à corriger les algorithmes si des impacts négatifs sont détectés.
Justice, Équité et Non-Discrimination Algorithmique :

Inspiration : Biosphere Code (P3), Déclaration de Montréal (Équité, Inclusion de la diversité), ACM (1.4), UNESCO (Équité et non-discrimination).
Justification/Adaptation : Les algorithmes de personnalisation ne doivent pas créer, perpétuer ou amplifier les biais et les discriminations à l'encontre d'individus ou de groupes.
Implication Pratique : Auditer les données et les modèles pour détecter les biais ; utiliser des techniques FAML ; concevoir pour l'inclusivité et l'accessibilité ; tester sur des populations diverses.
Transparence et Explicabilité des Processus de Personnalisation :

Inspiration : Biosphere Code (P6), Déclaration de Montréal (Participation démocratique), ACM (1.3), UNESCO (Transparence et explicabilité), Irish Guidelines (Transparency).
Justification/Adaptation : Les utilisateurs ont le droit de comprendre comment et pourquoi leur expérience est personnalisée. L'opacité favorise la méfiance et la manipulation.
Implication Pratique : Documenter clairement le fonctionnement des algorithmes ; fournir des explications intelligibles aux utilisateurs (XAI, contre-explications) ; être transparent sur les données utilisées et les objectifs de la personnalisation.
Protection Renforcée de la Vie Privée et des Données Personnelles :

Inspiration : Déclaration de Montréal (Protection de l'intimité), ACM (1.6), IEEE-CS/ACM (P3.12), UNESCO (Vie privée), Federal Data Ethics Framework (Respect Privacy).
Justification/Adaptation : La personnalisation repose sur les données personnelles ; leur protection est donc primordiale. Le principe de "Privacy by Design" doit être la norme.
Implication Pratique : Appliquer la minimisation des données ; obtenir un consentement éclairé et granulaire ; sécuriser les données ; permettre aux utilisateurs d'accéder, de corriger et de supprimer leurs données.
Intégrité Professionnelle, Compétence et Prudence :

Inspiration : ACM (1.3, 2.1, 2.2, 2.6), IEEE-CS/ACM (P4: Jugement, P8: Self), Déclaration de Montréal (Prudence).
Justification/Adaptation : Le développement d'algorithmes de personnalisation éthiques requiert un haut niveau de compétence technique, une conscience des enjeux éthiques, et une démarche prudente.
Implication Pratique : Se former continuellement aux aspects techniques et éthiques ; être honnête sur les limites de ses compétences et des systèmes développés ; anticiper les risques et les usages détournés ; privilégier la robustesse et la sécurité.
Conception Adaptative et Ouverte à la Correction :

Inspiration : Biosphere Code (P4).
Justification/Adaptation : Les impacts des algorithmes peuvent évoluer. Les systèmes doivent être conçus pour permettre des ajustements et des corrections en cas d'effets négatifs.
Implication Pratique : Concevoir des algorithmes modulaires et maintenables ; mettre en place des mécanismes de feedback et de révision continue ; documenter les versions et les modifications.
Collaboration Multidisciplinaire et Dialogue avec les Parties Prenantes :

Inspiration : Déclaration de Montréal (Participation démocratique), UNESCO (Gouvernance et collaboration multipartites).
Justification/Adaptation : Les enjeux éthiques de la personnalisation sont complexes et dépassent le seul cadre technique.
Implication Pratique : Solliciter et intégrer l'avis d'experts en éthique, en sciences sociales, et des représentants des utilisateurs dans le processus de conception et d'évaluation ; favoriser une culture de discussion ouverte sur les dilemmes éthiques au sein des équipes.
Règles de Pratique Professionnelle :

Cette section déclinerait chaque principe fondamental en actions et comportements attendus plus spécifiques pour les codeurs dans leur travail quotidien. Par exemple, sous "Transparence et Explicabilité" : "Les codeurs doivent s'efforcer de documenter les principales variables et logiques qui influencent les recommandations de l'algorithme de personnalisation, d'une manière qui puisse être communiquée de façon simplifiée aux utilisateurs." Ou sous "Protection Renforcée de la Vie Privée" : "Les codeurs doivent implémenter par défaut les paramètres de confidentialité les plus protecteurs pour l'utilisateur ('privacy by default')".
Engagement envers la Profession et la Société :

Devoir de contribuer positivement à la réputation de la profession.
Responsabilité de partager les connaissances sur les pratiques éthiques.
Devoir d'alerte en cas de pratiques non éthiques graves.
Mécanismes d'Application, de Soutien et de Révision du Code :

Procédures pour interpréter le code et résoudre les dilemmes.
Soutien institutionnel pour les codeurs qui soulèvent des préoccupations éthiques.
Engagement à réviser et mettre à jour le code périodiquement en fonction de l'évolution des technologies et des compréhensions éthiques.
5.2.3. Intégration des Principes d'Élaboration d'un Code

Conformément aux principes d'élaboration d'un code de déontologie efficace  :   

Utilité : Le code doit être formulé en des termes clairs, concrets et directement applicables aux situations rencontrées par les codeurs d'algorithmes de personnalisation. Il doit fournir des repères pour la prise de décision.
Pluralité : Son processus d'élaboration et de révision devrait idéalement impliquer une consultation large : codeurs, data scientists, product managers, experts en UX, éthiciens, juristes, représentants d'utilisateurs et de la société civile.
Impartialité et Intégrité : Le code doit viser l'intérêt des utilisateurs et de la société, et ne pas être un simple outil de légitimation des pratiques commerciales existantes. Son intégrité doit être garantie par un processus de gouvernance indépendant.
Transparence : Le processus d'élaboration, les justifications des principes et des règles, ainsi que les mécanismes de révision du code doivent être transparents et accessibles.
Pour qu'un tel code soit véritablement efficace, il ne peut rester un simple document consultatif. Il doit être activement promu, intégré dans la formation initiale et continue des codeurs, et surtout, soutenu par une culture organisationnelle qui valorise la responsabilité éthique. Cela pourrait impliquer son intégration dans les outils de développement (ex: linters éthiques, checklists pour les revues de code), dans les méthodologies de projet (ex: "ethics stories" dans les sprints agiles), et dans les critères d'évaluation professionnelle. Le défi est de rendre l'éthique "vivante" et consubstantielle à la pratique du codage des algorithmes de personnalisation.   

Le tableau suivant présente les principes clés proposés pour ce nouveau code de déontologie, en indiquant leurs principales inspirations et leur adaptation spécifique au domaine de la personnalisation.

Tableau 3 : Principes Clés pour un Code de Déontologie des Codeurs d'Algorithmes de Personnalisation

Principe Proposé pour le Nouveau Code	Inspiration Principale	Justification/Adaptation pour la Personnalisation	Implication Pratique pour le Codeur
1. Primauté du Bien-être et de l'Autonomie de l'Utilisateur	Déclaration de Montréal (Bien-être, Autonomie) ; ACM (1.1, 1.2) 	La personnalisation doit servir l'utilisateur, pas le manipuler ou nuire à son bien-être psychologique ou à sa capacité de choix.	Éviter les "dark patterns", concevoir pour le contrôle utilisateur, évaluer l'impact sur la santé mentale.
2. Responsabilité des Impacts Algorithmiques	Biosphere Code (P1) ; Déclaration de Montréal (Responsabilité) ; IEEE-CS/ACM (P1) 	Les codeurs sont co-responsables des effets de leurs algorithmes, même non intentionnels.	Participer aux AIA, monitorer les effets post-déploiement, documenter les risques.
3. Justice, Équité et Non-Discrimination Algorithmique	Biosphere Code (P3) ; Déclaration de Montréal (Équité, Inclusion) ; ACM (1.4) 	La personnalisation ne doit pas discriminer ni exacerber les inégalités existantes.	Utiliser FAML, auditer les biais, tester sur des groupes diversifiés, concevoir pour l'accessibilité.
4. Transparence et Explicabilité des Processus	Biosphere Code (P6) ; Déclaration de Montréal (Participation démocratique) ; UNESCO (T&E) 	Les utilisateurs doivent pouvoir comprendre les bases de la personnalisation à laquelle ils sont soumis.	Documenter la logique algorithmique, fournir des explications (XAI), être clair sur l'usage des données.
5. Protection Renforcée de la Vie Privée et des Données	Déclaration de Montréal (Intimité) ; ACM (1.6) ; GDPR	La personnalisation est gourmande en données ; une protection maximale est requise. "Privacy by Design/Default".	Minimisation des données, consentement éclairé, anonymisation/pseudonymisation, sécurité des données.
6. Intégrité Professionnelle, Compétence et Prudence	ACM (1.3, 2.1, 2.2, 2.6) ; IEEE-CS/ACM (P4, P8) ; Déclaration de Montréal (Prudence) 	Maintenir un haut niveau de savoir-faire technique et éthique, anticiper les risques.	Formation continue (technique et éthique), honnêteté sur les limites, conception robuste et sécurisée.
7. Conception Adaptative et Ouverte à la Correction	Biosphere Code (P4) 	Les algorithmes et leurs impacts évoluent ; la conception doit permettre des ajustements éthiques.	Modularité, maintenabilité, mécanismes de feedback, documentation des changements.
8. Collaboration Multidisciplinaire et Dialogue	Déclaration de Montréal (Participation démocratique) ; UNESCO (Gouvernance multipartite) 	Les défis éthiques de la personnalisation sont complexes et nécessitent des perspectives variées.	Travailler avec des éthiciens, designers UX, juristes, utilisateurs ; culture de débat éthique.
  
5.3. Limitations de l'Étude

Plusieurs limitations doivent être reconnues concernant cette étude.
Premièrement, l'analyse du Biosphere Code a été contrainte par l' inaccessibilité de certains documents de référence hébergés sur Google Drive. Par conséquent, l'interprétation de ce code et de son processus d'élaboration s'est fondée sur les informations publiquement disponibles, telles que l'article de blog fondateur  et les analyses critiques ou mentions dans d'autres sources. Bien que ces sources fournissent une bonne compréhension des principes, des nuances ou des détails sur son application pratique pourraient avoir été manqués.   

Deuxièmement, la formulation d'un nouveau code de déontologie pour les codeurs d'algorithmes de personnalisation revêt un caractère nécessairement exploratoire et normatif. Les principes et la structure proposés constituent une première esquisse qui nécessiterait une validation et un enrichissement par un processus délibératif impliquant les parties prenantes concernées (codeurs, entreprises, experts en éthique, représentants des utilisateurs).

Troisièmement, l'évaluation de l'applicabilité universelle et de l'efficacité des étapes de modification proposées pour les algorithmes prédateurs est limitée par l'absence de tests empiriques approfondis sur une grande variété d'algorithmes de personnalisation spécifiques en conditions réelles. L'efficacité des techniques XAI et FAML, par exemple, peut varier considérablement en fonction de la complexité de l'algorithme, de la nature des données et du contexte d'application.

Quatrièmement, la définition même de ce qui constitue une logique "prédatrice" peut comporter une part de subjectivité et varier selon les contextes culturels, les sensibilités individuelles et les cadres réglementaires. Ce qui est perçu comme une manipulation inacceptable par certains peut être considéré comme une technique marketing persuasive par d'autres. Bien que ce rapport s'efforce de s'appuyer sur des principes éthiques largement reconnus (comme ceux de la Déclaration de Montréal), la frontière reste parfois floue et sujette à débat.

Enfin, la portée de cette étude est principalement axée sur les dimensions éthiques et techniques. Les aspects purement économiques, juridiques (au-delà des grands principes de protection des données) ou sociologiques des algorithmes de personnalisation prédateurs, bien que connexes, n'ont été abordés que de manière périphérique. Une analyse plus approfondie de ces dimensions nécessiterait des recherches complémentaires.

Malgré ces limitations, cette étude vise à apporter une contribution significative à la réflexion sur l'encadrement éthique des algorithmes de personnalisation, en proposant des pistes concrètes pour l'action et la délibération.

6. Travaux Futurs et Perspectives
Les résultats présentés dans ce rapport ouvrent plusieurs pistes de recherche et de réflexion pour approfondir la compréhension et l'encadrement éthique des algorithmes de personnalisation. Ces perspectives s'articulent autour de l'opérationnalisation de l'éthique, des défis de son implémentation, du rôle des dynamiques de pouvoir et de la nécessité d'une approche co-évolutive de la régulation. L'objectif à long terme est de parvenir à une "IA digne de confiance" , où l'éthique n'est pas une contrainte externe, mais une propriété intrinsèque de systèmes conçus et gouvernés de manière responsable. Cette confiance se construit par des pratiques transparentes, responsables et équitables, impliquant une évolution des mentalités autant que des technologies.   

6.1. Opérationnalisation et Mesure de l'Éthique Algorithmique

Un défi majeur réside dans la traduction effective des principes éthiques de haut niveau en pratiques d'ingénierie logicielle concrètes, mesurables et intégrables dans les cycles de développement.

Développement de métriques fines : Si des métriques existent pour l'équité (FAML ), il est nécessaire de développer et de valider des indicateurs plus nuancés pour évaluer comment les algorithmes de personnalisation affectent des concepts comme le "bien-être", l'"autonomie" ou la "diversité informationnelle" des utilisateurs. Comment quantifier une "bulle de filtre" ou l'impact d'une interface sur le stress de l'utilisateur? Ces recherches pourraient s'inspirer des travaux en psychologie, en économie comportementale et en interaction homme-machine.   
Intégration des Évaluations d'Impact Éthique (EIE) : L'Évaluation de l'Impact Algorithmique (AIA)  est un outil prometteur. Des recherches futures devraient se concentrer sur son adaptation spécifique aux algorithmes de personnalisation et sur son intégration fluide dans les méthodologies de développement agiles, qui sont courantes dans l'industrie technologique. Comment réaliser une EIE pertinente sans ralentir excessivement les cycles d'innovation? Quels sont les seuils de risque qui déclenchent des examens plus approfondis?   
Outils d'aide à la conception éthique : Développer des outils (ex: bibliothèques de code, plugins pour IDE, plateformes de test) qui aident les codeurs à anticiper les risques éthiques, à implémenter des "garde-fous" (ex: limites de fréquence pour les notifications, mécanismes de diversification des recommandations) et à vérifier la conformité de leurs algorithmes avec les principes éthiques ou les exigences d'un code de déontologie.
6.2. Défis de l'Implémentation et Adoption des Codes de Déontologie

La simple existence d'un code de déontologie, aussi bien formulé soit-il, ne garantit pas son adoption ni son efficacité.

Surmonter les pressions organisationnelles et économiques : Les recherches montrent que les entreprises technologiques sont souvent soumises à des pressions intenses pour la performance à court terme, ce qui peut marginaliser les considérations éthiques. Comment créer des incitations (économiques, réputationnelles, réglementaires) pour que les entreprises soutiennent activement l'application des codes de déontologie par leurs employés?   
Rendre les codes "vivants" : Un code de déontologie ne doit pas être un document statique. Des travaux sont nécessaires pour explorer comment l'intégrer dans les pratiques quotidiennes des codeurs : formation continue, études de cas, mentorat éthique, inclusion de dilemmes éthiques dans les revues de code ou les rétrospectives de projet. Le rôle des "ethics entrepreneurs" ou des "champions de l'éthique" au sein des équipes  mérite d'être étudié plus avant comme mécanisme de diffusion et d'appropriation.   
Gestion de l'individualisation du risque : Souvent, la responsabilité éthique est individualisée sur les praticiens sans que les structures organisationnelles ne leur fournissent le soutien ou le pouvoir nécessaires pour agir. Comment les codes de déontologie peuvent-ils être articulés avec des mécanismes de responsabilité organisationnelle pour éviter que le codeur ne soit le seul fusible en cas de problème?   
6.3. Le Rôle des Dynamiques de Pouvoir et de la Culture Organisationnelle

Les décisions de conception algorithmique ne se prennent pas dans un vide social ou organisationnel.

Influence des structures et des incitations : Une analyse plus fine des dynamiques de pouvoir au sein des équipes de développement et des entreprises est nécessaire pour comprendre comment les décisions relatives à l'éthique des algorithmes de personnalisation sont réellement prises, négociées, ou parfois évitées. Quels sont les rôles respectifs des codeurs, des chefs de produit, des designers UX, du management et du marketing dans l'émergence ou la prévention des logiques prédatrices?   
Cultiver une culture d'éthique et de responsabilité : Au-delà des règles formelles, comment instiller une véritable culture de la responsabilité éthique? Cela passe par le leadership, la valorisation des compétences éthiques, la création d'espaces de discussion sécurisés pour aborder les dilemmes, et l'intégration de l'éthique dans les processus de recrutement et d'évaluation.
Soutenir la prise de parole ("Speaking Up") : Les mécanismes permettant aux employés de signaler des préoccupations éthiques ("whistleblowing" ou alerte éthique interne) sont cruciaux. Le "tech worker activism" , où des employés se mobilisent collectivement pour des pratiques plus éthiques, est un phénomène croissant dont il faut étudier les conditions d'émergence et l'impact. Comment les codes de déontologie peuvent-ils protéger et encourager ceux qui osent "parler vrai au pouvoir"?   
6.4. Vers une Régulation Co-évolutive

L'encadrement des algorithmes de personnalisation ne peut reposer uniquement sur l'autorégulation ou les codes de déontologie (relevant de la "soft law"). Une interaction dynamique avec la régulation étatique ("hard law") est indispensable.

Articulation entre "soft law" et "hard law" : Comment les codes de déontologie peuvent-ils informer et compléter la législation (ex: l'AI Act européen )? Peuvent-ils servir de base à des standards techniques ou à des certifications qui faciliteraient la démonstration de conformité à la loi?   
Rôle des organismes de standardisation et de certification : Des organismes indépendants pourraient jouer un rôle dans l'élaboration de standards pour l'éthique des algorithmes de personnalisation et dans la certification des systèmes ou des processus de développement, offrant ainsi des garanties aux utilisateurs et aux régulateurs.
Adaptabilité de la régulation : Face à l'évolution rapide des technologies, la régulation doit elle-même être adaptative et co-évolutive, capable d'anticiper les nouveaux risques sans étouffer l'innovation bénéfique. Des approches de "bac à sable réglementaire" (regulatory sandboxes) pourraient être explorées pour tester de nouvelles approches de personnalisation éthique.
En conclusion, les travaux futurs devront s'attacher à combler le fossé entre les principes éthiques et leur mise en œuvre effective dans le monde complexe et dynamique du développement des algorithmes de personnalisation. Cela nécessitera une collaboration étroite entre chercheurs de diverses disciplines, praticiens de l'industrie, décideurs politiques et la société civile.

7. Conclusion
L'ère de la personnalisation algorithmique, porteuse de promesses d'expériences utilisateur enrichies et de services sur mesure, est également traversée par des tensions éthiques fondamentales. L'émergence et la prolifération de logiques prédatrices, souvent matérialisées par des "dark patterns" insidieux, menacent l'autonomie, le bien-être et la confiance des individus dans l'écosystème numérique. Ce rapport a cherché à répondre à cette problématique en explorant deux voies complémentaires : la modification éthique des algorithmes existants et la formulation d'une déontologie pour ceux qui les conçoivent.

En s'appuyant sur les principes robustes de la Déclaration de Montréal pour un développement responsable de l'IA , nous avons esquissé une démarche en quatre phases pour réorienter les algorithmes de personnalisation prédateurs. Cette démarche, qui va du diagnostic éthique à la gouvernance continue, en passant par la redéfinition des objectifs et la modification technique, souligne que la lutte contre ces dérives ne peut être un simple ajustement cosmétique. Elle appelle à une refonte systémique, intégrant les impératifs de bien-être, d'autonomie, d'équité et de transparence au cœur même de la conception algorithmique. L'utilisation d'outils comme l'AIA , XAI  et FAML  s'avère cruciale pour opérationnaliser ces principes.   

Parallèlement, inspiré par la vision holistique du Biosphere Code  et en dialogue avec des codes de déontologie établis comme ceux de l'ACM  et de l'IEEE-CS/ACM , ce rapport a jeté les bases d'un code de déontologie spécifiquement destiné aux codeurs d'algorithmes de personnalisation. Les huit principes fondamentaux proposés – primauté du bien-être et de l'autonomie de l'utilisateur, responsabilité des impacts, justice et équité, transparence et explicabilité, protection de la vie privée, intégrité et prudence, conception adaptative, et collaboration – visent à équiper les professionnels d'une boussole éthique adaptée aux défis uniques de leur domaine. Ce code insiste sur une responsabilité proactive, considérant l'impact "écologique" de la personnalisation sur l'environnement informationnel et décisionnel de l'utilisateur.   

Il est toutefois crucial de reconnaître que ni les modifications techniques ni les codes de déontologie ne peuvent, à eux seuls, garantir une personnalisation algorithmique éthique. Comme l'analyse l'a montré, les pressions économiques, la culture organisationnelle et les dynamiques de pouvoir jouent un rôle déterminant. La lutte contre les logiques prédatrices et la promotion d'une déontologie forte sont donc des processus itératifs et adaptatifs, nécessitant une vigilance constante et un engagement de tous les instants.   

L'avenir de la personnalisation algorithmique dépendra de notre capacité collective – chercheurs, codeurs, entreprises, régulateurs et citoyens – à cultiver un écosystème où l'innovation technologique est indissociable d'une profonde responsabilité éthique. Il s'agit de s'assurer que la personnalisation, loin de devenir un instrument de manipulation sophistiquée, demeure un outil au service de l'épanouissement humain, de la découverte et du libre arbitre. Les travaux futurs devront continuer à explorer les moyens de traduire ces aspirations en pratiques concrètes, mesurables et durablement ancrées dans le tissu technologique et social.





@online{MontrealDeclaration_Full,
  title        = {La D{\'{e}}claration de Montr{\'{e}}al IA responsable},
  author       = {{Universit{\'{e}} de Montr{\'{e}}al}},
  year         = {2018},
  url          = {https://declarationmontreal-iaresponsable.com/la-declaration/},
  urldate      = {2024-05-15},
  note         = {Version int{\'{e}}grale. Consult{\'{e}} pour.[1]}
}

@online{MontrealDeclaration_About,
  title        = {About the Montr{\'{e}}al Declaration on Responsible AI},
  author       = {{Universit{\'{e}} de Montr{\'{e}}al}},
  year         = {2018},
  url          = {https://montrealdeclaration-responsibleai.com/about/},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[12]}
}

@online{MontrealDeclaration_Activities,
  title        = {D{\'{e}}claration de Montr{\'{e}}al IA responsable},
  author       = {{Universit{\'{e}} de Montr{\'{e}}al}},
  url          = {https://declarationmontreal-iaresponsable.com/},
  urldate      = {2024-05-15},
  note         = {Page d'accueil et informations g{\'{e}}n{\'{e}}rales. Consult{\'{e}} pour.[7]}
}

@online{BiosphereCode_DarkMachines,
  title        = {The Biosphere Code},
  author       = {{Dark Machines}},
  year         = {2019},
  url          = {https://darkmachines.earth/blog/the-biosphere-code},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[2, 15]}
}

@article{Watson_MaisOuVaLeWeb_2019,
  author       = {Watson, Sara M.},
  title        = {Technologies : sortir du biais d'optimisme et commencer {\`{a}} en {\'{e}}valuer les effets},
  journal      = {Mais o{\`{u}} va le Web?},
  year         = {2019},
  month        = {May},
  url          = {https://maisouvaleweb.fr/technologies-sortir-biais-doptimisme-commencer-a-evaluer-effets/},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[10]}
}

@online{Progressistes_Revue_2014,
  author       = {{Revue Progressistes}},
  title        = {LES COULISSES DE LA PROPRET{\'{E}} LE PROGR{\`{E}}S - La revue Progressistes},
  year         = {2014},
  url          = {https://revue-progressistes.org/wp-content/uploads/2014/08/progressistes-nc2b05-juillet-aout-sept1.pdf},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[3]}
}

@online{NoisenoiseMusic_ScryCaptcha_2025,
  author       = {{noisenotmusic}},
  title        = {Review: Scry, ‘CAPTCHA’ (self-released, Mar 10)},
  year         = {2025},
  month        = {April},
  url          = {https://noisenotmusic.com/2025/04/10/review-scry-captcha-self-released-mar-10/},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[4]}
}

@article{Brown_Thesis_DarkPatterns_2023,
  author       = {Brown, Edward},
  title        = {Harmful by Design: Examining the Detrimental Effects of Manipulative User Interface and User Experience Design Practices},
  year         = {2023},
  school       = {University of Mississippi},
  type         = {Honors Thesis},
  url          = {https://egrove.olemiss.edu/context/hon_thesis/article/4170/viewcontent/EDWARD_BROWN_THESIS.pdf},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[5]}
}

@online{DarkPatternsOrg_Types,
  title        = {Types of Deceptive Pattern},
  author       = {{DarkPatterns.org}},
  url          = {https://www.darkpatterns.org/types-of-dark-pattern},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[6]}
}

@online{DarkPatternsOrg_ReadingList,
  title        = {Deceptive Patterns - Reading list},
  author       = {{Deceptive.design}},
  url          = {https://www.deceptive.design/reading-list},
  urldate      = {2024-05-15},
  note         = {Anciennement darkpatterns.org. Consult{\'{e}} pour.[24]}
}

@online{DarkPatternsOrg_Home,
  title        = {Dark Patterns - User Interfaces Designed to Trick People},
  author       = {{DarkPatterns.org}},
  url          = {https://www.darkpatterns.org/},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[21]}
}

@article{Kortelainen_DarkPatternsEthics_2025,
  author       = {Kortelainen, Jomo},
  title        = {Dark Patterns and Ethics: an Underexplored Connection},
  year         = {2025},
  month        = {March},
  eprint       = {2503.01828},
  archiveprefix = {arXiv},
  primaryclass = {cs.HC},
  url          = {https://arxiv.org/html/2503.01828v1},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[22]}
}

@article{Ahmad_DarkPatternsImpact_2025,
  author       = {Ahmad, Abid and Anand, Anu and Paul, Justin and Reza, M. N. H.},
  title        = {The impact of dark patterns on user experience and decision-making: a review and research agenda},
  journal      = {Behaviour & Information Technology},
  year         = {2025},
  volume       = {Online ahead of print},
  pages        = {1--24},
  doi          = {10.1080/17517575.2025.2457961},
  url          = {https://www.tandfonline.com/doi/full/10.1080/17517575.2025.2457961?af=R},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[23]}
}

@online{Wikipedia_DeclarationMontreal,
  title        = {D{\'{e}}claration de Montr{\'{e}}al pour un d{\'{e}}veloppement responsable de l'intelligence artificielle},
  author       = {{Wikip{\'{e}}dia}},
  year         = {2025},
  month        = {January},
  url          = {https://fr.wikipedia.org/wiki/D%C3%A9claration_de_Montr%C3%A9al_pour_un_d%C3%A9veloppement_responsable_de_l%27intelligence_artificielle},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[13, 14]}
}

@online{UNESCO_EthicsAIRecommendation,
  title        = {Recommandation sur l'{\'{e}}thique de l'intelligence artificielle},
  author       = {{UNESCO}},
  url          = {https://www.unesco.org/fr/artificial-intelligence/recommendation-ethics},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[16]}
}

@article{Quantmetry_EquiteAlgorithmique_2021,
  author       = {{Quantmetry}},
  title        = {Intelligence Artificielle et {\'{E}}thique : comment d{\'{e}}finir et mesurer l'{\'{e}}quit{\'{e}} algorithmique?},
  journal      = {Quantmetry Blog},
  year         = {2021},
  month        = {May},
  url          = {https://www.quantmetry.com/blog/intelligence-artificielle-et-ethique-comment-definir-et-mesurer-lequite-algorithmique/},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[31]}
}

@online{ACM_CodeOfEthics_Full,
  title        = {ACM Code of Ethics and Professional Conduct},
  author       = {{Association for Computing Machinery (ACM)}},
  year         = {2018},
  month        = {June},
  url          = {https://www.acm.org/code-of-ethics},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[38]}
}

@online{ACM_SECodeOfEthics,
  title        = {Software Engineering Code of Ethics and Professional Practice},
  author       = {{ACM/IEEE-CS Joint Task Force on Software Engineering Ethics and Professional Practices}},
  year         = {1999},
  url          = {https://ethics.acm.org/code-of-ethics/software-engineering-code/},
  urldate      = {2024-05-15},
  note         = {Version 5.2. Consult{\'{e}} pour.[40]}
}

@online{Scribd_ACMCode,
  title        = {3 ACM Code of Ethics and Professional Conduct},
  year         = {N.d.},
  url          = {https://www.scribd.com/presentation/689037361/3-ACM-Code-of-Ethics-and-Professional-Conduct},
  urldate      = {2024-05-15},
  note         = {Présentation de slides. Consult{\'{e}} pour.[39]}
}

@online{Scribd_SECode,
  title        = {software-engineering-code-of-ethics-and-professional-practice_compress. pdf},
  year         = {N.d.},
  url          = {https://www.slideshare.net/slideshow/softwareengineeringcodeofethicsandprofessionalpracticecompresspdf/254355087},
  urldate      = {2024-05-15},
  note         = {Présentation de slides. Consult{\'{e}} pour.[42]}
}

@online{Scribd_Ethics171,
  title        = {1-7-1 Ethics},
  year         = {N.d.},
  url          = {https://www.scribd.com/document/678936889/1-7-1-ethics},
  urldate      = {2024-05-15},
  note         = {Document. Consult{\'{e}} pour.[43]}
}

@online{NOU_CIT831,
  title        = {CIT 831: Software Engineering II - Course Material},
  author       = {{National Open University of Nigeria}},
  year         = {N.d.},
  url          = {https://nou.edu.ng/coursewarecontent/CIT%20831_FINAL%20REVIEW.pdf},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[44, 45]}
}

@online{Gordana_SECodeEthicsPres,
  author       = {Dodig-Crnkovic, Gordana},
  title        = {Ethics and Professional Responsibility in Computing},
  year         = {2017},
  month        = {October},
  url          = {http://www.gordana.se/work/PRESENTATIONS-files/20171030-ETFOS-ETHICS-GDC.pdf},
  urldate      = {2024-05-15},
  note         = {Présentation. Consult{\'{e}} pour.[46]}
}

@thesis{Ly_Thesis_SE,
  author       = {Ly, Minh},
  title        = {Software Engineering},
  year         = {2017},
  school       = {HAAGA-HELIA University of Applied Sciences},
  type         = {Bachelor's Thesis},
  url          = {https://www.theseus.fi/bitstream/10024/150706/1/Minh_Ly.pdf},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[47]}
}

@online{LearnLearnUK_IEEECode,
  title        = {IEEE Software Engineering Code of Ethics},
  author       = {{Learn Learn UK}},
  url          = {https://learnlearn.uk/alevelcs/ieee-code-ethics/},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[48]}
}

@online{Slideshare_SECodeOfEthics,
  author       = {Various},
  title        = {Professional Code of Ethics in Software Engineering},
  year         = {N.d.},
  url          = {https://www.slideshare.net/slideshow/professional-code-of-ethics-in-software-engineering/12197665},
  urldate      = {2024-05-15},
  note         = {Agr{\'{e}}gat de pr{\'{e}}sentations. Consult{\'{e}} pour.[41]}
}

@online{Canada_AIA_Tool,
  title        = {Algorithmic Impact Assessment},
  author       = {{Treasury Board of Canada Secretariat}},
  year         = {2019},
  month        = {March},
  url          = {https://open.canada.ca/data/en/dataset/5423054a-093c-4239-85be-fa0b36ae0b2e},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[34, 36]}
}

@online{Canada_AIA_Guide,
  title        = {Algorithmic Impact Assessment},
  author       = {{Government of Canada}},
  url          = {https://www.canada.ca/en/government/system/digital-government/digital-government-innovations/responsible-use-ai/algorithmic-impact-assessment.html},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[35]}
}

@article{Wachter_Counterfactual_2018,
  author       = {Wachter, Sandra and Mittelstadt, Brent and Russell, Chris},
  title        = {Counterfactual Explanations Without Opening the Black Box: Automated Decisions and the GDPR},
  journal      = {Harvard Journal of Law \& Technology},
  year         = {2018},
  volume       = {31},
  number       = {2},
  pages        = {841--887},
  url          = {https://www.researchgate.net/publication/320796885_Counterfactual_Explanations_Without_Opening_the_Black_Box_Automated_Decisions_and_the_GDPR},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[37]}
}

@article{Ahmad_XAI_Bias_Hyperpersonalization_2025,
  author       = {Ahmad, Abid and Anand, Anu and Paul, Justin and Reza, M. N. H.},
  title        = {The Role of Explainable AI in Bias Mitigation for Hyper-personalization},
  journal      = {ResearchGate (Preprint)},
  year         = {2025},
  month        = {January},
  doi          = {10.13140/RG.2.2.27654.55367},
  url          = {https://www.researchgate.net/publication/387092348_The_Role_of_Explainable_AI_in_Bias_Mitigation_for_Hyper-personalization},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[25]}
}

@article{Marconi_XRS_Review_2023,
  author       = {Marconi, Mirko},
  title        = {Discovering the Unknown Suggestion: a Short Review on Explainability for Recommender Systems},
  journal      = {CEUR Workshop Proceedings},
  year         = {2023},
  volume       = {3627},
  pages        = {1--10},
  url          = {https://boa.unimib.it/bitstream/10281/466854/1/Marconi-2023-CEUR-VoR.pdf},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[26]}
}

@article{Pessach_XAI_Evaluation_2023,
  author       = {Pessach, Dana and Shmueli, Erez},
  title        = {A Review on Explainable AI: From Theory to Practice},
  journal      = {Information Fusion},
  year         = {2023},
  volume       = {99},
  pages        = {101871},
  doi          = {10.1016/j.inffus.2023.101871},
  note         = {Cited in [27] context, not directly browsed but relevant to XAI survey.}
}

@article{Zhao_EthicalRS_XAI_2024,
  author       = {Zhao, Shunan and Elahi, Mehdi and An, Jisun and Kwak, Haewoon and Schedl, Markus},
  title        = {Research Agenda of Ethical Recommender Systems based on Explainable AI},
  journal      = {ResearchGate (Preprint)},
  year         = {2024},
  month        = {July},
  url          = {https://www.researchgate.net/publication/382096169_Research_Agenda_of_Ethical_Recommender_Systems_based_on_Explainable_AI},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[27]}
}

@article{Feng_UserAttitudesAI_2025,
  author       = {Feng, Y. and Kou, Y. and Gui, X. and Chen, Y. and Wang, D.},
  title        = {Understanding User Attitudes and Concerns Towards AI in Social Media Algorithms},
  year         = {2025},
  month        = {March},
  eprint       = {2503.03927},
  archiveprefix = {arXiv},
  primaryclass = {cs.HC},
  url          = {https://arxiv.org/pdf/2503.03927},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[58]}
}

@article{Ahmad_ML_BigData_2025,
  author       = {Ahmad, Abid and Anand, Anu and Paul, Justin and Reza, M. N. H.},
  title        = {Exploring the Intersection of Machine Learning and Big Data: A Survey},
  journal      = {ResearchGate (Preprint)},
  year         = {2025},
  month        = {February},
  doi          = {10.13140/RG.2.2.30170.72643},
  url          = {https://www.researchgate.net/publication/388798847_Exploring_the_Intersection_of_Machine_Learning_and_Big_Data_A_Survey},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[28]}
}

@article{Ahmad_ML_BigData_MDPI_2025,
  author       = {Ahmad, Abid and Anand, Anu and Paul, Justin and Reza, M. N. H.},
  title        = {Machine Learning in Big Data: Challenges, Applications, and Future Directions},
  journal      = {Journal of Big Data and Cognitive Computing},
  year         = {2025},
  volume       = {7},
  number       = {1},
  pages        = {13},
  doi          = {10.3390/bdcc7010013},
  url          = {https://www.mdpi.com/2504-4990/7/1/13},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[29]}
}

@online{RapidInnovation_AIScalableAgents_2024,
  author       = {{Rapid Innovation}},
  title        = {For Developers: Best Practices in Designing Scalable AI Agent Architecture},
  year         = {2024},
  url          = {https://www.rapidinnovation.io/post/for-developers-best-practices-in-designing-scalable-ai-agent-architecture},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[30]}
}

@article{Fang_FairnessSearch_2022,
  author       = {Fang, Yun and Liu, Xuanhui and Yang, Liu and Barria-Pineda, Jael and Croft, W. Bruce and Zamani, Hamed},
  title        = {Fairness in Search and Recommendation},
  journal      = {Foundations and Trends{\textregistered} in Information Retrieval},
  year         = {2022},
  volume       = {16},
  number       = {3-4},
  pages        = {200--410},
  doi          = {10.1561/1500000089},
  url          = {https://www.cse.scu.edu/~yfang/Fairness_Search_FnTIR.pdf},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[32]}
}

@article{Dong_FairnessGraphLearning_2022,
  author       = {Dong, Yushun and Liu, Yu and Wang, Nianfel and Yu, Jundong and Ding, Jiejun and Li, Hui and He, Xiangnan},
  title        = {Fairness in Graph Machine Learning: A Survey},
  year         = {2022},
  month        = {May},
  eprint       = {2205.05396},
  archiveprefix = {arXiv},
  primaryclass = {cs.LG},
  url          = {https://arxiv.org/html/2205.05396v2},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[33]}
}

@online{Eval_PrincipesDirecteurs_2015,
  title        = {Principes directeurs et cadre d{\'{e}}ontologique},
  author       = {Galea, S{\'{e}}bastien},
  year         = {2015},
  url          = {https://www.eval.fr/quest-ce-que-levaluation/principes-directeurs-et-cadre-deontologique/},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[49]}
}

@online{OAGCanada_Deontologie_2021,
  title        = {1031 R{\`e}gles de d{\'{e}}ontologie r{\'{e}}gissant une mission de certification},
  author       = {{Bureau du v{\'{e}}rificateur g{\'{e}}n{\'{e}}ral du Canada (OAG-BVG)}},
  year         = {2021},
  month        = {June},
  url          = {https://www.oag-bvg.gc.ca/internet/methodologie/audit-de-performance/manuel/1031.shtm},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[59]}
}

@article{Rakova_WalkingAIEthics_2023,
  author       = {Rakova, Bogdana and Yang, Jingying and Kapania, Sonia and Reinecke, Katharina},
  title        = {Walking the Walk of AI Ethics: Organizational Challenges and the Individualization of Risk among Ethics Entrepreneurs},
  journal      = {Proceedings of the ACM on Human-Computer Interaction},
  year         = {2023},
  volume       = {7},
  number       = {CSCW1},
  pages        = {Article 99, 1--30},
  doi          = {10.1145/3579504},
  url          = {https://www.researchgate.net/publication/371517465_Walking_the_Walk_of_AI_Ethics_Organizational_Challenges_and_the_Individualization_of_Risk_among_Ethics_Entrepreneurs},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[11]}
}

@online{USG_DataEthicsFramework,
  title        = {Federal Data Strategy: Data Ethics Framework},
  author       = {{U.S. Government}},
  year         = {2020},
  url          = {https://resources.data.gov/assets/documents/fds-data-ethics-framework.pdf},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[19]}
}

@online{ManagementConcepts_DataEthicsCourse,
  title        = {Federal Data Ethics Framework (Course 4611)},
  author       = {{Management Concepts}},
  url          = {https://www.managementconcepts.com/course/id/4611/},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[20]}
}

@online{IrishGov_AIGuidelines,
  title        = {Guidelines for the Responsible Use of Artificial Intelligence in the Public Service},
  author       = {{Government of Ireland - AI Advisory Council}},
  year         = {2024},
  url          = {https://iamaeg.net/files/CF0E1575-C621-4F8B-9CA4-B669741568C8.pdf},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[17]}
}

@online{EU_AICodePractice,
  title        = {Code de bonnes pratiques en mati{\`e}re d'IA {\`a} usage g{\'{e}}n{\'{e}}ral},
  author       = {{Commission Europ{\'{e}}enne}},
  year         = {2025},
  month        = {April},
  url          = {https://digital-strategy.ec.europa.eu/fr/policies/ai-code-practice},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[60]}
}

@online{EcoleBranchee_AICodeEcole,
  title        = {Un mod{\`e}le de base pour cr{\'{e}}er un code d'{\'{e}}thique sur l'usage de l'IA {\`a} l'{\'{e}}cole},
  author       = {{L'{\'{E}}cole branch{\'{e}}e}},
  year         = {2025},
  month        = {May},
  url          = {https://ecolebranchee.com/modele-base-creer-code-ethique-usage-ia-ecole/},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[61]}
}

@online{IRBAI_AILegislation,
  title        = {AI Compliance & Legislation},
  author       = {{Institute for Responsible BPM and AI (IRBAI)}},
  url          = {https://irbai.org/compliance-legislation/},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[18]}
}

@article{Schlossberger_EthicalEngineering_2023,
  author       = {Schlossberger, Eugene},
  title        = {Ethical Engineering: A Practical Guide with Case Studies},
  publisher    = {CRC Press},
  year         = {2023},
  note         = {Information from publisher and PhilPeople. Consult{\'{e}} pour.[62, 63]}
}

@online{DokumenPub_EthicalEngineering,
  title        = {Ethical Engineering: A Practical Guide with Case Studies},
  author       = {Schlossberger, Eugene},
  year         = {2023},
  url          = {https://dokumen.pub/ethical-engineering-a-practical-guide-with-case-studies-1032151129-9781032151120.html},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[54]}
}

@article{Charitsis_AlgorithmicLuddism_2024,
  author       = {Charitsis, Vasileios and Van den Eede, Yoni and Molder, Hedwig},
  title        = {Towards Algorithmic Luddism: class politics in data capitalism},
  journal      = {Information, Communication \& Society},
  year         = {2024},
  volume       = {Online ahead of print},
  pages        = {1--18},
  doi          = {10.1080/1369118X.2024.2350904},
  url          = {https://www.researchgate.net/publication/386473380_Towards_Algorithmic_Luddism_class_politics_in_data_capitalism},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[57]}
}

@article{Ahmad_DigitalizationImplications_2025,
  author       = {Ahmad, Abid and Anand, Anu and Paul, Justin and Reza, M. N. H.},
  title        = {Environmental, Legal, and Governance Implications of Digitalization: Software Engineering, Sustainability, and Accountability},
  journal      = {European Scientific Journal, ESJ},
  year         = {2025},
  volume       = {20},
  number       = {15},
  pages        = {105},
  doi          = {10.19044/esj.2024.v20n15p105},
  url          = {https://eujournal.org/index.php/esj/article/view/19303},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[56]}
}

@online{MTU_EthicalSoftwareDesign_2019,
  author       = {Sullivan, Kelly},
  title        = {A Critical Review of Current Approaches and Practices in Computing Ethics Education and a Proposal for an Ethically Sensitive Software Design Intervention},
  year         = {2019},
  school       = {Michigan Technological University},
  type         = {PhD Dissertation},
  url          = {https://www.mtu.edu/cs/graduate/dissertations/pdfs/a-critical-review-of-current-approaches-and-practices-in-computing.pdf},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[55]}
}

@online{ISJPS_AxeDonneesIA,
  title        = {Axe donn{\'{e}}es et intelligence artificielle},
  author       = {{Institut des Sciences Juridique et Philosophique de la Sorbonne (ISJPS)}},
  url          = {https://isjps.pantheonsorbonne.fr/axes-recherche/axe-donnees-et-intelligence-artificielle},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[64]}
}

@online{ChildEthics_ERIC,
  title        = {RECHERCHE {\'{E}}THIQUE IMPLIQUANT DES ENFANTS},
  author       = {{Ethical Research Involving Children (ERIC)}},
  year         = {2022},
  url          = {https://childethics.com/wp-content/uploads/2022/04/ERIC-compendium-FR_LR.pdf},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[65]}
}

@article{COE_IRIS_DSA_2023,
  author       = {{Conseil de l'Europe}},
  title        = {IRIS Sp{\'{e}}cial 2023-2: La l{\'{e}}gislation sur les services num{\'{e}}riques (DSA) et le r{\^{e}}glement sur les march{\'{e}}s num{\'{e}}riques (DMA)},
  year         = {2023},
  url          = {https://rm.coe.int/iris-special-2023-02fr/1680aeda49},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[9]}
}

@article{Chen_YumMe_2018,
  author       = {Chen, Yu and Li, Lirong and Ganesan, D. and Thaker, K.},
  title        = {Yum-Me: A Personalized Nutrient-Based Meal Recommender System},
  journal      = {Proceedings of the ACM on Interactive, Mobile, Wearable and Ubiquitous Technologies},
  year         = {2018},
  volume       = {2},
  number       = {4},
  pages        = {1--26},
  doi          = {10.1145/3287061},
  url          = {https://pmc.ncbi.nlm.nih.gov/articles/PMC6242282/},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[66]}
}

@online{CCNUnistra_AmbitionNumerique,
  author       = {{Conseil national du num{\'{e}}rique (CNNum)}},
  title        = {Ambition num{\'{e}}rique : pour une politique fran{\c{c}}aise et europ{\'{e}}enne de la transition num{\'{e}}rique},
  year         = {2015},
  url          = {https://ccn.unistra.fr/websites/ccn/documentation/Administration-Fonctionpublique/CNNum--rapport-ambition-numerique.pdf},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[67]}
}

@article{Haupt_PersonalizationPrivacy_2025,
  author       = {Haupt, Felix and Haupt, Freya},
  title        = {Personalization Algorithms: Design, Economic Consequences, and Privacy},
  year         = {2025},
  school       = {Massachusetts Institute of Technology},
  type         = {PhD dissertation},
  url          = {https://dspace.mit.edu/bitstream/handle/1721.1/159105/haupt-haupt-phd-idss-2025.pdf?sequence=-1&isAllowed=y},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[68]}
}

@online{FasterCapital_BehavioralTargetingEthics,
  title        = {Ethical considerations in behavioral targeting},
  author       = {{FasterCapital}},
  url          = {https://fastercapital.com/topics/ethical-considerations-in-behavioral-targeting.html},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[69]}
}

@article{Abinesh_AIAdvertising_2024,
  author       = {Abinesh, T. K. and Dulloo, P.},
  title        = {AI-Powered Advertising: A Comprehensive Analysis of Targeting, Personalization, Content Creation, and Ad Optimization},
  journal      = {IGI Global (Book Chapter Preview)},
  year         = {2024},
  url          = {https://www.igi-global.com/viewtitle.aspx?TitleId=376253&isxn=9798369395615},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[70]}
}

@online{SmartDev_AIEthicsGuide,
  title        = {AI Ethics Concerns: A Business-Oriented Guide to Responsible AI},
  author       = {{SmartDev}},
  url          = {https://smartdev.com/ai-ethics-concerns-a-business-oriented-guide-to-responsible-ai/},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[71]}
}

@article{Alikhademi_VulnerabilityCyber_2025,
  author       = {Alikhademi, Kian and others},
  title        = {AI-enhanced cybersecurity: Vulnerability-based prevention, defense, and mitigation using generative AI},
  journal      = {Orclever Proceedings of Research and Development},
  year         = {2025},
  volume       = {5},
  number       = {1},
  url          = {https://www.researchgate.net/publication/388789724_AI-Enhanced_Cybersecurity_Vulnerability-Based_Prevention_Defense_and_Mitigation_using_Generative_AI},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[72]}
}

@article{Ahmad_AITrustZeroDay_2025,
  author       = {Ahmad, Abid and Anand, Anu and Paul, Justin and Reza, M. N. H.},
  title        = {Advancing Ai Trust And Transparency In Zero-Day Vulnerability Mitigation},
  journal      = {ResearchGate (Preprint)},
  year         = {2025},
  month        = {June},
  doi          = {10.13140/RG.2.2.26928.33280},
  url          = {https://www.researchgate.net/publication/391731900_Advancing_Ai_Trust_And_Transparency_In_Zero-Day_Vulnerability_Mitigation},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[73]}
}

@online{Diploweb_LivresGeopolitiques_2025,
  title        = {Actualit{\'{e}} des livres g{\'{e}}opolitiques},
  author       = {{Diploweb.com}},
  year         = {2025},
  month        = {February},
  url          = {https://www.diploweb.com/Actualite-des-livres-geopolitiques-720.html},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[74]}
}

@article{Kapania_MontrealDeclarationCritique_2023,
  author       = {Kapania, Sonia and Rakova, Bogdana and Yang, Jingying and Reinecke, Katharina},
  title        = {From Principles to Practice: A Multidimensional Analysis of the Montreal Declaration for Responsible AI},
  journal      = {ACM SIGCAS/SIGCHI Conference on Computing and Sustainable Societies (COMPASS)},
  year         = {2023},
  url          = {https://osf.io/sj2z5/download/},
  urldate      = {2024-05-15},
  note         = {Consult{\'{e}} pour.[8]}
}