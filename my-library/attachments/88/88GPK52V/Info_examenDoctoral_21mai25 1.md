Rapport d'Expertise en Apprentissage Automatique : Interprétabilité, Systèmes de Recommandation, et Comparaison BMA-Bagging

Introduction

L'apprentissage automatique (AA) est en train de remodeler fondamentalement de nombreux secteurs d'activité et domaines de recherche. Des systèmes de diagnostic médical aux moteurs de recherche en passant par les véhicules autonomes, sa capacité à extraire des connaissances et à effectuer des prédictions à partir de données massives offre des possibilités sans précédent. Cependant, cette puissance s'accompagne d'une complexité croissante des modèles. Des architectures sophistiquées, telles que les réseaux de neurones profonds, fonctionnent souvent comme des "boîtes noires", où les mécanismes internes conduisant à une décision spécifique sont opaques, même pour leurs concepteurs. Cette opacité soulève des questions fondamentales et urgentes concernant la confiance que nous pouvons accorder à ces systèmes, la transparence de leurs opérations et la responsabilité en cas d'erreur ou de comportement indésirable.   

Face à ces défis, le concept d'interprétabilité des modèles d'apprentissage automatique (abordé dans la Question 1 de cette étude) a émergé comme un champ de recherche crucial. Il ne s'agit plus seulement d'obtenir des prédictions précises, mais de comprendre comment et pourquoi ces prédictions sont faites. Cette compréhension est particulièrement vitale dans les domaines dits sensibles – tels que la santé, la finance ou la justice – où les décisions algorithmiques peuvent avoir des conséquences directes et significatives sur la vie des individus. L'interprétabilité est donc essentielle pour valider la robustesse des modèles, déboguer leurs erreurs, s'assurer de leur équité et, in fine, pour permettre une adoption responsable et éthique de l'IA.   

Parallèlement, les systèmes de recommandation (Question 2) sont devenus une composante omniprésente de notre expérience numérique quotidienne. Qu'il s'agisse de suggérer des produits sur des plateformes de commerce électronique, des films sur des services de streaming, ou des articles d'actualité, ces systèmes filtrent et personnalisent l'information à grande échelle. Comprendre les diverses techniques qui sous-tendent ces recommandations – du filtrage collaboratif traditionnel aux approches plus modernes basées sur l'apprentissage profond – est indispensable pour évaluer leur efficacité, leur pertinence, mais aussi les biais potentiels qu'ils pourraient introduire ou amplifier.   

Enfin, dans la quête constante d'amélioration des performances et de la robustesse des modèles d'AA, les méthodes d'ensemble, qui combinent plusieurs modèles pour obtenir une prédiction finale, jouent un rôle de premier plan. Le Bayesian Model Averaging (BMA) et le Bagging (Question 3) sont deux approches d'ensemble populaires, mais qui reposent sur des fondements théoriques et des philosophies distincts. Une analyse comparative approfondie de ces méthodes est nécessaire pour discerner leurs forces, leurs faiblesses, et les contextes dans lesquels l'une pourrait être préférée à l'autre.   

Ce rapport vise à fournir une analyse de niveau doctoral sur ces trois thématiques interdépendantes. Premièrement, il explorera en profondeur la notion d'interprétabilité en apprentissage automatique, en définissant ses concepts clés, en soulignant ses enjeux pratiques et éthiques, en analysant les principales méthodes développées pour rendre les modèles plus transparents, et en examinant les approches pour évaluer la qualité de ces interprétations. Deuxièmement, il présentera une explication détaillée de ce que sont les systèmes de recommandation, passera en revue les grandes familles de techniques existantes, et se concentrera sur une comparaison approfondie de deux méthodes spécifiques. Troisièmement, il mènera une analyse comparative rigoureuse du Bayesian Model Averaging et du Bagging, en scrutant leurs bases théoriques, leurs principes de fonctionnement et leurs implications pratiques. L'objectif global est de synthétiser les connaissances actuelles, d'identifier les liens entre ces domaines et de fournir une perspective éclairée sur des aspects essentiels de l'apprentissage automatique contemporain.

Partie 1 : Interprétabilité des Modèles d'Apprentissage Automatique

L'ascension fulgurante des modèles d'apprentissage automatique, en particulier des techniques d'apprentissage profond, a conduit à des avancées spectaculaires dans de nombreux domaines. Cependant, la complexité inhérente à ces modèles, souvent qualifiés de "boîtes noires", pose des défis significatifs en termes de compréhension et de confiance. L'interprétabilité et l'explicabilité émergent donc comme des préoccupations centrales, visant à rendre les décisions algorithmiques plus transparentes, compréhensibles et fiables pour les utilisateurs humains.

1.1. Définitions et Concepts Fondamentaux de l'Interprétabilité

La terminologie dans le domaine de l'interprétabilité n'est pas encore totalement standardisée, et les termes "interprétabilité" et "explicabilité" sont parfois utilisés de manière interchangeable. Néanmoins, une distinction conceptuelle est souvent opérée.

L'interprétabilité est fréquemment définie comme la capacité à expliquer ou à fournir un sens aux humains en termes compréhensibles concernant le fonctionnement d'un modèle ou la manière dont il parvient à une décision spécifique. Elle peut être considérée comme une caractéristique intrinsèque de certains modèles (par exemple, un arbre de décision simple dont la logique est directement lisible) ou comme le résultat d'une méthode appliquée a posteriori à un modèle complexe pour en sonder le comportement. Selon Lipton (2018), l'interprétabilité fait référence à la capacité de décrire ce qu'un modèle a appris, tandis que l'explication est un concept post-hoc qui fournit des informations sur le fonctionnement d'un modèle.   

L'explicabilité, souvent incarnée par le terme XAI (Explainable Artificial Intelligence), représente un concept plus large. Elle vise à développer des modèles ou des systèmes capables de produire des détails ou des raisons qui rendent leur fonctionnement clair ou facile à comprendre pour un public cible donné. L'interprétabilité est ainsi un moyen crucial pour atteindre l'explicabilité. Doran, Schulz et Besold (2017) soulignent que le dictionnaire Oxford définit une "explication" comme "une déclaration ou un compte-rendu qui clarifie quelque chose ; une raison ou une justification donnée pour une action ou une croyance". Ils interrogent alors la mesure dans laquelle les systèmes XAI actuels fournissent réellement de telles explications, suggérant une tension entre les capacités affichées des systèmes et la nature profonde d'une explication satisfaisante.   

Cette nuance terminologique reflète une ambition croissante : il ne s'agit plus seulement de permettre une inspection passive du modèle, mais de développer des systèmes capables de communiquer activement et intelligemment leur logique interne.

Pour mieux cerner ces notions, Doran et al.  proposent une conceptualisation des perspectives sur l'IA explicable, distinguant plusieurs types de systèmes :   

Systèmes opaques (Opaque systems) : Ce sont des systèmes où les mécanismes qui transforment les entrées en sorties sont complètement invisibles pour l'utilisateur. Ils fonctionnent comme des oracles, fournissant des prédictions sans aucune indication sur le "comment" ou le "pourquoi" de ces prédictions. Toute approche authentiquement "boîte noire", où l'inspection de l'algorithme ou de son implémentation ne fournit aucun aperçu du raisonnement réel du système, est classée ici.   
Systèmes interprétables (Interpretable systems) : Dans ce cas, l'utilisateur a la capacité d'analyser mathématiquement les mécanismes algorithmiques du système. Cela suppose une certaine forme de transparence au niveau du modèle lui-même, permettant une compréhension de son fonctionnement interne. Par exemple, les coefficients d'une régression linéaire ou la structure d'un arbre de décision peuvent être examinés directement.   
Systèmes compréhensibles (Comprehensible systems) : Ces systèmes émettent des symboles (par exemple, des caractéristiques importantes, des exemples similaires, des règles extraites) qui permettent à l'utilisateur de comprendre, par son propre effort d'analyse, comment une entrée spécifique a été mappée à une sortie correspondante. La compréhensibilité est donc une notion graduelle : le degré de compréhensibilité d'un système correspond à la facilité ou à la difficulté relative avec laquelle l'utilisateur peut compiler et comprendre ces symboles émis. L'utilisateur reste responsable de l'assemblage et de la compréhension de ces éléments.   
Systèmes véritablement explicables (Truly explainable systems) : Cette notion, introduite par Doran et al. , représente une avancée conceptuelle. Ici, le raisonnement automatisé est au cœur du processus : le système lui-même est capable de générer des explications élaborées et intelligibles par l'humain, sans nécessiter une post-analyse ou un assemblage manuel par l'utilisateur. Ces systèmes, bien qu'encore à un stade de développement naissant, promettent une interaction où l'IA peut justifier ses actions de manière autonome.   
Cette taxonomie met en lumière une évolution significative dans les attentes vis-à-vis de l'IA. On passe d'une simple demande de visibilité des mécanismes internes (systèmes interprétables) à un besoin d'explications actives, contextualisées et générées par le système lui-même (systèmes véritablement explicables). Cette progression reflète une ambition croissante pour des systèmes d'IA qui ne sont pas seulement transparents dans leur construction, mais aussi capables de communiquer et de justifier leur comportement de manière proactive. Cela a des implications profondes non seulement sur la conception des modèles algorithmiques mais aussi sur la nature des interfaces homme-machine et sur la collaboration entre humains et IA.

1.2. Enjeux Pratiques et Éthiques Rendannt l'Interprétabilité Cruciale

L'exigence d'interprétabilité pour les modèles d'apprentissage automatique n'est pas une simple quête académique ; elle répond à des impératifs pratiques et éthiques pressants, particulièrement lorsque ces systèmes sont déployés dans des domaines sensibles où leurs décisions ont des conséquences directes et parfois graves sur la vie des individus.

Importance dans les domaines sensibles :
L'application de l'AA dans des secteurs critiques tels que la santé, la finance, et la justice pénale a mis en évidence la nécessité impérieuse de comprendre les décisions algorithmiques.

En santé, les systèmes d'IA sont de plus en plus utilisés pour le diagnostic de maladies, la proposition de plans de traitement, ou l'analyse d'imagerie médicale. Une décision erronée ou mal comprise peut avoir des conséquences vitales. Les cliniciens doivent pouvoir comprendre et valider la logique d'une recommandation algorithmique, notamment pour s'assurer qu'elle est conforme aux protocoles cliniques et aux meilleures pratiques.   
Dans le secteur financier, l'AA est employée pour l'octroi de crédits, la détection de fraudes, ou la tarification d'assurances. Le refus d'un prêt basé sur un algorithme opaque peut sembler arbitraire et injuste, et potentiellement être discriminatoire.   
En justice pénale, des algorithmes sont utilisés pour l'évaluation des risques de récidive ou comme aide à la décision pour les juges. L'opacité de ces outils soulève des préoccupations majeures quant à l'équité et aux droits fondamentaux des individus.   
D'autres domaines incluent les décisions relatives aux politiques d'assurance, à la publicité ciblée, aux processus de recrutement, ou aux admissions universitaires.   
Dans chacun de ces contextes, les décisions prises par les algorithmes ne sont pas de simples suggestions ; elles façonnent des opportunités, déterminent l'accès à des services essentiels, et peuvent même affecter la liberté individuelle. L'opacité d'un modèle dans de telles situations est non seulement insatisfaisante mais potentiellement dangereuse et socialement inacceptable. L'enjeu est de s'assurer que ces puissants outils sont utilisés de manière responsable et juste.

Confiance et Transparence :
L'un des principaux moteurs de la recherche en XAI est la nécessité de bâtir la confiance dans les systèmes d'IA. Les modèles "boîtes noires", par leur nature même, engendrent la méfiance et le scepticisme, car les utilisateurs ne peuvent pas comprendre comment une décision a été atteinte. Des explications claires et détaillées sur le raisonnement d'un système sont perçues comme indispensables pour atteindre une confiance totale, permettant ainsi d'évaluer si les standards éthiques et moraux de la machine sont respectés. La transparence, facilitée par l'interprétabilité, est donc une condition préalable à l'acceptation et à l'adoption généralisée de l'IA dans des applications critiques.   

Responsabilité (Accountability) :
L'interprétabilité est intrinsèquement liée à la notion de responsabilité. Si un système prend une décision erronée ou préjudiciable, il est essentiel de pouvoir déterminer pourquoi cette décision a été prise et qui en est responsable. Les explications fournies par les méthodes d'interprétabilité permettent aux analystes, aux auditeurs, ou aux régulateurs d'évaluer si une décision a été atteinte par des arguments rationnels et si elle n'incorpore pas des étapes de raisonnement qui entrent en conflit avec des normes éthiques ou légales. La demande pour que la prise de décision automatisée soit transparente, responsable et compréhensible est croissante. Le principe d'"Accountability" est d'ailleurs l'un des sept principes fondamentaux énoncés par l'Association for Computing Machinery (ACM) pour la transparence et la responsabilité algorithmiques, stipulant que les institutions doivent être tenues responsables des décisions prises par les algorithmes qu'elles utilisent, même s'il n'est pas toujours possible d'expliquer en détail comment ces algorithmes produisent leurs résultats.   

Équité et Détection de Biais :
Les modèles d'apprentissage automatique sont entraînés sur des données qui peuvent refléter et même amplifier les biais sociétaux existants. Un modèle opaque peut perpétuer ou introduire des discriminations sans que cela soit apparent. L'interprétabilité offre des outils pour sonder les modèles et détecter si leurs décisions sont basées sur des variables sensibles (comme le genre, l'origine ethnique) de manière inappropriée ou si des biais systémiques influencent leurs prédictions. Le principe d'"Awareness" de l'ACM souligne que les concepteurs et utilisateurs de systèmes analytiques doivent être conscients des biais potentiels et des préjudices qu'ils peuvent causer. De plus, le principe de "Validation and Testing" insiste sur la nécessité de tester rigoureusement les modèles pour déterminer s'ils génèrent des préjudices discriminatoires. L'incapacité à expliquer le fonctionnement d'un algorithme peut effectivement masquer ou renforcer des pratiques discriminatoires , rendant l'interprétabilité indispensable pour promouvoir l'équité.   

Ces différents enjeux – confiance, responsabilité, et équité – ne sont pas isolés mais profondément interconnectés. Il est difficile de faire confiance à un système dont on ne comprend pas le fonctionnement, impossible de tenir une entité responsable pour les décisions d'un système opaque, et ardu de garantir l'équité d'un modèle sans pouvoir inspecter sa logique décisionnelle. L'interprétabilité se présente ainsi comme le socle commun permettant d'aborder ces défis de manière cohérente. Par exemple, pour qu'un individu fasse confiance à une décision de prêt algorithmique , il doit être assuré que le système est équitable (ne le discrimine pas sur des bases illégitimes) et que l'institution financière est responsable de cette décision. L'interprétabilité fournit les moyens de vérifier cette équité et d'établir cette responsabilité, conduisant in fine à une confiance éclairée.   

Considérations Réglementaires :
La prise de conscience de ces enjeux a conduit à une pression réglementaire croissante.

Le Règlement Général sur la Protection des Données (RGPD) de l'Union Européenne, en vigueur depuis 2018, a introduit des dispositions concernant la prise de décision automatisée, y compris le profilage. Bien que l'existence d'un "droit à l'explication" direct soit débattue par les juristes, les articles 13, 14 et 15 du RGPD exigent que les responsables de traitement fournissent aux personnes concernées des "informations utiles concernant la logique sous-jacente, ainsi que l'importance et les conséquences prévues de ce traitement". Cette exigence pousse à une plus grande transparence.   
Plus récemment, l'AI Act de l'Union Européenne (dont des versions sont en discussion) propose une approche basée sur les risques, imposant des exigences strictes pour les systèmes d'IA considérés à "haut risque". Parmi ces exigences figurent la transparence et l'interprétabilité. L'article 13 de certaines propositions de l'AI Act stipule que les systèmes d'IA à haut risque doivent être conçus et développés de manière à assurer que leur fonctionnement soit suffisamment transparent pour permettre aux utilisateurs d'interpréter le résultat du système et de l'utiliser de manière appropriée.   
Des standards techniques commencent également à émerger. Par exemple, la norme IEEE P7001 sur la transparence des systèmes autonomes considère l'explicabilité comme une composante de la transparence et définit des niveaux d'exigences, comme la capacité du système à répondre à des questions de type "pourquoi?" (explication locale) ou "que se passerait-il si?" (analyse contrefactuelle).   
Cette vague réglementaire agit comme un puissant catalyseur pour la recherche et l'adoption de l'XAI. La conformité n'est plus seulement une question de bonnes pratiques ou d'éthique, mais devient une obligation légale dans de nombreux contextes d'application de l'IA. Cela contraint les entreprises et les institutions à intégrer l'interprétabilité dès la phase de conception des systèmes, avec des implications économiques, techniques et organisationnelles majeures. L'enjeu n'est plus seulement de développer des modèles performants, mais des modèles performants et explicables.

1.3. Analyse Détaillée des Principales Méthodes d'Interprétabilité

Pour répondre au besoin croissant de transparence, une multitude de méthodes d'interprétabilité ont été développées. Elles peuvent être classées selon plusieurs axes, ce qui aide à comprendre leur portée et leur applicabilité.

Taxonomie des méthodes :

Intrinsèquement interprétables vs. Post-hoc :

Les modèles intrinsèquement interprétables sont ceux dont la structure même est transparente et compréhensible par nature. Des exemples classiques incluent la régression linéaire (où les coefficients indiquent l'importance et la direction de l'influence de chaque variable), les arbres de décision (dont les chemins de décision peuvent être lus comme des règles IF-THEN), et les systèmes basés sur des règles. Leur processus de décision est directement accessible sans nécessiter d'outils d'explication supplémentaires.   
Les méthodes post-hoc sont conçues pour expliquer des modèles qui ont déjà été entraînés, souvent des "boîtes noires" comme les réseaux de neurones profonds ou les forêts aléatoires. Elles fonctionnent en analysant le comportement du modèle (ses entrées et sorties) sans modifier sa structure interne. Ces méthodes sont particulièrement utiles lorsque la performance prédictive du modèle complexe est primordiale et qu'on ne souhaite pas la sacrifier pour une interprétabilité intrinsèque.   
Spécifiques au modèle vs. Agnostiques au modèle :

Les méthodes spécifiques au modèle sont conçues pour une classe particulière de modèles et exploitent leur structure interne. Par exemple, l'analyse de l'importance des caractéristiques basée sur la réduction de l'impureté de Gini est spécifique aux arbres de décision et aux forêts aléatoires. De même, les cartes de saillance (saliency maps) sont souvent utilisées pour visualiser les régions d'une image qui activent le plus les neurones dans les réseaux de convolution.
Les méthodes agnostiques au modèle (model-agnostic) peuvent, en théorie, être appliquées à n'importe quel modèle d'apprentissage automatique, car elles n'accèdent qu'aux entrées et aux sorties du modèle, le traitant comme une boîte noire. LIME et SHAP sont des exemples éminents de cette catégorie. Leur principal avantage est la flexibilité : un analyste peut utiliser le même outil d'interprétation pour comparer différents types de modèles.   
Locales vs. Globales :

Les explications locales se concentrent sur la compréhension d'une prédiction individuelle. Elles répondent à des questions comme : "Pourquoi cette demande de prêt spécifique a-t-elle été refusée?" ou "Quelles caractéristiques de cette image ont conduit à sa classification comme 'chat'?".   
Les explications globales visent à décrire le comportement général du modèle dans son ensemble. Elles cherchent à répondre à des questions comme : "Quelles sont les caractéristiques les plus importantes en moyenne pour ce modèle?" ou "Comment le modèle réagit-il globalement à la variation d'une caractéristique donnée?".   
Il est important de noter qu'il n'existe pas de méthode d'interprétabilité universellement supérieure. Le choix d'une méthode ou d'une combinaison de méthodes dépendra fortement du type de modèle utilisé, du public auquel l'explication est destinée (par exemple, un développeur de modèles, un expert du domaine, un client final), de la nature de l'explication recherchée (locale ou globale), et des contraintes computationnelles. Souvent, une compréhension holistique du comportement d'un modèle ne peut être atteinte qu'en combinant plusieurs approches d'interprétabilité. Par exemple, on pourrait utiliser SHAP pour obtenir des explications locales détaillées pour des instances spécifiques, tout en utilisant la Permutation Feature Importance pour avoir une vue d'ensemble des facteurs les plus influents au niveau global. Cette complémentarité est essentielle pour une interprétation robuste.

Méthodes agnostiques locales : LIME et SHAP

Parmi les méthodes post-hoc et agnostiques au modèle, LIME et SHAP ont gagné une popularité considérable en raison de leur flexibilité et de la nature intuitive de leurs explications.

LIME (Local Interpretable Model-agnostic Explanations) :

Principe : LIME vise à expliquer les prédictions de n'importe quel classifieur ou régresseur en apprenant un modèle interprétable (par exemple, un modèle linéaire, un arbre de décision peu profond) qui approxime localement le comportement du modèle boîte noire autour de l'instance de prédiction spécifique que l'on souhaite expliquer.   
Fonctionnement : Pour expliquer une prédiction pour une instance donnée, LIME procède en plusieurs étapes :
Il génère un ensemble de données de voisinage en perturbant légèrement l'instance originale (par exemple, en masquant des mots dans un texte, en modifiant des super-pixels dans une image, ou en échantillonnant à partir d'une distribution pour des données tabulaires).
Il obtient les prédictions du modèle boîte noire pour chacun de ces nouveaux points de données générés.
Il ajuste ensuite un modèle simple et interprétable (le "modèle explicatif") sur cet ensemble de données de voisinage, en pondérant les points de données en fonction de leur proximité avec l'instance originale. Les caractéristiques utilisées par ce modèle simple sont choisies pour être interprétables par l'humain (par exemple, la présence ou l'absence de mots, de super-pixels).
Caractéristiques souhaitées : LIME a été conçu avec plusieurs objectifs en tête : être agnostique au modèle, fournir une fidélité locale (l'explication doit bien refléter le comportement du modèle dans le voisinage de l'instance), et être interprétable (l'explication elle-même doit être compréhensible).   
Forces : LIME est applicable à une grande variété de types de données (texte, images, données tabulaires) et de modèles. Ses explications, souvent présentées comme une liste de caractéristiques importantes avec leurs poids, sont généralement intuitives.
Limites : La stabilité des explications de LIME peut être une préoccupation, car elles peuvent varier en fonction de la manière dont le voisinage est échantillonné et de la définition de la "localité" (la fonction de noyau de proximité). De plus, en utilisant un modèle simple pour approximer un modèle complexe, LIME peut ne pas toujours capturer toute la richesse ou la complexité du comportement du modèle original, même localement.   
Utilisation pour la confiance : Les explications LIME peuvent aider les utilisateurs à évaluer s'ils doivent faire confiance à une prédiction spécifique et peuvent également être utilisées pour comparer le comportement de différents modèles sur des instances particulières.   
SHAP (SHapley Additive exPlanations) :

Principe : SHAP est une approche unifiée pour l'interprétation des prédictions de modèles, qui attribue à chaque caractéristique une valeur d'importance pour une prédiction particulière. Ces valeurs d'importance, appelées valeurs SHAP, sont basées sur les valeurs de Shapley, un concept issu de la théorie des jeux coopératifs.   
Fonctionnement : La valeur de Shapley d'une caractéristique pour une prédiction donnée est sa contribution marginale moyenne à la prédiction, calculée en considérant toutes les combinaisons possibles (coalitions) des autres caractéristiques. Essentiellement, elle mesure comment la prédiction change lorsque la caractéristique est ajoutée à différentes combinaisons de caractéristiques déjà présentes.   
Propriétés désirables : SHAP se distingue par ses solides fondements théoriques et garantit trois propriétés importantes pour les explications additives :
Exactitude locale (Local Accuracy) : La somme des valeurs SHAP des caractéristiques pour une instance donnée (plus la valeur de base ou espérée) est égale à la prédiction du modèle pour cette instance.
Absence (Missingness) : Une caractéristique qui n'a aucune influence sur la prédiction (par exemple, si sa valeur est manquante et que cela n'affecte pas la sortie) devrait avoir une valeur SHAP de zéro.
Cohérence (Consistency) : Si un modèle est modifié de telle sorte que la contribution d'une caractéristique à la prédiction augmente ou reste la même (quelles que soient les autres caractéristiques), alors la valeur SHAP attribuée à cette caractéristique ne devrait pas diminuer. Cette propriété assure que les attributions se comportent de manière intuitive.   
Forces : Le principal atout de SHAP réside dans son cadre théorique robuste qui unifie plusieurs méthodes d'interprétation existantes (y compris LIME, qui peut être vu comme une approximation des valeurs de Shapley sous certaines conditions de choix de noyau et de fonction de perte). Il fournit des garanties de cohérence que d'autres méthodes n'offrent pas toujours. Des implémentations efficaces comme KernelSHAP (agnostique au modèle mais potentiellement lent) et TreeSHAP (optimisé pour les modèles basés sur les arbres) le rendent applicable en pratique. Les visualisations basées sur SHAP (diagrammes de dépendance, graphiques récapitulatifs) sont également très informatives.   
Limites : Le calcul exact des valeurs de Shapley peut être très coûteux en termes de calculs, en particulier pour les modèles non arborescents et lorsque le nombre de caractéristiques est élevé. KernelSHAP, bien qu'agnostique, peut être lent. L'interprétation des valeurs SHAP pour des caractéristiques fortement corrélées peut également être délicate, car la méthode suppose une certaine indépendance lors de la permutation des coalitions.
L'émergence de SHAP marque une étape importante dans le domaine de l'interprétabilité locale. En fournissant un cadre unifié, théoriquement fondé sur les valeurs de Shapley, SHAP offre une approche plus rigoureuse et cohérente que certaines méthodes antérieures plus heuristiques comme LIME. Le fait que SHAP puisse, par exemple, guider le choix des paramètres de LIME pour que ce dernier satisfasse les propriétés de cohérence  témoigne d'une maturation du domaine, passant d'approches ad-hoc à des méthodologies plus axiomatiques. La popularité croissante de SHAP dans la communauté de l'apprentissage automatique atteste de son utilité pratique et de la valeur de ses garanties théoriques.   

Méthodes basées sur les règles et les arbres de décision :

Ces méthodes sont souvent citées comme des exemples de modèles intrinsèquement interprétables, bien que leur complexité puisse influencer leur degré réel de compréhensibilité.

Arbres de décision : Un arbre de décision unique est intrinsèquement interprétable car chaque chemin de la racine à une feuille correspond à une série de conditions sur les caractéristiques, qui peut être directement traduite en une règle IF-THEN. La prédiction à la feuille est le résultat de cette règle. L'importance des caractéristiques peut être dérivée de leur fréquence d'apparition près de la racine de l'arbre ou de la quantité de réduction d'impureté (par exemple, l'indice de Gini ou l'entropie) qu'elles apportent à chaque scission.   
Forêts aléatoires (Random Forests) : Une forêt aléatoire est un ensemble de multiples arbres de décision entraînés sur des sous-ensembles bootstrap des données et des caractéristiques. Bien qu'une forêt entière soit plus complexe à interpréter globalement qu'un seul arbre, des mesures d'importance des caractéristiques (comme l'importance moyenne de Gini ou l'importance par permutation) peuvent être agrégées sur tous les arbres de la forêt pour donner une estimation globale de l'influence de chaque caractéristique. Pour des explications locales, des méthodes comme TreeSHAP peuvent décomposer la prédiction d'une forêt pour une instance spécifique en contributions de caractéristiques.   
Systèmes basés sur des règles : Ces systèmes utilisent un ensemble de règles logiques (souvent de type IF-THEN) pour prendre des décisions. Ces règles peuvent être définies par des experts du domaine ou apprises à partir des données (par exemple, avec des algorithmes comme RuleFit  ou RIPPER). Il est également possible d'extraire des règles approximatives à partir de modèles plus complexes (boîtes noires) pour fournir une explication simplifiée. Les règles sont généralement considérées comme très compréhensibles par les humains.   
Forces : La principale force de ces méthodes, en particulier pour les arbres simples et les ensembles de règles concis, est leur haute intelligibilité. Elles peuvent modéliser des relations non linéaires et des interactions entre caractéristiques de manière explicite.
Limites : Les arbres de décision uniques peuvent être instables (de petites variations dans les données d'entraînement peuvent conduire à des arbres très différents) et peuvent ne pas toujours bien généraliser. Les forêts aléatoires améliorent la stabilité et la performance, mais l'ensemble du modèle devient moins directement interprétable. De même, un grand nombre de règles complexes peut devenir difficile à appréhender pour un humain. L'extraction de règles à partir de modèles complexes peut entraîner une perte de fidélité par rapport au modèle original.   
Ces approches illustrent bien le dilemme classique entre précision et interprétabilité. Un arbre de décision simple est facile à comprendre mais peut offrir des performances prédictives moindres par rapport à une forêt aléatoire, qui est plus performante mais plus opaque. Les techniques d'interprétation pour les modèles d'ensemble, comme l'importance agrégée des caractéristiques ou les méthodes basées sur SHAP, tentent de naviguer ce compromis. Elles permettent d'obtenir des informations sur le fonctionnement de ces modèles plus complexes, mais une compréhension globale et exhaustive de la logique d'une grande forêt aléatoire ou d'un vaste ensemble de règles reste un défi.

Le cas de l'attention dans les réseaux de neurones :

Les mécanismes d'attention ont été initialement introduits dans les réseaux de neurones pour améliorer les performances, en particulier dans des tâches séquentielles comme la traduction automatique ou la reconnaissance d'images, en permettant au modèle de se concentrer sur les parties les plus pertinentes de l'entrée. Rapidement, ces poids d'attention ont été proposés comme un moyen d'expliquer les décisions du modèle. L'idée intuitive est que les parties de l'entrée qui reçoivent des poids d'attention plus élevés sont celles qui contribuent le plus à la sortie du modèle.   

Cependant, cette interprétation a fait l'objet d'un débat animé dans la communauté scientifique :

Le camp "Attention is not Explanation" (Jain & Wallace, 2019)  :
Cette étude a remis en question la fiabilité des poids d'attention comme explications fidèles. Leurs principaux arguments étaient :   

Faible corrélation avec d'autres mesures d'importance : Les poids d'attention ne montraient souvent qu'une faible corrélation avec d'autres mesures d'importance des caractéristiques bien établies, telles que celles basées sur les gradients ou les techniques de "leave-one-out".
Existence d'attentions contradictoires : Il était possible de construire des distributions d'attention alternatives, très différentes de celles apprises par le modèle, qui produisaient néanmoins des prédictions quasi identiques. Cela suggère que l'attention apprise n'est pas nécessairement la seule "bonne" explication, ni même une explication fidèle du comportement causal du modèle.
Le camp "Attention is not not Explanation" (Wiegreffe & Pinter, 2019)  :
En réponse, Wiegreffe et Pinter ont avancé que la conclusion de Jain et Wallace était trop catégorique. Leurs arguments incluaient :   

La définition de l'explication est cruciale : Ce qui constitue une "explication" satisfaisante peut varier. Les poids d'attention pourraient ne pas être une explication causale complète, mais ils pourraient néanmoins fournir des informations utiles sur le comportement du modèle.
L'attention est une partie intégrante du modèle : Détacher les scores d'attention du reste du modèle pour les manipuler (comme dans la recherche d'attentions contradictoires) dégrade le modèle lui-même et ne reflète pas comment le modèle fonctionne réellement, car les poids d'attention sont appris conjointement avec les autres paramètres du modèle.
Proposition de tests alternatifs : Ils ont suggéré d'autres protocoles pour évaluer si et quand l'attention peut servir d'explication, tels que l'utilisation d'une baseline avec des poids d'attention uniformes pour mesurer l'impact de l'apprentissage de l'attention, la calibration de la variance des poids d'attention sur plusieurs exécutions avec des graines aléatoires différentes, l'utilisation de diagnostics avec des poids gelés de modèles pré-entraînés, ou encore un entraînement contradictoire de l'attention de bout en bout.
Ils ont montré que même lorsque des distributions d'attention contradictoires fiables pouvaient être trouvées, celles-ci ne fonctionnaient pas bien sur des diagnostics simples, indiquant que les travaux antérieurs ne réfutaient pas complètement l'utilité des mécanismes d'attention pour l'explicabilité.
Ce débat sur l'attention met en exergue une difficulté fondamentale dans l'interprétation des mécanismes internes des modèles d'apprentissage profond. Ce qui peut sembler intuitivement explicatif, comme les visualisations des poids d'attention, peut ne pas résister à un examen rigoureux de sa fidélité ou de sa robustesse en tant qu'explication causale. Cela souligne la nécessité de développer des méthodologies de test rigoureuses et des définitions claires de ce qui constitue une "bonne" explication, au-delà de la simple visualisation des activations internes. L'interprétabilité n'est pas simplement une question de "regarder à l'intérieur" du modèle ; elle exige une démarche scientifique pour valider que ce qui est observé reflète véritablement et de manière fiable le processus décisionnel du modèle.

Tableau 1 : Tableau Comparatif des Principales Méthodes d'Interprétabilité

Méthode	Type (Intrinsèque/Post-hoc)	Agnosticité (Agnostique/Spécifique)	Scope (Local/Global)	Principe de base	Forces Clés	Faiblesses/Limites Techniques et Conceptuelles	Exemples d'Application
LIME (Local Interpretable Model-agnostic Explanations)	Post-hoc	Agnostique	Local	Approximation locale du modèle boîte noire par un modèle interprétable (ex: linéaire) sur un voisinage de l'instance à expliquer. 	Applicable à divers types de données (texte, image, tabulaire) et modèles. Intuitif. 	Stabilité des explications (sensibilité à l'échantillonnage et à la définition de la localité). Peut ne pas capturer toute la complexité locale. 	Expliquer les prédictions de classifieurs d'images, de modèles de NLP. 
SHAP (SHapley Additive exPlanations)	Post-hoc	Agnostique (KernelSHAP), Spécifique (TreeSHAP)	Local (peut être agrégé pour global)	Attribution de l'importance des caractéristiques basée sur les valeurs de Shapley de la théorie des jeux. 	Fondement théorique solide (exactitude locale, cohérence, additivité). Unifie plusieurs méthodes. 	Coût computationnel pour les modèles non arborescents (KernelSHAP). Interprétation délicate avec caractéristiques corrélées.	Expliquer les prédictions de modèles complexes en finance (scores de crédit), santé.
Arbres de Décision	Intrinsèque	Spécifique	Global (structure de l'arbre), Local (chemin de décision)	Partitionnement récursif de l'espace des caractéristiques basé sur des critères de division (ex: Gini, entropie). 	Très interprétable (règles IF-THEN). Visualisation facile. Gère les non-linéarités. 	Instabilité (sensibles aux petites variations des données). Tendance au surapprentissage si non élagués. Peuvent mal modéliser les relations linéaires. 	Systèmes d'aide à la décision médicale, segmentation client.
Forêts Aléatoires	Intrinsèque (ensemble d'arbres) mais globalement opaque	Spécifique	Global (importance agrégée des caractéristiques), Local (avec TreeSHAP ou analyse d'arbres individuels)	Ensemble d'arbres de décision entraînés sur des échantillons bootstrap des données. 	Haute performance, robustesse au surapprentissage. Fournit des mesures d'importance des caractéristiques (Gini, permutation). 	Le modèle agrégé est une "boîte noire". L'interprétation globale directe est difficile. L'importance de Gini peut être biaisée avec des caractéristiques de cardinalités différentes ou corrélées.	Détection de fraude, diagnostic médical, applications écologiques. 
Règles (IF-THEN)	Intrinsèque (si apprises directement), Post-hoc (si extraites)	Spécifique (si apprises), Agnostique (si extraites d'un modèle boîte noire)	Local (une règle pour une décision), Global (ensemble de règles)	Représentation logique des conditions conduisant à une décision.	Très haute intelligibilité pour les humains. Faciles à communiquer.	Les ensembles de règles peuvent devenir très grands et complexes. L'extraction de règles fidèles à partir de modèles complexes est difficile.	Systèmes experts, filtrage de spam, underwriting.
Attention (dans les Réseaux de Neurones)	Post-hoc (analyse des poids appris)	Spécifique (aux architectures avec attention)	Local (poids d'attention pour une instance)	Poids attribués aux parties de l'entrée indiquant leur importance pour la sortie. 	Fournit une intuition sur les parties de l'entrée sur lesquelles le modèle se "concentre". Utile en NLP et vision.	Débat sur la fidélité comme explication ("Attention is not Explanation"). Peut ne pas corréler avec d'autres mesures d'importance. Sensible aux configurations. 	Traduction automatique, classification de texte, reconnaissance d'objets dans les images.
  
1.4. Évaluation de l'Interprétabilité

L'évaluation de l'interprétabilité des modèles d'apprentissage automatique est un aspect aussi crucial que complexe. Si l'objectif est de rendre les modèles compréhensibles et fiables, il est impératif de pouvoir mesurer la "qualité" des explications produites.

Défis de l'évaluation :
Le domaine de l'évaluation de l'XAI est confronté à plusieurs défis majeurs :

Manque de métriques standardisées et fiables : Il n'existe pas de consensus universel sur la manière de mesurer l'interprétabilité. L'évaluation actuelle est souvent fragmentée, s'appuyant sur des métriques subjectives ou des proxies qui peuvent être biaisés ou incomplets.   
Absence de "vérité terrain" (ground truth) pour les explications : Contrairement à la prédiction où l'on peut comparer la sortie du modèle à une valeur réelle, il est difficile de définir ce qu'est une explication "correcte" ou "vraie" de manière objective. Cela complique grandement la comparaison quantitative entre différentes méthodes d'XAI.   
Vulnérabilité à la manipulation : Certaines métriques d'interprétabilité ou les explications elles-mêmes peuvent être sujettes à des manipulations, intentionnelles ou non, où des explications trompeuses pourraient apparaître comme satisfaisantes selon certaines métriques.   
Approches d'évaluation (inspirées de Doshi-Velez & Kim, 2017 ) :
Pour structurer l'évaluation, Doshi-Velez et Kim proposent une taxonomie qui distingue trois niveaux d'évaluation, allant de tâches spécifiques à des proxies plus généraux :   

Évaluation fondée sur l'application (Application-grounded) :

Description : Cette approche est la plus contextuelle et la plus proche de l'objectif final. Elle consiste à mener des expériences avec de vrais utilisateurs humains (souvent des experts du domaine) effectuant leurs tâches réelles à l'aide du système d'IA explicable. L'évaluation porte sur l'utilité de l'explication dans l'accomplissement de cette tâche.
Exemples : Un médecin utilise un système XAI pour l'aide au diagnostic et on évalue si les explications améliorent sa précision diagnostique, sa confiance, ou sa capacité à détecter des erreurs du modèle. Pour des raisons pratiques (coût, temps), des versions simplifiées de la tâche réelle peuvent être utilisées.   
Avantages : Évaluation la plus directe de l'utilité réelle de l'explication.
Limites : Coûteuse en temps et en ressources, difficile à mettre en œuvre à grande échelle, nécessite des experts du domaine.
Évaluation fondée sur l'humain (Human-grounded) :

Description : Lorsque les expériences en contexte réel sont trop complexes ou coûteuses, cette approche utilise de vrais humains (qui peuvent être des non-experts ou des profanes recrutés via des plateformes de crowdsourcing) pour effectuer des tâches simplifiées qui capturent l'essence de la qualité d'une explication.
Exemples :
Choix binaire forcé : Présenter aux participants deux explications pour la même prédiction et leur demander de choisir la "meilleure" selon certains critères (clarté, utilité, etc.).
Simulation de la prédiction : Donner aux participants une explication et une instance d'entrée, et leur demander de prédire la sortie du modèle. Leur capacité à le faire correctement mesure leur compréhension.
Simulation contrefactuelle : Présenter une explication, une instance, sa prédiction, et demander quels changements dans l'entrée mèneraient à une prédiction différente.   
Avantages : Plus facile à mettre en œuvre et moins coûteuse que l'évaluation fondée sur l'application, permet de tester des aspects plus généraux de la qualité de l'explication.
Limites : Les tâches simplifiées peuvent ne pas refléter pleinement la complexité des cas d'usage réels.
Évaluation fondée sur la fonction (Functionally-grounded) :

Description : Cette approche ne nécessite pas d'expériences humaines directes. Elle s'appuie sur des définitions formelles et des proxies quantitatifs de l'interprétabilité pour évaluer la qualité de l'explication.
Exemples : Mesurer la parcimonie d'un arbre de décision (nombre de nœuds ou de feuilles), la fidélité d'un modèle de substitution par rapport au modèle original, la robustesse d'une explication à de petites perturbations de l'entrée.
Avantages : Facile à automatiser, peu coûteuse, utile pour le développement itératif et la comparaison rapide de méthodes. Particulièrement pertinente lorsque les méthodes ne sont pas encore matures pour des tests humains ou lorsque ces derniers sont irréalisables.   
Limites : Les proxies formels ne capturent pas toujours ce qui rend une explication réellement compréhensible ou utile pour un humain. Une explication peut être "bonne" selon une métrique fonctionnelle mais mauvaise du point de vue humain.
Métriques d'évaluation spécifiques :
Les approches ci-dessus peuvent s'appuyer sur diverses métriques, qui peuvent être qualitatives ou quantitatives :

Qualitatives/Subjectives (souvent issues d'évaluations fondées sur l'humain) :

Qualité de l'explication (Explanation Goodness) : Évaluée par des humains sur des critères comme la clarté, la précision, la concision, la satisfaction de l'utilisateur. Hoffman et al. proposent une "Goodness Checklist" pour guider cette évaluation.   
Compréhension de l'utilisateur (User Understanding) : Mesure à quel point l'utilisateur comprend le fonctionnement du système, que ce soit pour une décision locale ou pour le comportement global du modèle.   
Confiance et Dépendance Appropriées (Appropriate Trust and Reliance) : L'explication aide-t-elle l'utilisateur à calibrer correctement sa confiance dans les prédictions du système, en évitant la sur-confiance ou la sous-confiance?.   
Quantitatives/Objectives (peuvent être fonctionnelles ou issues d'évaluations fondées sur l'humain) :

Fidélité (Fidelity) : À quel point l'explication (par exemple, un modèle de substitution) reflète-t-elle fidèlement le comportement du modèle original qu'elle cherche à expliquer?.   
Robustesse/Stabilité (Robustness/Stability) : Des entrées similaires produisent-elles des explications similaires et cohérentes? L'explication est-elle résistante aux petites perturbations ou aux manipulations contradictoires?.   
Performance sur tâche proxy : Si l'explication est elle-même un modèle (par exemple, un arbre de décision extrait d'un réseau de neurones), quelle est sa performance prédictive?
Complexité de l'explication : Des mesures comme la taille de l'arbre de décision, le nombre de règles dans un ensemble de règles, ou le nombre de caractéristiques dans une explication locale.
Adaptabilité et Résistance à la falsification (Tamper-Resistance) des métriques : Les métriques d'évaluation elles-mêmes doivent être robustes et ne pas être facilement "jouables".   
Scalabilité des métriques : Les métriques doivent être calculables efficacement, même pour des modèles et des ensembles de données volumineux.   
Bien que les métriques fonctionnelles et les proxies quantitatifs soient précieux pour le développement et la comparaison algorithmique, l'évaluation de l'interprétabilité, en particulier dans les domaines à fort enjeu, ne peut se passer de la dimension humaine. L'objectif ultime de l'XAI est de rendre les modèles d'IA compréhensibles par les humains et utiles pour les humains dans leurs tâches et prises de décision. Par conséquent, même si elles sont plus coûteuses et complexes à mettre en œuvre, les évaluations centrées sur l'humain (qu'elles soient fondées sur l'application ou sur des tâches simplifiées) sont indispensables pour valider réellement si une méthode d'interprétabilité atteint ses objectifs de clarté, d'utilité et de renforcement de la confiance. Une explication peut être techniquement fidèle et concise selon une métrique formelle, mais rester obscure ou même trompeuse pour un utilisateur final. La validation humaine est donc le test ultime de la valeur d'une explication.

Tableau 2 : Tableau des Approches d'Évaluation de l'Interprétabilité (basé sur Doshi-Velez & Kim, 2017)

Approche d'Évaluation	Description	Métriques/Exemples de Tests Associés	Avantages	Limites/Défis
Application-grounded (Fondée sur l'application)	Expériences avec de vrais humains (experts du domaine) sur des tâches réelles ou des versions simplifiées de tâches réelles. 	Mesure de l'amélioration de la performance de l'expert (ex: précision du diagnostic médical), efficacité de la tâche, confiance de l'expert, découverte de nouvelles connaissances. 	Évaluation la plus directe de l'utilité réelle de l'explication dans son contexte d'usage. Forte validité écologique.	Très coûteuse en temps et en ressources. Nécessite des experts du domaine. Difficile à généraliser. Peut être influencée par de nombreux facteurs confondants.
Human-grounded (Fondée sur l'humain)	Expériences avec de vrais humains (peuvent être des non-experts) sur des tâches simplifiées et abstraites qui capturent l'essence de la qualité de l'explication. 	Choix binaire forcé entre explications, capacité à simuler la prédiction du modèle, temps de réponse, évaluation subjective de la qualité/satisfaction. 	Moins coûteuse et plus facile à mettre en œuvre que l'évaluation fondée sur l'application. Permet de contrôler plus facilement les variables. Plus grand bassin de participants potentiels.	Les tâches simplifiées peuvent ne pas refléter la complexité des usages réels. La généralisabilité aux experts du domaine peut être limitée.
Functionally-grounded (Fondée sur la fonction)	Évaluation sans intervention humaine directe, utilisant des proxies formels et quantitatifs de l'interprétabilité. 	Parcimonie (taille de l'arbre, nombre de règles), fidélité (erreur du modèle explicatif par rapport au modèle original), robustesse (stabilité de l'explication face à des perturbations). 	Facile à automatiser, peu coûteuse, rapide. Utile pour le développement itératif et la comparaison d'algorithmes. Peut être utilisée lorsque les tests humains sont infaisables ou non éthiques. 	Les proxies formels ne capturent pas toujours la compréhension ou l'utilité humaine. Risque de sur-optimiser pour une métrique qui n'est pas alignée avec les besoins réels des utilisateurs.
  
Partie 2 : Systèmes de Recommandation

Les systèmes de recommandation sont devenus des outils technologiques omniprésents, influençant de manière significative la manière dont les individus découvrent et interagissent avec l'information, les produits et les services dans un monde numérique saturé de choix.

2.1. Définition et Objectifs des Systèmes de Recommandation

Un système de recommandation (SR), ou système de suggestion, est fondamentalement un système de filtrage d'information qui cherche à prédire la "note" ou la "préférence" qu'un utilisateur attribuerait à un item (élément). Plus largement, les SR sont définis comme des systèmes qui aident les utilisateurs à identifier des items d'intérêt parmi un ensemble potentiellement très vaste d'alternatives. Pour ce faire, ils analysent les données du comportement historique des utilisateurs (comme les achats passés, les évaluations, les clics) et/ou les caractéristiques des items pour prédire le contenu, les produits ou les services que les utilisateurs pourraient trouver intéressants ou utiles.   

Les objectifs principaux des systèmes de recommandation sont multiples et servent souvent à la fois les intérêts des utilisateurs et ceux des plateformes qui les déploient :

Lutter contre la surcharge d'information : Aider les utilisateurs à naviguer dans de vastes catalogues d'items et à trouver ce qui est pertinent pour eux, évitant ainsi la paralysie décisionnelle.   
Augmenter la satisfaction et la fidélité des utilisateurs : En fournissant des recommandations personnalisées et pertinentes, les SR visent à améliorer l'expérience utilisateur, ce qui peut conduire à une plus grande satisfaction et à une fidélisation accrue à la plateforme.   
Augmenter les ventes et l'engagement : Pour les plateformes commerciales, un objectif clé est d'augmenter les revenus, par exemple en facilitant la découverte de produits (conversion), en suggérant des items complémentaires (cross-selling), ou en encourageant une plus grande consommation de contenu.   
Permettre la découverte (Sérendipité) : Au-delà de recommander des items évidemment liés aux préférences passées, certains SR visent à introduire une part de nouveauté et de surprise, en suggérant des items que l'utilisateur n'aurait pas découverts par lui-même mais qu'il pourrait néanmoins apprécier.   
Le fonctionnement de base d'un SR implique typiquement deux modules principaux : un module d'apprentissage qui analyse les données passées (interactions utilisateur-item, caractéristiques des items/utilisateurs) pour inférer des modèles de préférences, et un module de conseil (ou de prédiction) qui applique le modèle appris pour générer des recommandations pour un utilisateur actif. L'objectif technique est souvent d'estimer une fonction de notation R : Utilisateur × Item → Évaluation pour les paires (utilisateur, item) pour lesquelles l'évaluation n'est pas encore connue.   

Cette dualité d'objectifs – servir l'utilisateur en lui fournissant des suggestions utiles et personnalisées, tout en servant la plateforme en augmentant l'engagement ou les revenus – est une caractéristique fondamentale des systèmes de recommandation. Idéalement, ces objectifs sont alignés : un utilisateur satisfait par des recommandations pertinentes est plus susceptible de continuer à utiliser la plateforme et d'y effectuer des transactions. Cependant, des tensions peuvent apparaître si, par exemple, le système privilégie la recommandation d'items à plus forte marge pour la plateforme au détriment de la pertinence optimale pour l'utilisateur. Comprendre cette double finalité est essentiel pour concevoir, évaluer et critiquer les systèmes de recommandation.

2.2. Aperçu des Principales Techniques Existantes

Le domaine des systèmes de recommandation a vu émerger une grande diversité de techniques, chacune avec ses propres principes, forces et faiblesses.

Filtrage Collaboratif (Collaborative Filtering - CF) :
C'est l'une des approches les plus anciennes et les plus influentes. Le principe fondamental est de faire des recommandations à un utilisateur en se basant sur les goûts d'autres utilisateurs ayant des préférences similaires (les "voisins") ou sur la similarité entre les items, cette similarité étant elle-même déduite des interactions des utilisateurs.   

Filtrage Collaboratif Basé sur l'Utilisateur (User-based CF - UBCF) : Identifie des utilisateurs similaires à l'utilisateur actif en comparant leurs historiques d'évaluation, puis recommande les items que ces utilisateurs similaires ont appréciés et que l'utilisateur actif ne connaît pas encore.   
Filtrage Collaboratif Basé sur l'Item (Item-based CF - IBCF) : Calcule les similarités entre les items en se basant sur la manière dont ils ont été évalués conjointement par les utilisateurs. Ensuite, il recommande à un utilisateur actif des items qui sont similaires à ceux qu'il a déjà appréciés dans le passé.   
Avantages du CF : Ne nécessite pas de connaissance du domaine sur les items (les recommandations sont basées uniquement sur les interactions). Peut générer des recommandations surprenantes et nouvelles (sérendipité).   
Inconvénients du CF : Souffre du problème de démarrage à froid (difficulté à faire des recommandations pour les nouveaux utilisateurs ou les nouveaux items, pour lesquels il y a peu ou pas d'interactions) , de la sparsité des données (la matrice utilisateur-item est souvent très creuse, rendant les calculs de similarité peu fiables) , et de problèmes de scalabilité avec un très grand nombre d'utilisateurs ou d'items.   
Filtrage Basé sur le Contenu (Content-Based Filtering - CBF) :
Cette approche recommande des items en se basant sur une comparaison entre les caractéristiques (attributs) des items et le profil des préférences de l'utilisateur. Le système apprend à identifier les caractéristiques des items qu'un utilisateur apprécie, puis recommande d'autres items possédant des caractéristiques similaires.   

Avantages du CBF : Peut gérer les nouveaux items (tant que leurs caractéristiques sont disponibles) sans problème de démarrage à froid pour ces items. Les recommandations peuvent être expliquées en se basant sur les caractéristiques communes. L'indépendance par rapport aux autres utilisateurs évite certains problèmes du CF.   
Inconvénients du CBF : Nécessite une description riche et structurée des items, ce qui peut être difficile à obtenir pour certains types d'items (ex: musique, films). Peut conduire à une sur-spécialisation, où l'utilisateur se voit recommander uniquement des items très similaires à ceux qu'il a déjà vus, limitant la découverte et la sérendipité. Souffre du démarrage à froid pour les nouveaux utilisateurs (leur profil de préférences n'est pas encore établi).   
Factorisation de Matrices (Matrix Factorization - MF) :
Les techniques de factorisation de matrices visent à découvrir des facteurs latents (caractéristiques cachées) qui expliquent les évaluations observées. Elles décomposent la matrice utilisateur-item (souvent très grande et creuse) en deux matrices de plus faible dimensionnalité, représentant respectivement les facteurs latents des utilisateurs et des items. La prédiction d'une évaluation est alors le produit scalaire des vecteurs de facteurs latents de l'utilisateur et de l'item correspondants.   

Exemples : SVD (Singular Value Decomposition) et ses variantes adaptées aux matrices creuses, Funk MF, SVD++, Asymmetric SVD.   
Avantages de la MF : Gère efficacement la sparsité des données. Offre souvent une meilleure précision de prédiction que les méthodes CF traditionnelles. Bonne scalabilité une fois le modèle appris.   
Inconvénients de la MF : Les facteurs latents sont souvent difficiles à interpréter, rendant les recommandations moins transparentes que celles du CF basé sur les voisins. Peut encore souffrir du problème de démarrage à froid, bien que des stratégies existent pour l'atténuer.   
Approches Hybrides (Hybrid Approaches) :
Ces systèmes combinent plusieurs techniques de recommandation (par exemple, CF et CBF, ou MF avec une autre méthode) pour exploiter leurs forces respectives et pallier leurs faiblesses individuelles.   

Avantages des approches hybrides : Peuvent potentiellement surmonter les limitations des méthodes uniques, comme le démarrage à froid et la sparsité, et offrir de meilleures performances globales.   
Inconvénients des approches hybrides : Leur conception et leur mise en œuvre peuvent être plus complexes. Le réglage fin des différents composants et de leur combinaison peut être difficile.   
Approches Basées sur l'Apprentissage Profond (Deep Learning) :
L'apprentissage profond a récemment été appliqué avec succès aux systèmes de recommandation, offrant de nouvelles façons de modéliser les interactions utilisateur-item et de capturer des relations complexes.

Neural Collaborative Filtering (NCF) : Généralise la factorisation de matrices en utilisant des réseaux de neurones (en particulier des perceptrons multicouches - MLP) pour apprendre la fonction d'interaction entre les embeddings (représentations vectorielles denses) des utilisateurs et des items.   
Réseaux de Neurones sur Graphes (Graph Neural Networks - GNNs) : Modélisent explicitement les interactions utilisateur-item comme un graphe biparti. Les GNNs apprennent ensuite les embeddings des utilisateurs et des items en propageant et en agrégeant des informations à travers la structure du graphe. LightGCN est une simplification de NGCF qui s'est montrée efficace.   
Modèles Basés sur les Transformers (ex: SASRec, BERT4Rec) : Inspirés par les succès des Transformers en traitement du langage naturel, ces modèles utilisent des mécanismes d'auto-attention pour capturer les dépendances séquentielles dans l'historique des interactions d'un utilisateur et prédire le prochain item pertinent.   
Avantages de l'apprentissage profond : Capacité à modéliser des relations non linéaires et des interactions d'ordre supérieur. Les modèles séquentiels (Transformers, RNNs) peuvent capturer la dynamique des préférences utilisateur.
Inconvénients de l'apprentissage profond : Nécessitent souvent de grandes quantités de données d'interaction pour être efficaces. Peuvent être coûteux en termes de calcul à l'entraînement. L'interprétabilité est souvent réduite (ce sont des "boîtes noires").
Systèmes Basés sur la Connaissance (Knowledge-Based Recommender Systems - KBRS) :
Ces systèmes s'appuient sur des connaissances explicites concernant les items, les besoins des utilisateurs, et des règles de recommandation (par exemple, des contraintes ou des inférences logiques) pour générer des suggestions. Ils sont souvent utilisés pour des items complexes, à faible fréquence d'achat, ou pour lesquels les données d'interaction sont rares (par exemple, services financiers, immobilier, appareils photo numériques). Ils impliquent souvent un dialogue avec l'utilisateur pour éliciter ses préférences.   

Avantages des KBRS : Ne souffrent pas du problème de démarrage à froid si la base de connaissances est bien établie. Peuvent justifier leurs recommandations de manière explicite. S'adaptent bien aux préférences changeantes des utilisateurs grâce à l'élicitation interactive.   
Inconvénients des KBRS : La construction et la maintenance de la base de connaissances peuvent être très coûteuses et laborieuses (knowledge engineering bottleneck).   
Systèmes Conscients du Contexte (Context-Aware Recommender Systems - CARS) :
Ces systèmes vont au-delà de la simple relation utilisateur-item en intégrant des informations contextuelles dans le processus de recommandation. Le contexte peut inclure des facteurs tels que le temps, le lieu, la météo, l'humeur de l'utilisateur, ou la présence d'autres personnes. La fonction de recommandation devient alors R : Utilisateur × Item × Contexte → Évaluation.   

Techniques d'intégration du contexte : Pré-filtrage contextuel (filtrer les données avant d'appliquer un SR 2D), post-filtrage contextuel (filtrer ou réordonner les recommandations après leur génération par un SR 2D), ou modélisation contextuelle (intégrer directement le contexte dans le modèle de prédiction).   
Avantages des CARS : Peuvent fournir des recommandations plus pertinentes, personnalisées et opportunes en s'adaptant à la situation spécifique de l'utilisateur.
Inconvénients des CARS : Augmentent la complexité du modèle et des données. La collecte et la modélisation des informations contextuelles peuvent être difficiles. Peuvent exacerber les problèmes de sparsité des données si le contexte est trop granulaire.   
L'évolution du domaine des systèmes de recommandation témoigne d'une sophistication croissante. Partant de techniques relativement simples basées sur les interactions directes (comme le filtrage collaboratif de voisinage), le champ s'est enrichi de modèles capables de découvrir des structures latentes (factorisation de matrices), puis a intégré des approches d'apprentissage profond pour capturer des relations non linéaires et des dépendances complexes (NCF, GNNs, Transformers). Parallèlement, un besoin de recommandations plus nuancées et adaptées à des situations spécifiques ou à des domaines où les données d'interaction sont rares a conduit au développement des systèmes basés sur la connaissance et des systèmes conscients du contexte. Cette trajectoire reflète une ambition constante d'intégrer davantage de sémantique, de contexte et d'utiliser des modèles plus puissants pour appréhender la complexité du comportement humain et des processus de choix.

Tableau 3 : Tableau Synoptique des Techniques de Systèmes de Recommandation

Technique	Principe Fondamental	Avantages Clés	Inconvénients Majeurs	Gestion typique de la sparsité/démarrage à froid	Exemples d'application
CF User-based (UBCF)	Recommandations basées sur les préférences d'utilisateurs similaires. 	Simple, intuitif, sérendipité. 	Sparsité, démarrage à froid (utilisateurs), scalabilité (utilisateurs). 	Mauvaise gestion de la sparsité. Problème pour nouveaux utilisateurs.	Recommandation de films, musique.
CF Item-based (IBCF)	Recommandations basées sur la similarité entre items (déduite des évaluations). 	Plus scalable que UBCF (similarités item-item souvent plus stables), bonne qualité. 	Sparsité (moins que UBCF), démarrage à froid (items). 	Meilleure gestion de la sparsité que UBCF. Problème pour nouveaux items.	Recommandation de produits (Amazon), articles. 
Content-Based Filtering (CBF)	Recommandations basées sur les caractéristiques des items et le profil utilisateur. 	Gère nouveaux items, explicabilité. 	Sur-spécialisation, nécessite description riche des items, démarrage à froid (utilisateurs). 	Gère bien les nouveaux items (si décrits). Problème pour nouveaux utilisateurs.	Recommandation d'articles d'actualité, de pages web.
Factorisation de Matrices (MF)	Décomposition de la matrice utilisateur-item en facteurs latents. 	Bonne gestion de la sparsité, haute précision, scalabilité. 	Interprétabilité réduite, démarrage à froid. 	Bonne gestion de la sparsité. Démarrage à froid pour nouveaux utilisateurs/items (besoin d'apprendre les facteurs).	Recommandation de films (Netflix Prize), produits. 
Neural Collaborative Filtering (NCF)	Généralisation de MF avec réseaux de neurones pour modéliser l'interaction. 	Modélise interactions non-linéaires, potentiellement plus précis que MF. 	Boîte noire, besoin de données, coût computationnel.	Similaire à MF pour démarrage à froid/sparsité, mais peut mieux capturer signaux faibles.	Recommandations avec données implicites. 
GNNs pour SR	Modélisation des interactions comme un graphe, apprentissage d'embeddings via propagation. 	Capture des relations d'ordre supérieur (voisins de voisins). 	Complexité, scalabilité sur très grands graphes, sur-lissage. 	Peut atténuer la sparsité en propageant l'information. Démarrage à froid reste un défi.	Recommandations sociales, e-commerce.
Transformers pour SR	Utilisation de l'auto-attention pour modéliser les séquences de comportement utilisateur. 	Capture des dépendances à long terme dans les séquences. 	Coût computationnel, besoin de longues séquences. 	Dépend de la richesse des séquences.	Recommandation du prochain item (musique, vidéo, produit).
Knowledge-Based RS (KBRS)	Utilisation de connaissances explicites (règles, contraintes) et raisonnement. 	Pas de démarrage à froid (si connaissance dispo), explicabilité, gestion de préférences complexes. 	Coût de création/maintenance de la base de connaissances. 	Immunisé au démarrage à froid si la base de connaissances couvre les nouveaux items/utilisateurs.	Domaines complexes (services financiers, configuration de produits). 
Context-Aware RS (CARS)	Intégration du contexte (temps, lieu, etc.) dans la recommandation. 	Recommandations plus pertinentes et personnalisées à la situation. 	Complexité accrue, collecte de données contextuelles, peut exacerber sparsité. 	Peut aider si le contexte réduit l'espace de recherche, mais peut aggraver la sparsité si trop granulaire.	Recommandations touristiques, mobiles, de restaurants. 
  
2.3. Explication Détaillée et Comparaison de Deux Techniques Choisies : Filtrage Collaboratif User-Based (UBCF) et Factorisation de Matrices (MF)

Pour une analyse plus approfondie, nous avons choisi de détailler et de comparer deux techniques fondamentales et influentes dans le domaine des systèmes de recommandation : le Filtrage Collaboratif Basé sur l'Utilisateur (UBCF), qui est une approche classique basée sur le voisinage, et la Factorisation de Matrices (MF), qui représente une évolution majeure vers les modèles à facteurs latents. Ce choix permet de contraster une méthode intuitive et directe avec une approche plus abstraite mais souvent plus performante, notamment dans des conditions de données éparses.

2.3.1. Technique 1 : Filtrage Collaboratif User-Based (UBCF)

Le filtrage collaboratif basé sur l'utilisateur (UBCF) est l'une des premières et des plus intuitives formes de systèmes de recommandation. Son principe repose sur l'idée simple que les personnes qui ont eu des goûts similaires dans le passé auront probablement des goûts similaires à l'avenir.

Algorithme et Étapes Mathématiques :

Représentation des données : Les données sont généralement stockées dans une matrice utilisateur-item (R), où chaque entrée (r_{ui}) représente l'évaluation (explicite, comme une note de 1 à 5, ou implicite, comme un achat) donnée par l'utilisateur (u) à l'item (i). Cette matrice est souvent très creuse.   
Calcul de la similarité entre utilisateurs : L'étape cruciale est d'identifier les utilisateurs qui sont "similaires" à l'utilisateur actif (a) (celui pour qui on veut générer des recommandations). Chaque utilisateur peut être représenté par un vecteur de ses évaluations. Plusieurs mesures de similarité peuvent être utilisées :   
Corrélation de Pearson : Cette mesure évalue à quel point les évaluations de deux utilisateurs varient de manière conjointe par rapport à leurs évaluations moyennes respectives. Elle est calculée uniquement sur les items que les deux utilisateurs ont évalués en commun. La formule pour la similarité entre l'utilisateur actif (a) et un autre utilisateur (u) est  :
sim(a,u)= 
∑ 
j∈I 
au
​
 
​
 (r 
aj
​
 − 
r
ˉ
  
a
​
 ) 
2
 

​
  
∑ 
j∈I 
au
​
 
​
 (r 
uj
​
 − 
r
ˉ
  
u
​
 ) 
2
 

​
 
∑ 
j∈I 
au
​
 
​
 (r 
aj
​
 − 
r
ˉ
  
a
​
 )(r 
uj
​
 − 
r
ˉ
  
u
​
 )
​
 
où (I_{au}) est l'ensemble des items évalués à la fois par (a) et (u), et (\bar{r}_a) et (\bar{r}_u) sont les évaluations moyennes respectives de (a) et (u) sur les items qu'ils ont évalués. La corrélation de Pearson varie de -1 (parfaitement dissimilaires) à +1 (parfaitement similaires).   
Similarité Cosinus : Elle mesure le cosinus de l'angle entre les vecteurs d'évaluation des deux utilisateurs. Une valeur proche de 1 indique une forte similarité, proche de 0 une faible similarité (orthogonalité), et proche de -1 une dissimilarité (directions opposées). La formule est :
sim(a,u)= 
∥ 
r

  
a
​
 ∥∥ 
r

  
u
​
 ∥
r

  
a
​
 ⋅ 
r

  
u
​
 
​
 = 
∑ 
j∈I
​
 r 
aj
2
​
 

​
  
∑ 
j∈I
​
 r 
uj
2
​
 

​
 
∑ 
j∈I
​
 r 
aj
​
 r 
uj
​
 
​
 
où les sommes sont sur tous les items (I). Il est courant de centrer les évaluations (soustraire la moyenne de l'utilisateur) avant de calculer la similarité cosinus pour tenir compte des différences de sévérité dans les notations.   
Sélection des Voisins (Neighborhood Selection) : Une fois les similarités calculées entre l'utilisateur actif (a) et tous les autres utilisateurs, on sélectionne un sous-ensemble des (k) utilisateurs les plus similaires (les (k) plus proches voisins, ou k-nearest neighbors). Le choix de (k) est un hyperparamètre important.   
Génération de Prédiction : Pour prédire l'évaluation que l'utilisateur actif (a) donnerait à un item (j) qu'il n'a pas encore évalué, on agrège les évaluations de cet item (j) par les voisins sélectionnés. Une formule courante est la moyenne pondérée  :
p 
aj
​
 = 
r
ˉ
  
a
​
 + 
∑ 
u∈K 
j
​
 
​
 ∣sim(a,u)∣
∑ 
u∈K 
j
​
 
​
 sim(a,u)×(r 
uj
​
 − 
r
ˉ
  
u
​
 )
​
 
où (K_j) est l'ensemble des (k) voisins de (a) qui ont évalué l'item (j), (sim(a,u)) est la similarité entre (a) et (u), et (\bar{r}_a) et (\bar{r}_u) sont les évaluations moyennes de l'utilisateur (a) et du voisin (u) sur les items qu'ils ont évalués (utilisées ici pour la normalisation). Les items avec les scores de prédiction les plus élevés sont alors recommandés.   
Avantages :

Simplicité et Intuitivité : L'algorithme est relativement simple à comprendre et à mettre en œuvre, et son principe de "bouche-à-oreille social" est intuitif.   
Indépendance du Domaine : Il ne nécessite aucune connaissance des caractéristiques des items, car les recommandations sont basées uniquement sur les interactions utilisateur-item.   
Sérendipité : L'UBCF peut aider les utilisateurs à découvrir des items nouveaux et inattendus, car il peut identifier des intérêts croisés à travers les profils de voisins éclectiques.   
Bon Point de Départ : Il ne nécessite que la matrice de feedback pour l'entraînement, ce qui en fait un bon point de départ pour de nombreux systèmes de recommandation.   
Inconvénients :

Sparsité des Données : La performance de l'UBCF se dégrade considérablement lorsque la matrice utilisateur-item est très creuse. S'il y a peu d'items co-évalués entre les utilisateurs, les mesures de similarité deviennent peu fiables ou impossibles à calculer.   
Démarrage à Froid (Cold Start) :
Nouveaux utilisateurs : Il est difficile de faire des recommandations pour les nouveaux utilisateurs car ils n'ont pas d'historique d'évaluation, ce qui empêche de trouver des voisins similaires.   
Nouveaux items : Les nouveaux items qui n'ont pas encore été évalués par un nombre suffisant d'utilisateurs ne seront pas recommandés, même s'ils pourraient être pertinents.
Scalabilité : Le calcul de la similarité entre l'utilisateur actif et tous les autres utilisateurs peut être très coûteux en termes de calcul, en particulier lorsque le nombre d'utilisateurs (m) est grand (complexité pouvant atteindre (O(m^2 d)) où (d) est le nombre d'items, si les vecteurs sont denses, ou dépendante du nombre d'évaluations si les vecteurs sont creux). Bien que le calcul des similarités puisse être fait hors ligne, la recherche des voisins pour un nouvel utilisateur actif peut encore être longue.   
Qualité Affectée par les Utilisateurs Peu Actifs : Les utilisateurs ayant très peu d'évaluations peuvent introduire du bruit ou ne pas être de bons indicateurs de similarité.
La performance de l'UBCF est donc fortement contingente à la structure des données sous-jacentes. Dans les scénarios où les utilisateurs évaluent peu d'items, où il y a peu de chevauchement dans les items évalués par différents utilisateurs, ou où les "communautés" de goût ne sont pas clairement définies et denses, l'efficacité de l'UBCF diminue rapidement. Son succès dépend de l'existence d'une structure de "voisinage" suffisamment riche et informative dans les données d'interaction.

2.3.2. Technique 2 : Factorisation de Matrices (MF)

La factorisation de matrices est une classe d'algorithmes de filtrage collaboratif qui a gagné en popularité, notamment suite à son succès lors du Netflix Prize. Elle aborde certains des problèmes de l'UBCF, en particulier la sparsité des données, en apprenant des représentations latentes (cachées) des utilisateurs et des items.

Modèles à Facteurs Latents :
L'idée centrale est de caractériser à la fois les utilisateurs et les items par des vecteurs dans un espace latent commun de dimensionnalité (f) (où (f) est généralement bien inférieur au nombre d'utilisateurs ou d'items).   

Chaque utilisateur (u) est associé à un vecteur de facteurs latents (p_u \in \mathbb{R}^f).
Chaque item (i) est associé à un vecteur de facteurs latents (q_i \in \mathbb{R}^f). Ces facteurs latents peuvent être interprétés comme capturant des aspects ou des caractéristiques sous-jacentes des items (par exemple, pour des films : le genre, la présence de certains acteurs, le niveau d'action, etc.) et les préférences correspondantes des utilisateurs pour ces aspects. La prédiction de l'évaluation (\hat{r}_{ui}) que l'utilisateur (u) donnerait à l'item (i) est alors estimée par le produit scalaire de leurs vecteurs de facteurs latents :
r
^
  
ui
​
 =q 
i
T
​
 p 
u
​
 = 
k=1
∑
f
​
 q 
ik
​
 p 
uk
​
 
.   
Bases Mathématiques et Apprentissage :
L'objectif principal est d'apprendre les vecteurs de facteurs latents (p_u) et (q_i) pour tous les utilisateurs et items. Cela se fait généralement en minimisant une fonction de coût qui mesure l'erreur entre les évaluations prédites et les évaluations réelles connues, tout en ajoutant des termes de régularisation pour éviter le surapprentissage.

Fonction Objectif : Une fonction objectif couramment utilisée est l'erreur quadratique régularisée, minimisée sur l'ensemble (Κ) des paires (utilisateur, item) pour lesquelles l'évaluation (r_{ui}) est connue  :
p 
∗
​
 ,q 
∗
​
 
min
​
  
(u,i)∈K
∑
​
 (r 
ui
​
 −q 
i
T
​
 p 
u
​
 ) 
2
 +λ(∥q 
i
​
 ∥ 
2
 +∥p 
u
​
 ∥ 
2
 )
Le terme (\lambda (|q_i|^2 + |p_u|^2)) est le terme de régularisation (souvent L2), où (\lambda) est un hyperparamètre qui contrôle la force de la régularisation.   
Algorithmes d'Apprentissage :
Descente de Gradient Stochastique (SGD) : Cette méthode itérative parcourt les évaluations connues. Pour chaque évaluation (r_{ui}), l'erreur de prédiction (e_{ui} = r_{ui} - q_i^T p_u) est calculée. Les vecteurs (p_u) et (q_i) sont ensuite mis à jour dans la direction opposée du gradient de l'erreur  :
q 
i
​
 ←q 
i
​
 +γ(e 
ui
​
 p 
u
​
 −λq 
i
​
 )
p 
u
​
 ←p 
u
​
 +γ(e 
ui
​
 q 
i
​
 −λp 
u
​
 )
où (\gamma) est le taux d'apprentissage.   
Alternating Least Squares (ALS) / Weighted Alternating Least Squares (WALS) : Puisque la fonction objectif n'est pas convexe par rapport à (p_u) et (q_i) simultanément, mais l'est si l'un des deux est fixé, ALS alterne entre la résolution pour (p_u) (en gardant (q_i) fixe) et la résolution pour (q_i) (en gardant (p_u) fixe). Chaque étape consiste à résoudre un problème de moindres carrés standard. WALS est une variante qui permet de pondérer différemment les entrées observées et non observées, ce qui est utile pour les données implicites ou pour mieux gérer la sparsité.   
Rôle de la SVD (Singular Value Decomposition) : Bien que la SVD soit une technique de décomposition de matrices bien connue, son application directe à la matrice utilisateur-item (souvent très creuse) est problématique car la SVD classique est mal définie pour les matrices incomplètes. Les méthodes de factorisation de matrices pour les systèmes de recommandation, comme celle popularisée par Simon Funk (Funk MF), apprennent les facteurs latents directement à partir des évaluations observées via des techniques d'optimisation comme la SGD, plutôt que d'appliquer une SVD complète.   
Gestion des Biais : Les évaluations des utilisateurs peuvent être influencées par des effets qui ne sont pas directement liés à l'interaction spécifique entre un utilisateur et un item. Par exemple, certains utilisateurs ont tendance à donner des notes systématiquement plus élevées (ou plus basses) que d'autres, et certains items sont intrinsèquement plus populaires (ou impopulaires) et reçoivent des notes plus élevées (ou plus basses) en moyenne. Pour tenir compte de ces biais, le modèle de prédiction est souvent affiné  :
r
^
  
ui
​
 =μ+b 
u
​
 +b 
i
​
 +q 
i
T
​
 p 
u
​
 

où (\mu) est l'évaluation moyenne globale sur toutes les données, (b_u) est le biais de l'utilisateur (u), et (b_i) est le biais de l'item (i). Ces termes de biais sont également appris lors de la minimisation de la fonction de coût.   

Avantages :

Meilleure Gestion de la Sparsité : En apprenant des représentations denses de faible dimension (facteurs latents), la MF peut généraliser à partir des évaluations observées pour prédire les évaluations manquantes, la rendant plus robuste à la sparsité que les méthodes basées sur le voisinage.   
Précision des Prédictions : La MF atteint souvent une meilleure précision de prédiction que les techniques de voisinage classiques, comme l'a démontré le concours Netflix Prize.   
Scalabilité : Une fois les facteurs latents appris, la prédiction pour une paire (utilisateur, item) est rapide (un simple produit scalaire). L'entraînement peut être coûteux, mais des algorithmes comme ALS peuvent être parallélisés.   
Représentation Compacte : Les matrices de facteurs latents sont beaucoup plus petites que la matrice utilisateur-item originale, ce qui permet une représentation plus compacte des données.   
Inconvénients :

Interprétabilité Réduite : Les facteurs latents appris par la MF sont des constructions mathématiques qui ne correspondent pas toujours à des concepts humains intuitifs ou facilement explicables (par exemple, "genre du film" ou "tendance de l'utilisateur pour l'action"). Cela rend les recommandations moins transparentes que celles de l'UBCF.
Démarrage à Froid : Comme pour l'UBCF, la MF a du mal avec les nouveaux utilisateurs ou les nouveaux items. Pour un nouvel utilisateur ou un nouvel item, il n'y a pas de vecteur de facteurs latents pré-appris. Des stratégies ad-hoc, comme l'utilisation de la moyenne des évaluations, des caractéristiques de contenu (si disponibles) pour estimer un vecteur initial, ou des techniques de projection pour les nouveaux items ayant quelques interactions, sont nécessaires.   
Difficulté à Intégrer des Caractéristiques Contextuelles (Side Features) : Les modèles de MF de base ne prennent en compte que les identifiants des utilisateurs et des items. L'intégration d'informations supplémentaires (caractéristiques démographiques des utilisateurs, attributs des items, contexte temporel) nécessite des extensions plus complexes du modèle de base, bien que cela soit possible.   
La force distinctive de la factorisation de matrices réside dans sa capacité à projeter les utilisateurs et les items, initialement décrits par des interactions éparses, dans un espace latent commun et dense de plus faible dimension. C'est cette réduction dimensionnelle qui lui permet de capturer les relations essentielles et les "goûts" sous-jacents, tout en filtrant le bruit et en comblant implicitement les nombreuses entrées manquantes de la matrice d'interaction. Contrairement à l'UBCF qui se base sur des similarités directes entre utilisateurs, la MF apprend une structure cachée, ce qui lui confère une meilleure capacité de généralisation et une plus grande robustesse face à la sparsité des données.

2.3.3. Comparaison UBCF vs. MF

La comparaison entre le Filtrage Collaboratif Basé sur l'Utilisateur (UBCF) et la Factorisation de Matrices (MF) met en lumière des compromis fondamentaux en matière de performance, de scalabilité, de gestion des données et d'interprétabilité.

Critère de comparaison	Filtrage Collaboratif User-Based (UBCF)	Factorisation de Matrices (MF)
Principe de base	Similarité entre utilisateurs ("voisins") pour prédire les préférences. 	Décomposition de la matrice utilisateur-item en facteurs latents pour modéliser les préférences. 
Précision prédictive	Peut être bonne avec des données denses et des voisinages clairs. Se dégrade avec la sparsité.	Généralement supérieure, surtout avec des données éparses, grâce à une meilleure généralisation. 
Scalabilité (entraînement/prédiction)	Calcul des similarités utilisateur-utilisateur (phase hors ligne) coûteux ((O(m^2))). Prédiction rapide une fois les voisins trouvés. 	Entraînement (apprentissage des facteurs) peut être coûteux (SGD, ALS). Prédiction très rapide (produit scalaire). 
Gestion de la sparsité	Souffre considérablement. La similarité devient peu fiable avec peu de co-évaluations. 	Gère intrinsèquement mieux la sparsité grâce à l'apprentissage des facteurs latents qui comblent les manques. 
Gestion du démarrage à froid	Problème pour les nouveaux utilisateurs (pas de voisins, pas d'historique). Moins pour les nouveaux items s'ils sont évalués par des utilisateurs existants. 	Problème pour les nouveaux utilisateurs et les nouveaux items (pas de vecteurs latents appris). Nécessite des stratégies ad-hoc. 
Interprétabilité des recommandations	Relativement élevée : "Des utilisateurs similaires à vous ont aimé X". 	Faible : Les facteurs latents sont abstraits et n'ont pas toujours de signification intuitive.
Complexité de mise en œuvre	Conceptuellement plus simple.	Plus complexe, surtout avec des optimisations comme ALS et la gestion des biais.
Capacité à intégrer des données contextuelles/implicites	Difficile dans le modèle de base.	Peut être étendu plus facilement pour inclure des biais, des aspects temporels, des données implicites, etc. 
Sérendipité	Peut offrir une bonne sérendipité via des voisins aux goûts variés. 	Peut en offrir si les facteurs latents capturent des aspects inattendus, mais peut aussi tendre vers la popularité.
  
Cette comparaison révèle un compromis fondamental entre l'intuition et l'abstraction. L'UBCF s'appuie sur une heuristique socialement intuitive : les recommandations des pairs. Sa logique est facile à expliquer. La MF, en revanche, adopte une approche plus abstraite en modélisant les préférences à travers des dimensions latentes qui ne sont pas directement observables ou interprétables. Cette abstraction permet souvent à la MF d'obtenir de meilleures performances brutes, en particulier en termes de précision et de robustesse à la sparsité des données, mais cela se fait au détriment d'une interprétabilité directe et au prix d'une plus grande complexité algorithmique. Le choix entre ces deux approches (ou leurs variantes plus modernes) dépendra donc fortement des priorités du système de recommandation : si l'explicabilité et la simplicité sont primordiales et que la densité des données le permet, l'UBCF peut être un choix viable. Si la performance maximale et une gestion efficace de la sparsité sont les objectifs principaux, la MF et ses dérivés sont souvent préférés, même si cela implique un effort supplémentaire pour, par exemple, expliquer a posteriori les recommandations basées sur les facteurs latents.

Partie 3 : Analyse Comparative Approfondie : Bayesian Model Averaging (BMA) et Bagging

Les méthodes d'ensemble, qui combinent les prédictions de plusieurs modèles, sont une stratégie courante en apprentissage automatique pour améliorer la performance et la robustesse par rapport à l'utilisation d'un modèle unique. Le Bayesian Model Averaging (BMA) et le Bagging (Bootstrap Aggregating) sont deux approches d'ensemble distinctes, tant par leurs fondements théoriques que par leurs mécanismes de fonctionnement.

3.1. Fondements Théoriques et Principes de Fonctionnement

3.1.1. Bayesian Model Averaging (BMA)

Le BMA est une approche statistique qui s'inscrit pleinement dans le paradigme bayésien pour traiter l'incertitude inhérente au processus de sélection d'un modèle. Plutôt que de choisir un unique "meilleur" modèle parmi un ensemble de candidats et de baser toutes les inférences et prédictions sur ce seul modèle (ce qui ignore l'incertitude liée à ce choix), le BMA propose de moyenner les prédictions de tous les modèles considérés, en pondérant chaque modèle par sa probabilité d'être le vrai modèle étant donné les données observées.   

Principes Bayésiens et Probabilités a posteriori des modèles :
Au cœur du BMA se trouve le théorème de Bayes, appliqué à l'espace des modèles. Si l'on considère un ensemble de modèles candidats ({M_1, M_2,..., M_K}), la probabilité a posteriori du modèle (M_j) étant donné les données (D) est donnée par  :
P(M 
j
​
 ∣D)= 
∑ 
k=1
K
​
 P(D∣M 
k
​
 )P(M 
k
​
 )
P(D∣M 
j
​
 )P(M 
j
​
 )
​
 

où :   

(P(M_j|D)) est la probabilité a posteriori du modèle (M_j), c'est-à-dire le degré de croyance en ce modèle après avoir observé les données.
(P(D|M_j)) est la vraisemblance marginale (marginal likelihood) du modèle (M_j), également appelée évidence (evidence) du modèle. Elle représente la probabilité d'observer les données (D) si le modèle (M_j) était le vrai modèle.
(P(M_j)) est la probabilité a priori du modèle (M_j), reflétant notre croyance initiale en ce modèle avant d'observer les données. Souvent, en l'absence d'information spécifique, un a priori uniforme est choisi, (P(M_j) = 1/K).
Le dénominateur est une constante de normalisation, assurant que la somme des probabilités a posteriori sur tous les modèles est égale à 1.
Vraisemblance Marginale et ses Défis :
La vraisemblance marginale (P(D|M_j)) est la clé du BMA. Elle est obtenue en intégrant la vraisemblance du modèle par rapport à ses paramètres (\theta_j), pondérée par la distribution a priori des paramètres (P(\theta_j|M_j))  :
P(D∣M 
j
​
 )=∫P(D∣θ 
j
​
 ,M 
j
​
 )P(θ 
j
​
 ∣M 
j
​
 )dθ 
j
​
 

Le calcul de cette intégrale est souvent le principal défi computationnel du BMA, car elle peut être de haute dimension et analytiquement intraitable. Plusieurs approximations ont été développées :   

Critère d'Information Bayésien (BIC) : Le BIC fournit une approximation asymptotique du logarithme de la vraisemblance marginale : (\log P(D|M_j) \approx \log P(D|\hat{\theta}_j, M_j) - \frac{d_j}{2} \log n), où (\hat{\theta}_j) est l'estimation du maximum de vraisemblance des paramètres, (d_j) est le nombre de paramètres du modèle (M_j), et (n) est la taille de l'échantillon. Le BIC pénalise la complexité du modèle.   
Approximation de Laplace : C'est une méthode analytique qui approxime l'intégrale en utilisant une approximation quadratique du logarithme de la densité a posteriori des paramètres autour de son mode.   
Méthodes de Monte Carlo par Chaînes de Markov (MCMC) : Des techniques de simulation comme l'estimateur de la moyenne harmonique (bien que souvent instable), la méthode de Chib, ou le Reversible Jump MCMC (qui permet de sauter entre des modèles de dimensions différentes) peuvent être utilisées pour estimer numériquement la vraisemblance marginale ou les rapports de vraisemblances marginales (facteurs de Bayes).   
Rôle des A Priori : Le choix des distributions a priori, tant sur les modèles (P(M_j)) que sur les paramètres (P(\theta_j|M_j)), est une composante essentielle de l'analyse bayésienne et peut influencer les probabilités a posteriori des modèles. Les méthodes bayésiennes objectives visent à utiliser des a priori "non informatifs" ou "de référence" pour minimiser cette influence, mais la définition de tels a priori, surtout pour les paramètres de modèles complexes ou lorsque les a priori sont impropres (ne s'intégrant pas à 1), peut être délicate et affecter la validité des facteurs de Bayes.   

Prédiction avec BMA :
Une fois les probabilités a posteriori des modèles (P(M_j|D)) obtenues, la prédiction d'une nouvelle quantité d'intérêt (\Delta) (par exemple, une nouvelle observation) est calculée comme la moyenne des prédictions de chaque modèle, pondérée par sa probabilité a posteriori  :
E= 
j=1
∑
K
​
 EP(M 
j
​
 ∣D)

Cette prédiction moyennée tient compte de l'incertitude associée à la sélection du modèle.   

Avantages et Inconvénients :

Avantages : Le BMA offre une manière rigoureuse et cohérente de prendre en compte l'incertitude du modèle, évitant les risques associés au choix d'un seul modèle qui pourrait être incorrect. Il tend à fournir de meilleures performances prédictives (par exemple, au sens du score logarithmique) que la sélection d'un modèle unique, surtout lorsque plusieurs modèles sont bien soutenus par les données.   
Inconvénients : La principale difficulté réside dans sa complexité computationnelle, notamment le calcul des vraisemblances marginales et la nécessité potentielle d'explorer un très grand espace de modèles (si (K) est grand). Les résultats peuvent être sensibles au choix des a priori, en particulier si les données sont peu informatives. De plus, l'ensemble des modèles considérés ({M_j}) doit être spécifié avec soin ; si des modèles importants sont omis, le BMA ne pourra pas les considérer.   
Le BMA incarne une approche théoriquement élégante et rigoureuse pour la gestion de l'incertitude du modèle au sein du cadre bayésien. Sa force réside dans sa capacité à intégrer l'évidence de chaque modèle de manière probabiliste. Cependant, cet idéal théorique se heurte fréquemment à des obstacles pratiques significatifs. La complexité du calcul de la vraisemblance marginale et la dépendance potentielle aux a priori ont conduit à un vaste corpus de recherche sur les méthodes d'approximation. Il existe donc une tension inhérente entre la pureté théorique du BMA et la praticabilité des solutions nécessaires pour son application effective, en particulier pour les classes de modèles complexes et les grands ensembles de données.

3.1.2. Bagging (Bootstrap Aggregating)

Le Bagging, introduit par Leo Breiman en 1996 , est une méthode d'ensemble plus heuristique, conçue pour améliorer la stabilité et la précision des algorithmes d'apprentissage automatique, en particulier ceux qui sont instables.   

Principe de l'Agrégation Bootstrap :
Le mécanisme du Bagging est simple et direct  :   

À partir d'un ensemble d'entraînement original de taille (s), on génère (M) nouveaux ensembles d'entraînement (appelés échantillons bootstrap), chacun de taille (s), en tirant des exemples avec remplacement à partir de l'ensemble original. En moyenne, chaque échantillon bootstrap contiendra environ 63% des exemples originaux, certains exemples apparaissant plusieurs fois et d'autres pas du tout.   
Un modèle de prédiction (le "prédicteur de base") est entraîné indépendamment sur chacun de ces (M) échantillons bootstrap, produisant ainsi (M) versions différentes du prédicteur.
Pour une nouvelle instance, les prédictions de ces (M) modèles sont agrégées :
Pour la régression (prédiction d'une valeur numérique), on prend généralement la moyenne des (M) prédictions.
Pour la classification (prédiction d'une classe), on effectue un vote majoritaire parmi les (M) prédictions de classe.
Impact sur le Biais et la Variance :
L'objectif principal et l'effet le plus notable du Bagging est la réduction de la variance du prédicteur. La variance d'un prédicteur fait référence à la variabilité de ses prédictions si l'on changeait l'ensemble d'entraînement. Les prédicteurs "instables" sont ceux dont la structure ou les prédictions changent considérablement en réponse à de petites modifications des données d'entraînement (par exemple, les arbres de décision non élagués, les réseaux de neurones). Le Bagging est particulièrement efficace pour ces types de prédicteurs instables car la moyenne de plusieurs versions indépendantes (ou quasi-indépendantes) d'une variable aléatoire a une variance plus faible que la variable aléatoire elle-même.
En revanche, le Bagging a généralement peu d'effet sur le biais du prédicteur, voire peut l'augmenter légèrement. Le biais fait référence à l'erreur systématique du prédicteur, c'est-à-dire à quel point ses prédictions moyennes s'écartent de la vraie valeur. Si le prédicteur de base est fortement biaisé (par exemple, un modèle linéaire simple essayant de capturer une relation très non-linéaire), le Bagging ne pourra pas corriger ce biais fondamental et n'apportera que peu d'amélioration.   

Compte-rendu Bayésien du Bagging (selon P. Domingos ) :
Pedro Domingos a exploré les raisons du succès du Bagging d'un point de vue bayésien. Il a testé deux hypothèses principales :   

Hypothèse 1 (finalement rejetée) : Le Bagging fonctionnerait parce qu'il serait une approximation de la procédure bayésienne optimale de moyenne de modèles (BMA).
Variante 1a : La pondération uniforme des modèles par le Bagging serait une imperfection, et une pondération correcte par les probabilités a posteriori des modèles (en supposant un a priori non informatif) donnerait de meilleurs résultats. Les tests empiriques ont contredit cette variante, la pondération non uniforme se comportant moins bien que le Bagging standard.
Variante 1b : Le Bagging supposerait implicitement une distribution a priori sur les modèles qui annulerait approximativement l'effet de la vraisemblance pour les modèles échantillonnés. Cela impliquerait un a priori favorisant les modèles avec une erreur d'entraînement plus élevée, ce qui est contre-intuitif et également contredit par les expériences.
Hypothèse 2 (soutenue par les résultats empiriques) : Le Bagging réduirait l'erreur parce qu'il modifierait efficacement l'espace des modèles de l'apprenant de base ou sa distribution a priori implicite vers un espace ou un a priori mieux adapté au domaine. Plus précisément, de nombreux apprenants (comme les arbres de décision) ont un "biais de simplicité" intrinsèque. Le Bagging, en produisant des modèles multiples et en les agrégeant, génère un modèle combiné qui est intrinsèquement plus complexe que le modèle de base unique. Domingos suggère que le Bagging contrecarre un biais de simplicité inapproprié de l'apprenant de base en déplaçant effectivement la probabilité vers des modèles plus complexes, qui peuvent mieux capturer la structure des données.
Contexte plus large de la Probabilité Algorithmique (Ray Solomonoff ) :
Bien que non directement une explication du Bagging, la théorie de la probabilité algorithmique de Solomonoff offre un cadre philosophique pertinent pour l'inférence inductive et la sélection/combinaison de modèles. Cette théorie combine le rasoir d'Occam (préférer les explications les plus simples) avec le principe des explications multiples. Elle assigne des probabilités aux hypothèses (représentées comme des algorithmes ou des programmes) en fonction de leur complexité (longueur du programme le plus court qui les décrit). Les hypothèses plus simples reçoivent une probabilité a priori plus élevée. Le BMA s'aligne plus directement sur cette idée en pondérant explicitement différents modèles. Le Bagging, bien que moins formellement lié, peut être vu comme une manière pragmatique d'explorer implicitement un espace de modèles plus riche en perturbant les données.   

La force du Bagging réside dans sa simplicité conceptuelle, sa facilité de mise en œuvre et son efficacité empirique prouvée pour améliorer la stabilité et la précision des modèles instables. Il ne repose pas sur des hypothèses fortes concernant la distribution des données ou l'espace des modèles, ce qui le rend largement applicable. Même si son fondement théorique bayésien est moins direct et plus débattu que celui du BMA, son succès pratique en a fait une technique d'ensemble incontournable. L'interprétation de Domingos, suggérant que le Bagging modifie l'a priori implicite de l'apprenant, offre une perspective bayésienne alternative à la simple analogie avec le BMA, soulignant que son efficacité pourrait provenir d'un changement fondamental dans l'espace des hypothèses explorées.

3.2. Comparaison Détaillée BMA vs. Bagging

Bien que le BMA et le Bagging soient tous deux des méthodes d'ensemble visant à améliorer les performances prédictives par rapport à un modèle unique, ils diffèrent considérablement dans leurs principes sous-jacents, leurs hypothèses, leur complexité et la manière dont ils abordent l'incertitude.

Critère	Bayesian Model Averaging (BMA)	Bagging (Bootstrap Aggregating)
Principes sous-jacents et hypothèses	Fondé sur le théorème de Bayes. Moyenne des prédictions de plusieurs modèles pondérés par leur probabilité a posteriori (P(M_j	D)). Suppose qu'un "vrai" modèle (ou une bonne approximation) existe dans l'ensemble considéré. L'incertitude porte sur le choix de ce modèle.
Gestion de l'incertitude du modèle et du surapprentissage	Gère explicitement l'incertitude du modèle via les probabilités a posteriori. La vraisemblance marginale pénalise naturellement les modèles trop complexes, aidant à éviter le surapprentissage. La régularisation peut aussi être incluse via les a priori sur les paramètres.	Réduit le surapprentissage principalement en réduisant la variance du prédicteur. L'agrégation lisse les prédictions, rendant le modèle final moins sensible aux particularités d'un seul ensemble d'entraînement.
Complexité computationnelle	Très élevée. Nécessite souvent d'entraîner de nombreux modèles distincts, de calculer (ou d'approximer) les vraisemblances marginales (difficile), et potentiellement d'explorer un vaste espace de modèles.	Élevée mais parallélisable. Nécessite d'entraîner (M) modèles de base, mais ces entraînements sont indépendants et peuvent être effectués en parallèle.
Caractéristiques de performance typiques	Peut offrir des améliorations optimales (au sens bayésien) si l'espace des modèles est bien spécifié et les calculs (ou approximations) sont précis. Souvent limité en pratique par la difficulté des calculs.	Améliore significativement la performance des prédicteurs instables (ex: arbres de décision, réseaux de neurones). Peut légèrement dégrader la performance des prédicteurs stables (ex: k-NN, régression linéaire). Robuste et largement applicable.
Interprétabilité	L'interprétabilité du modèle moyenné peut être difficile si de nombreux modèles structurellement différents contribuent. Cependant, les poids (P(M_j	D)) peuvent indiquer quels types de modèles sont les plus soutenus par les données.
Sensibilité aux a priori / hyperparamètres	Potentiellement sensible au choix des a priori sur les modèles (P(M_j)) et sur les paramètres des modèles (P(\theta_j	M_j)), surtout avec des données limitées.
Fondement théorique	Fortement ancré dans la théorie des probabilités bayésiennes.	Plus heuristique, bien que des analyses théoriques existent (ex: réduction de variance pour les prédicteurs instables). Le "compte-rendu bayésien" de Domingos suggère un changement de l'a priori implicite plutôt qu'une approximation du BMA.
  
L'une des distinctions les plus fondamentales entre le BMA et le Bagging réside dans leur philosophie de gestion de l'incertitude et d'amélioration de la généralisation. Le BMA adopte une approche que l'on pourrait qualifier de "descendante" (top-down) : il part d'un ensemble défini de modèles candidats et utilise les principes rigoureux de la théorie bayésienne pour quantifier l'incertitude relative à chaque modèle et pour combiner leurs prédictions de manière optimale. Il s'agit d'une démarche "model-centric", où la question centrale est de savoir comment choisir et pondérer au mieux parmi un ensemble de modèles potentiels.

Le Bagging, à l'inverse, suit une approche "ascendante" (bottom-up), plus algorithmique et pragmatique. Il ne part pas d'un ensemble de modèles distincts, mais d'un algorithme d'apprentissage unique (le prédicteur de base). Il génère ensuite de la diversité en perturbant les données d'entraînement via le bootstrap, créant ainsi de multiples instances de ce même type de prédicteur. L'amélioration provient de l'agrégation de ces instances, qui vise principalement à réduire l'instabilité (variance) de l'apprenant. C'est une démarche "learner-centric", où la question est de savoir comment rendre un apprenant donné plus robuste et performant.

Cette différence de philosophie a des conséquences directes. Le BMA, avec son ambition de modéliser explicitement l'incertitude sur l'espace des modèles, se heurte à une complexité computationnelle et conceptuelle importante (spécification des a priori, calcul des évidences). Le Bagging, plus simple et direct, offre une solution "prête à l'emploi" qui fonctionne bien dans de nombreux cas, en particulier avec des apprenants instables, sans nécessiter de spécifications probabilistes complexes. L'analyse de Domingos , qui suggère que le Bagging ne se comporte pas comme une approximation du BMA mais plutôt comme une méthode qui modifie l'a priori implicite de l'apprenant vers des modèles plus complexes, renforce cette distinction. Le Bagging ne cherche pas à trouver le "bon" poids pour des modèles existants, mais à créer un nouveau "type" de modèle agrégé qui explore une région différente de l'espace des hypothèses.   

3.3. Implications et Domaines d'Application

Les différences fondamentales entre le BMA et le Bagging se traduisent par des domaines d'application et des implications pratiques distincts.

Bayesian Model Averaging (BMA) :

Applications : Le BMA est particulièrement pertinent dans les domaines où une quantification rigoureuse de l'incertitude associée à la structure du modèle est cruciale, et où l'espace des modèles candidats peut être défini de manière sensée et gérable. Cela inclut souvent :
La sélection de variables en régression linéaire (où chaque modèle correspond à un sous-ensemble différent de prédicteurs).
Certains domaines scientifiques où l'on cherche à comparer des théories alternatives représentées par des modèles statistiques distincts.
Les contextes où les décisions ont des conséquences graves et où une compréhension probabiliste de l'incertitude du modèle est exigée.
Implications : L'utilisation du BMA nécessite généralement une expertise en statistiques bayésiennes. Bien que computationnellement exigeant, il peut fournir des informations précieuses non seulement sur les prédictions, mais aussi sur la plausibilité relative des différentes structures de modèles envisagées, aidant ainsi à l'inférence scientifique. La qualité des résultats dépendra fortement de la pertinence de l'ensemble des modèles considérés et de la validité des approximations utilisées pour la vraisemblance marginale.
Bagging :

Applications : Le Bagging est une technique d'application très large, en raison de sa simplicité et de son efficacité prouvée avec les apprenants instables. Il est couramment utilisé avec :
Les arbres de décision : C'est la base des Forêts Aléatoires (Random Forests), qui sont une extension du Bagging appliquant une randomisation supplémentaire au niveau de la sélection des caractéristiques à chaque nœud. Les Forêts Aléatoires sont parmi les algorithmes d'apprentissage automatique les plus performants et les plus utilisés pour une grande variété de tâches de classification et de régression.
Les réseaux de neurones : Le Bagging peut aider à stabiliser l'entraînement des réseaux de neurones et à améliorer leur généralisation.
D'autres modèles instables comme les classifieurs basés sur des règles.
Implications : Le Bagging est facile à implémenter et ne nécessite pas d'hypothèses fortes sur les données. Son principal avantage est l'amélioration de la précision et la réduction de la variance, ce qui le rend attrayant lorsque la performance prédictive brute est l'objectif principal. Cependant, il augmente l'opacité du modèle final (un ensemble de modèles est plus difficile à interpréter qu'un modèle unique), bien que des techniques existent pour extraire une importance des caractéristiques du modèle baggé.
En résumé, le BMA est une approche sophistiquée et théoriquement fondée pour la combinaison de modèles dans un cadre bayésien, idéale lorsque l'incertitude du modèle doit être quantifiée avec rigueur. Le Bagging est une méthode plus pragmatique et algorithmique, extrêmement efficace pour améliorer les performances des modèles instables par réduction de variance, et qui a trouvé une application très large, notamment à travers les forêts aléatoires.

Conclusion Générale

Ce rapport a exploré trois domaines fondamentaux de l'apprentissage automatique contemporain : l'interprétabilité des modèles, les systèmes de recommandation, et une comparaison des techniques d'ensemble BMA et Bagging. Chacun de ces domaines répond à des défis spécifiques et contribue à l'avancement et à l'application responsable de l'IA.

L'interprétabilité (XAI) s'est imposée comme une nécessité incontournable face à la complexité croissante des modèles d'AA, en particulier dans les secteurs à fort enjeu comme la santé et la finance. La distinction entre systèmes opaques, interprétables, compréhensibles et "véritablement explicables" illustre une quête de transparence et de communication accrues entre l'IA et l'humain. Des méthodes variées, qu'elles soient intrinsèques ou post-hoc, spécifiques ou agnostiques au modèle, locales ou globales (comme LIME, SHAP, ou l'analyse des arbres de décision et des règles), offrent une panoplie d'outils pour sonder les "boîtes noires". Le débat autour de la validité de l'attention comme explication souligne la complexité de cette tâche et la nécessité d'une évaluation rigoureuse, idéalement centrée sur l'humain, pour valider la qualité et l'utilité des explications produites. Les enjeux éthiques, tels que la confiance, la responsabilité et l'équité, ainsi que les cadres réglementaires émergents comme l'AI Act de l'UE, renforcent l'urgence de développer et d'adopter des pratiques d'XAI robustes.

Les systèmes de recommandation sont devenus des médiateurs essentiels de notre interaction avec l'information et les produits. Leur évolution, depuis le filtrage collaboratif traditionnel (basé sur l'utilisateur ou sur l'item) et le filtrage basé sur le contenu, jusqu'aux approches sophistiquées de factorisation de matrices (comme la SVD et ses dérivés) et plus récemment aux modèles basés sur l'apprentissage profond (NCF, GNNs, Transformers), témoigne d'une recherche constante d'amélioration de la pertinence et de la personnalisation. La comparaison détaillée entre le filtrage collaboratif basé sur l'utilisateur (UBCF) et la factorisation de matrices (MF) a mis en évidence les compromis entre l'intuitivité et la performance face à la sparsité des données. Alors que l'UBCF offre une explication plus directe des recommandations, la MF, grâce à sa capacité à modéliser des facteurs latents, tend à mieux gérer la sparsité et à offrir une meilleure précision. L'intégration croissante de contextes variés et de connaissances explicites (KBRS, CARS) montre une tendance vers des recommandations encore plus fines et adaptées.

Enfin, l'analyse comparative du Bayesian Model Averaging (BMA) et du Bagging a révélé deux philosophies distinctes pour l'amélioration des performances des modèles par l'agrégation. Le BMA, ancré dans la théorie bayésienne, offre une approche rigoureuse pour gérer l'incertitude du modèle en pondérant les prédictions selon la plausibilité a posteriori de chaque modèle. Sa complexité computationnelle reste cependant un frein majeur. Le Bagging, plus heuristique, améliore la stabilité et la précision des modèles instables par rééchantillonnage bootstrap et agrégation, avec un succès empirique notable, notamment pour les arbres de décision. L'interprétation de Domingos, suggérant que le Bagging modifie l'a priori implicite de l'apprenant vers des modèles plus complexes, offre un éclairage bayésien alternatif à son fonctionnement.

En synthèse, ces trois domaines, bien que distincts, convergent vers un objectif commun : rendre l'apprentissage automatique plus performant, plus fiable, plus compréhensible et plus aligné avec les attentes et les valeurs humaines. Les défis restent nombreux, qu'il s'agisse de développer des métriques d'interprétabilité universelles, de concevoir des systèmes de recommandation équitables et transparents, ou de mieux comprendre les fondements théoriques des méthodes d'ensemble les plus efficaces. La poursuite de la recherche dans ces directions est essentielle pour garantir que l'IA continue de progresser de manière bénéfique et responsable.




\documentclass[twocolumn, a4paper, 10pt]{article}

% --- PACKAGES ---
\usepackage[french]{babel}
\usepackage[utf8]{inputenc}
\usepackage[T1]{fontenc}
\usepackage{amsmath, amssymb, amsfonts} % Math packages
\usepackage{graphicx} % For images
\usepackage{hyperref} % For hyperlinks and PDF metadata
\usepackage{times} % Using Times font
\usepackage{multicol} % Already handled by twocolumn option, but good to know
\usepackage{lipsum} % For dummy text, remove in final version
\usepackage{geometry} % For page margins
\geometry{a4paper, top=2.5cm, bottom=2.5cm, left=2cm, right=2cm, columnsep=0.8cm}
\usepackage{natbib} % For APALIKE citations
\bibliographystyle{apalike}
\usepackage{sectsty} % To customize section titles
\usepackage{caption} % For figure and table captions
\usepackage{booktabs} % For professional quality tables
\usepackage{enumitem} % For customized lists
\usepackage{float} % For better control over float placement (figures, tables)
\usepackage{parskip} % To have space between paragraphs instead of indent

% --- DOCUMENT METADATA ---
\title{Analyse Approfondie de l'Interprétabilité en Apprentissage Automatique et des Systèmes de Recommandation}
\author{Votre Nom \\ Votre Institution \\ Votre Email}
\date{\today}

% --- CUSTOMIZATIONS ---
\sectionfont{\fontsize{12}{15}\selectfont\bfseries}
\subsectionfont{\fontsize{11}{14}\selectfont\bfseries}
\subsubsectionfont{\fontsize{10}{13}\selectfont\itshape}

% Hyphenation (optional, if you have specific words)
% \hyphenation{ma-chine lear-ning}

% --- BEGIN DOCUMENT ---
\begin{document}

\maketitle
\begin{abstract}
Ce rapport de niveau doctoral explore deux domaines cruciaux de l'apprentissage automatique contemporain : l'interprétabilité des modèles et les systèmes de recommandation. La première partie se penche sur la définition, l'évaluation, ainsi que les enjeux pratiques et éthiques de l'interprétabilité, en particulier dans les secteurs sensibles. Elle analyse les principales méthodes d'interprétabilité, leur fonctionnement, leurs applications, forces et limitations, en s'appuyant notamment sur les travaux de Doran et al. (2017) et Burkart & Huber (2021). La seconde partie introduit les systèmes de recommandation, leurs techniques fondamentales, et propose une comparaison détaillée de deux approches majeures, en se référant aux surveys comme celui de Ko et al. et aux avancées en filtrage collaboratif décrites par Koren & Bell. Ce document vise à fournir une synthèse analytique et critique, soulignant les défis actuels et les perspectives de recherche futures pour ces deux thématiques interdépendantes et en pleine évolution.
\end{abstract}

\tableofcontents
\newpage

% --- MAIN CONTENT ---

\section{Introduction Générale}
L'apprentissage automatique (AA) a révolutionné de nombreux domaines, offrant des capacités prédictives et décisionnelles sans précédent. Cependant, la complexité croissante des modèles, souvent qualifiés de "boîtes noires", soulève des questions fondamentales quant à leur transparence et leur fiabilité. Parallèlement, l'application de l'AA à la personnalisation de l'expérience utilisateur a conduit à l'essor des systèmes de recommandation, devenus omniprésents dans notre quotidien numérique.

Ce rapport aborde deux facettes essentielles de l'AA moderne. Premièrement, nous nous intéressons à l'interprétabilité (ou explicabilité) des modèles d'AA. Comprendre pourquoi un modèle prend une décision spécifique est non seulement crucial pour la validation et le débogage, mais aussi pour garantir l'équité, la responsabilité et la confiance, surtout dans des domaines à haut risque comme la médecine, la finance ou la justice. Nous explorerons les conceptualisations de l'interprétabilité et les diverses méthodes développées pour rendre les modèles plus transparents.

Deuxièmement, nous nous pencherons sur les systèmes de recommandation. Ces systèmes visent à prédire les préférences des utilisateurs et à leur suggérer des items pertinents (films, produits, articles, etc.). Leur efficacité repose sur des algorithmes sophistiqués qui analysent de vastes quantités de données. Nous présenterons un panorama des techniques existantes avant de comparer en détail deux approches significatives.

L'objectif de ce travail est de fournir une analyse approfondie et comparative de ces deux thématiques, en s'appuyant sur la littérature scientifique de référence, afin de dégager les enjeux actuels et les perspectives d'avenir.

% ------------------------------------------------------------------------------
\section{Partie I : Interprétabilité des Modèles d'Apprentissage Automatique}
% ------------------------------------------------------------------------------

\subsection{Problématique et Découverte de l'Interprétabilité}
L'adoption généralisée de modèles d'apprentissage automatique complexes, tels que les réseaux de neurones profonds ou les forêts aléatoires, a conduit à des performances remarquables. Néanmoins, cette performance s'accompagne souvent d'un manque de transparence. La "problématique de la boîte noire" se réfère à l'incapacité de comprendre facilement le raisonnement interne d'un modèle. Cette opacité pose plusieurs défis :
\begin{itemize}
    \item \textbf{Confiance et Adoption :} Les utilisateurs, en particulier dans les domaines critiques, hésitent à faire confiance à des décisions qu'ils ne comprennent pas.
    \item \textbf{Débogage et Amélioration :} Sans compréhension du fonctionnement interne, il est difficile d'identifier et de corriger les erreurs du modèle.
    \item \textbf{Équité et Biais :} Les modèles peuvent apprendre et perpétuer des biais présents dans les données, conduisant à des décisions discriminatoires. L'interprétabilité est essentielle pour détecter et atténuer ces biais.
    \item \textbf{Responsabilité et Réglementation :} En cas d'erreur du modèle ayant des conséquences graves, il est crucial de pouvoir déterminer la responsabilité. Des réglementations comme le RGPD en Europe introduisent un "droit à l'explication".
    \item \textbf{Découverte Scientifique :} Dans des domaines comme la biologie ou la médecine, l'interprétabilité peut aider à découvrir de nouvelles connaissances à partir des patterns identifiés par le modèle.
\end{itemize}
La "découverte" dans ce contexte se réfère à la prise de conscience progressive de ces enjeux et à l'émergence de l'interprétabilité (ou XAI - Explainable Artificial Intelligence) comme un champ de recherche majeur.

\subsection{État de l'Art en Interprétabilité}
La recherche en interprétabilité a produit une variété de définitions, de taxonomies et de méthodes.

\subsubsection{Conceptualisations de l'Interprétabilité}
\citet{Doran2017} proposent une conceptualisation de l'explicabilité en IA qui distingue différentes perspectives. Ils soulignent que ce qui constitue une "bonne" explication peut varier considérablement en fonction de l'audience (par exemple, un développeur de modèles vs un utilisateur final non expert) et du but de l'explication. Ils identifient des facettes telles que la transparence du modèle, la justification post-hoc, et la simulation du raisonnement.

\citet{Burkart2019} offrent un survey complet sur l'explicabilité des modèles d'apprentissage supervisé. Ils classifient les méthodes d'explicabilité selon plusieurs dimensions :
\begin{itemize}
    \item \textbf{Intrinsèque vs. Post-hoc :} L'interprétabilité intrinsèque est obtenue avec des modèles simples par conception (ex: arbres de décision, régression linéaire). Les méthodes post-hoc sont appliquées à des modèles déjà entraînés, souvent complexes.
    \item \textbf{Spécifique au modèle vs. Agnostique au modèle :} Les méthodes spécifiques ne fonctionnent qu'avec certains types de modèles (ex: attention pour les réseaux de neurones). Les méthodes agnostiques peuvent être appliquées à n'importe quel modèle (ex: LIME, SHAP).
    \item \textbf{Locale vs. Globale :} Les explications locales se concentrent sur une prédiction individuelle. Les explications globales visent à comprendre le comportement général du modèle.
\end{itemize}
Ils discutent également des différentes formes que peuvent prendre les explications (règles, caractéristiques importantes, exemples prototypiques, etc.).

\subsubsection{Principales Méthodes d'Interprétabilité}
Nous présentons ici quelques familles de méthodes, en nous inspirant des classifications de \citet{Burkart2019}.

\paragraph{Modèles Intrinsèquement Interprétables :}
Ces modèles sont transparents par nature.
\begin{itemize}
    \item \textbf{Régression Linéaire/Logistique :} Les coefficients indiquent l'importance et la direction de l'influence de chaque variable.
    \item \textbf{Arbres de Décision :} Le chemin de décision est une série de règles explicites.
    \item \textbf{Systèmes Basés sur des Règles :} (ex: Listes de règles, RIPPER).
\end{itemize}
Leur limitation principale est souvent une performance moindre sur des tâches complexes par rapport aux modèles "boîte noire".

\paragraph{Méthodes Agnostiques au Modèle (Post-hoc) :}
Ces méthodes traitent le modèle comme une boîte noire et tentent d'expliquer son comportement en observant ses entrées et sorties.
\begin{itemize}
    \item \textbf{LIME (Local Interpretable Model-agnostic Explanations) :} \citep{Ribeiro2016LIME} Explique une prédiction individuelle en approximant localement le modèle complexe par un modèle interprétable plus simple (ex: régression linéaire) sur des perturbations de l'instance d'origine.
        \begin{itemize}
            \item \textit{Fonctionnement :} Génère un voisinage de l'instance à expliquer, pèse ces voisins par leur proximité, entraîne un modèle interprétable sur ce voisinage pondéré.
            \item \textit{Domaines d'application :} Texte, image, données tabulaires.
            \item \textit{Forces :} Agnostique, facile à comprendre, explications locales intuitives.
            \item \textit{Limitations :} Stabilité des explications, définition de la "localité" et de la fonction de perturbation.
        \end{itemize}
    \item \textbf{SHAP (SHapley Additive exPlanations) :} \citep{Lundberg2017SHAP} Basé sur les valeurs de Shapley issues de la théorie des jeux coopératifs, SHAP attribue à chaque variable une valeur représentant sa contribution à la prédiction, en tenant compte des interactions.
        \begin{itemize}
            \item \textit{Fonctionnement :} Calcule les valeurs de Shapley pour chaque variable, garantissant des propriétés théoriques désirables (efficacité, symétrie, nullité, additivité).
            \item \textit{Domaines d'application :} Principalement données tabulaires, mais des adaptations existent pour images et textes.
            \item \textit{Forces :} Solides fondations théoriques, fournit des explications locales et globales cohérentes.
            \item \textit{Limitations :} Coût de calcul potentiellement élevé pour les modèles complexes et grand nombre de variables (bien que des approximations existent comme KernelSHAP ou TreeSHAP).
        \end{itemize}
    \item \textbf{Partial Dependence Plots (PDP) et Individual Conditional Expectation (ICE) Plots :} Visualisent l'effet marginal d'une ou deux variables sur la prédiction du modèle. PDP montre l'effet moyen, ICE montre l'effet pour chaque instance.
\end{itemize}

\paragraph{Méthodes Spécifiques au Modèle (Post-hoc) :}
Ces méthodes exploitent la structure interne de modèles particuliers.
\begin{itemize}
    \item \textbf{Importance des Variables dans les Forêts Aléatoires :} Mesurée par la diminution moyenne de l'impureté (Gini) ou la diminution moyenne de la précision (permutation).
    \item \textbf{Méthodes Basées sur les Gradients et l'Attention (pour les Réseaux de Neurones) :}
        \begin{itemize}
            \item \textit{Saliency Maps / Gradient-based :} Visualisent les pixels d'une image qui influencent le plus la sortie (ex: \citet{Simonyan2013Deep}).
            \item \textit{Attention Mechanisms :} Intrinsèques à certaines architectures (ex: Transformers), les poids d'attention peuvent indiquer quelles parties de l'entrée le modèle "regarde".
            \item \textit{CAM (Class Activation Mapping) et Grad-CAM :} Produisent des cartes de localisation des régions d'une image importantes pour une classe spécifique.
        \end{itemize}
\end{itemize}

\subsection{Méthodologie d'Évaluation de l'Interprétabilité}
Évaluer l'interprétabilité est un défi car elle est subjective et dépend du contexte. \citet{DoshiVelez2017Rigorous} plaident pour une évaluation rigoureuse. On distingue plusieurs niveaux d'évaluation :
\begin{itemize}
    \item \textbf{Application-grounded Evaluation :} Évaluation avec des experts du domaine dans une tâche réelle. C'est le plus coûteux mais le plus pertinent.
    \item \textbf{Human-grounded Evaluation :} Évaluation avec des humains (non experts ou experts simplifiés) sur des tâches simplifiées. Ex: Les humains peuvent-ils utiliser l'explication pour prédire le comportement du modèle ?
    \item \textbf{Functionally-grounded Evaluation :} Évaluation sans humains, en utilisant des proxies formels pour la qualité de l'explication (ex: fidélité au modèle, robustesse de l'explication).
\end{itemize}
Des métriques comme la fidélité (à quel point l'explication approxime bien le modèle), la compréhensibilité (l'explication est-elle facile à comprendre ?), la concision, la robustesse (des petites perturbations de l'entrée ne devraient pas changer radicalement l'explication) sont souvent utilisées.

\subsection{Résultats et Limitations des Méthodes Actuelles}
\paragraph{Résultats Positifs :}
\begin{itemize}
    \item Une panoplie de méthodes a été développée, offrant différents types d'explications pour divers modèles et types de données.
    \item Des outils comme LIME et SHAP ont gagné en popularité et sont largement utilisés en pratique.
    \item Prise de conscience accrue de l'importance de l'XAI dans la communauté AA et par les régulateurs.
\end{itemize}

\paragraph{Limitations Techniques et Conceptuelles :}
\begin{itemize}
    \item \textbf{Fidélité vs. Interprétabilité :} Il y a souvent un compromis. Une explication très simple peut ne pas être fidèle au modèle complexe.
    \item \textbf{Explications Trompeuses :} Des recherches ont montré que certaines explications peuvent être manipulées ou ne pas refléter le véritable raisonnement du modèle \citep{Adebayo2018Sanity}.
    \item \textbf{Manque de Consensus sur la Définition et l'Évaluation :} Ce qui constitue une "bonne" explication reste débattu.
    \item \textbf{Coût de Calcul :} Certaines méthodes (ex: SHAP exact) sont coûteuses.
    \item \textbf{Causalité vs. Corrélation :} La plupart des méthodes d'interprétabilité identifient des corrélations, pas nécessairement des relations causales. Une variable peut être importante pour la prédiction sans être la cause réelle.
    \item \textbf{Audience des Explications :} Les explications doivent être adaptées à l'utilisateur final, ce qui est rarement le cas avec les outils actuels qui sont souvent conçus pour des data scientists.
\end{itemize}

\subsection{Enjeux Pratiques et Éthiques}
L'interprétabilité est cruciale dans les domaines sensibles pour plusieurs raisons :
\begin{itemize}
    \item \textbf{Santé :} Comprendre pourquoi un modèle diagnostique une maladie, pour la confiance du médecin et du patient, et pour éviter des erreurs critiques.
    \item \textbf{Finance :} Expliquer les décisions de prêt ou de trading, pour la conformité réglementaire et l'équité.
    \item \textbf{Justice :} Justifier les évaluations de risque de récidive, pour éviter les biais discriminatoires et assurer un procès équitable.
    \item \textbf{Véhicules Autonomes :} Comprendre les décisions de conduite en cas d'incident.
\end{itemize}
Les enjeux éthiques incluent :
\begin{itemize}
    \item \textbf{Biais et Équité :} L'interprétabilité aide à détecter si un modèle discrimine certains groupes.
    \item \textbf{Responsabilité :} Qui est responsable si un modèle expliqué prend une mauvaise décision ?
    \item \textbf{Transparence vs. Propriété Intellectuelle :} Révéler le fonctionnement d'un modèle peut exposer des secrets commerciaux.
    \item \textbf{Manipulation :} Des explications peuvent être utilisées pour tromper les utilisateurs ou pour "jouer" avec le système.
\end{itemize}

\subsection{Futur Works et Perspectives en Interprétabilité}
\begin{itemize}
    \item Développement d'explications causales.
    \item Méthodes d'évaluation de l'interprétabilité plus robustes et standardisées.
    \item Explications interactives et adaptées à différents types d'utilisateurs.
    \item Intégration de l'interprétabilité dès la conception des modèles ("interpretable by design").
    \item Recherche sur la robustesse des explications face aux attaques adversariales.
    \item Cadres théoriques plus solides pour l'interprétabilité.
\end{itemize}

% ------------------------------------------------------------------------------
\section{Partie II : Systèmes de Recommandation}
% ------------------------------------------------------------------------------

\subsection{Problématique et Découverte des Systèmes de Recommandation}
Avec l'explosion du volume d'informations et de choix disponibles en ligne (produits, films, musique, actualités, etc.), les utilisateurs sont confrontés à une surcharge informationnelle. Les systèmes de recommandation (SR) ont émergé pour aider les utilisateurs à découvrir des items pertinents et personnalisés, améliorant ainsi l'expérience utilisateur et stimulant l'engagement et les ventes pour les entreprises.

La problématique centrale est de prédire les préférences futures d'un utilisateur pour des items qu'il n'a pas encore vus ou évalués, en se basant sur son historique d'interactions, ses caractéristiques, et potentiellement celles d'autres utilisateurs et items.

La "découverte" dans ce domaine a été marquée par des étapes clés, comme les premiers systèmes de filtrage collaboratif (Tapestry, GroupLens), l'essor du e-commerce, et des défis comme le Netflix Prize qui ont catalysé l'innovation.

\subsection{État de l'Art des Systèmes de Recommandation}
\citet{Ko2023Survey} (en supposant une publication récente, ou se référant à des surveys généraux comme \citet{Adomavicius2005Toward}) classifient les techniques de recommandation. Les approches principales incluent :

\begin{itemize}
    \item \textbf{Filtrage Collaboratif (Collaborative Filtering - CF) :}
    Cette approche se base sur l'idée que les utilisateurs qui ont eu des préférences similaires par le passé auront des préférences similaires à l'avenir.
    \begin{itemize}
        \item \textit{Memory-based (User-based et Item-based) :} Calcule les similarités entre utilisateurs ou items et fait des prédictions basées sur les évaluations des voisins les plus proches.
        \item \textit{Model-based :} Construit un modèle des préférences des utilisateurs (ex: factorisation de matrices, réseaux de neurones). \citet{Koren2009Advances} détaillent les avancées majeures en factorisation de matrices, notamment pour le Netflix Prize.
    \end{itemize}
    \item \textbf{Filtrage Basé sur le Contenu (Content-Based Filtering - CBF) :}
    Recommande des items similaires à ceux que l'utilisateur a aimés par le passé, en se basant sur les caractéristiques (attributs) des items et le profil de l'utilisateur.
    \item \textbf{Approches Hybrides :}
    Combinent plusieurs techniques (ex: CF et CBF) pour pallier les limitations de chaque approche individuelle et améliorer la performance.
    \item \textbf{Systèmes Basés sur la Connaissance (Knowledge-Based) :}
    Utilisent des connaissances explicites sur les items, les préférences utilisateurs et les critères de recommandation (ex: "Je cherche un appareil photo reflex pour moins de 500€").
    \item \textbf{Approches Contextuelles (Context-Aware) :}
    Prennent en compte le contexte de l'utilisateur (heure, lieu, humeur) pour affiner les recommandations.
    \item \textbf{Deep Learning for Recommendation :}
    Utilisation de réseaux de neurones profonds pour modéliser des relations complexes dans les données d'interaction (ex: Autoencoders, Recurrent Neural Networks, Graph Neural Networks).
\end{itemize}

\subsection{Analyse Détaillée et Comparaison de Deux Techniques}
Nous allons nous concentrer sur deux techniques fondamentales et largement utilisées : le **Filtrage Collaboratif Basé sur les Utilisateurs (User-Based CF)** et la **Factorisation de Matrices (MF)**, une méthode de Filtrage Collaboratif Basé sur des Modèles.

\subsubsection{Filtrage Collaboratif Basé sur les Utilisateurs (User-Based CF)}
\paragraph{Principe de Fonctionnement :}
\begin{enumerate}
    \item \textbf{Construction de la Matrice Utilisateur-Item :} Représente les évaluations (ratings) données par les utilisateurs aux items. C'est souvent une matrice creuse.
    \item \textbf{Calcul de Similarité entre Utilisateurs :} Pour un utilisateur actif $u$, on calcule sa similarité avec tous les autres utilisateurs. Les mesures de similarité courantes sont le cosinus, la corrélation de Pearson, ou la distance de Jaccard.
    $$ \text{sim}(u, v) = \frac{\sum_{i \in I_{uv}} (r_{ui} - \bar{r}_u)(r_{vi} - \bar{r}_v)}{\sqrt{\sum_{i \in I_{uv}} (r_{ui} - \bar{r}_u)^2} \sqrt{\sum_{i \in I_{uv}} (r_{vi} - \bar{r}_v)^2}} $$
    (Exemple : Corrélation de Pearson, où $I_{uv}$ est l'ensemble des items évalués à la fois par $u$ et $v$, $r_{ui}$ est l'évaluation de $u$ pour $i$, et $\bar{r}_u$ est l'évaluation moyenne de $u$).
    \item \textbf{Identification des Voisins (Neighborhood Selection) :} On sélectionne les $k$ utilisateurs les plus similaires à l'utilisateur actif (les "voisins").
    \item \textbf{Prédiction/Recommandation :} Pour prédire l'évaluation d'un item $j$ par l'utilisateur $u$, on agrège les évaluations de cet item $j$ par les voisins de $u$, souvent en pondérant par leur similarité.
    $$ \hat{r}_{uj} = \bar{r}_u + \frac{\sum_{v \in N_u} \text{sim}(u, v) \cdot (r_{vj} - \bar{r}_v)}{\sum_{v \in N_u} |\text{sim}(u, v)|} $$
    où $N_u$ est l'ensemble des voisins de $u$.
\end{enumerate}

\paragraph{Domaines d'Application Privilégiés :}
E-commerce, recommandation de films, musique, articles, où les interactions utilisateur-item sont abondantes.

\paragraph{Forces :}
\begin{itemize}
    \item Simple à comprendre et à implémenter.
    \item Pas besoin de connaître les caractéristiques des items.
    \item Capacité à générer des recommandations sérendipiteuses (items inattendus mais pertinents).
\end{itemize}

\paragraph{Limitations Techniques et Conceptuelles :}
\begin{itemize}
    \item \textbf{Sparsité des Données (Data Sparsity) :} La matrice utilisateur-item est souvent très creuse, ce qui rend difficile le calcul de similarités fiables.
    \item \textbf{Problème du Démarrage à Froid (Cold Start) :} Difficile de faire des recommandations pour de nouveaux utilisateurs (pas d'historique) ou de nouveaux items (pas d'évaluations).
    \item \textbf{Scalabilité :} Le calcul de similarité entre tous les paires d'utilisateurs peut être coûteux avec un grand nombre d'utilisateurs ($O(N^2 M)$ ou $O(N^2)$ avec optimisations, où N est le nb d'utilisateurs, M le nb d'items).
    \item \textbf{Synonymie et Popularity Bias :} Les items populaires tendent à être plus recommandés.
\end{itemize}

\subsubsection{Factorisation de Matrices (Matrix Factorization - MF)}
Cette technique, popularisée par le Netflix Prize \citep{Koren2009Advances}, est une méthode de filtrage collaboratif basé sur des modèles.

\paragraph{Principe de Fonctionnement :}
L'idée est de décomposer la matrice d'évaluations utilisateur-item $R$ (dimensions $N \times M$) en deux matrices de facteurs latents de plus faible dimension : une matrice $P$ (dimensions $N \times K$) représentant les utilisateurs et une matrice $Q$ (dimensions $M \times K$) représentant les items. $K$ est la dimension de l'espace latent (typiquement $K \ll N, M$).
Chaque utilisateur $u$ est représenté par un vecteur $p_u \in \mathbb{R}^K$ et chaque item $i$ par un vecteur $q_i \in \mathbb{R}^K$. L'évaluation prédite $\hat{r}_{ui}$ est simplement le produit scalaire de ces vecteurs :
$$ \hat{r}_{ui} = p_u^T q_i = \sum_{k=1}^K p_{uk} q_{ik} $$
Les vecteurs $p_u$ et $q_i$ sont appris en minimisant une fonction de coût sur les évaluations observées, souvent l'erreur quadratique regularisée :
$$ \min_{P,Q} \sum_{(u,i) \in \mathcal{K}} (r_{ui} - p_u^T q_i)^2 + \lambda (||p_u||^2 + ||q_i||^2) $$
où $\mathcal{K}$ est l'ensemble des paires $(u,i)$ pour lesquelles $r_{ui}$ est connue, et $\lambda$ est un terme de régularisation pour éviter le surapprentissage.
L'optimisation se fait typiquement par Descente de Gradient Stochastique (SGD) ou Alternating Least Squares (ALS).
Des biais peuvent être ajoutés : $\hat{r}_{ui} = \mu + b_u + b_i + p_u^T q_i$, où $\mu$ est la moyenne globale, $b_u$ le biais de l'utilisateur $u$, $b_i$ le biais de l'item $i$.

\paragraph{Domaines d'Application Privilégiés :}
Similaires au User-Based CF, mais souvent plus performants et scalables pour les grands jeux de données. Largement utilisé dans l'industrie.

\paragraph{Forces :}
\begin{itemize}
    \item \textbf{Meilleure Gestion de la Sparsité :} En apprenant des représentations latentes denses, MF peut mieux généraliser à partir des données éparses.
    \item \textbf{Scalabilité :} L'apprentissage peut être efficace (surtout avec SGD), et la prédiction est rapide ($O(K)$).
    \item \textbf{Performance :} Souvent plus précis que les méthodes memory-based.
    \item \textbf{Flexibilité :} Peut incorporer des informations implicites, des biais, des aspects temporels.
\end{itemize}

\paragraph{Limitations Techniques et Conceptuelles :}
\begin{itemize}
    \item \textbf{Problème du Démarrage à Froid :} Persiste, bien que des techniques d'intégration de contenu ou d'attributs puissent l'atténuer (factorisation hybride).
    \item \textbf{Interprétabilité des Facteurs Latents :} Les dimensions latentes $K$ n'ont pas toujours une signification sémantique claire, ce qui peut rendre le modèle moins interprétable que les approches basées sur les voisins.
    \item \textbf{Moins de Sérendipité :} Peut tendre à recommander des items plus "évidents" ou populaires si non géré.
    \item \textbf{Coût d'Entraînement :} Peut être significatif pour de très grands jeux de données, bien que des techniques d'optimisation existent.
\end{itemize}

\subsubsection{Tableau Comparatif}

\begin{table}[H]
\centering
\caption{Comparaison : User-Based CF vs. Factorisation de Matrices}
\label{tab:cf_vs_mf}
\begin{tabular}{@{}lll@{}}
\toprule
Caractéristique        & User-Based CF                        & Factorisation de Matrices         \\ \midrule
Approche             & Memory-based                         & Model-based                       \\
Gestion Sparsité     & Faible                               & Bonne                             \\
Scalabilité          & Limitée (surtout calcul similarité)  & Bonne (apprentissage et prédiction) \\
Performance          & Modérée                              & Élevée                            \\
Démarrage à Froid    & Problématique                        & Problématique (atténuable)        \\
Interprétabilité     & Relativement bonne (voisins)         & Faible (facteurs latents)         \\
Sérendipité          & Potentiellement élevée               & Modérée                           \\
Complexité Implém.   & Simple                               & Modérée                           \\
Données Utilisées    & Explicites (ratings)                 & Explicites, implicites (adaptable) \\ \bottomrule
\end{tabular}
\end{table}

\subsection{Méthodologie d'Évaluation des Systèmes de Recommandation}
L'évaluation est cruciale. On distingue :
\begin{itemize}
    \item \textbf{Évaluation Hors Ligne (Offline Evaluation) :}
    Utilise des jeux de données historiques. On divise les données en ensembles d'entraînement et de test.
    \begin{itemize}
        \item \textit{Métriques de Prédiction de Rating :} RMSE (Root Mean Squared Error), MAE (Mean Absolute Error).
        $$ \text{RMSE} = \sqrt{\frac{1}{|\mathcal{T}|} \sum_{(u,i) \in \mathcal{T}} (r_{ui} - \hat{r}_{ui})^2} $$
        où $\mathcal{T}$ est l'ensemble de test.
        \item \textit{Métriques de Classement (pour Top-N recommandations) :} Precision@k, Recall@k, MAP (Mean Average Precision), NDCG (Normalized Discounted Cumulative Gain).
    \end{itemize}
    \item \textbf{Évaluation en Ligne (Online Evaluation / A/B Testing) :}
    Déploie différentes versions du système à des groupes d'utilisateurs réels et mesure l'impact sur des métriques business (taux de clic, conversion, engagement, etc.). C'est l'évaluation la plus fiable.
    \item \textbf{Évaluation Utilisateur (User Studies) :}
    Collecte des retours qualitatifs des utilisateurs sur la qualité des recommandations (pertinence, nouveauté, diversité, sérendipité).
\end{itemize}
Il est important de considérer des aspects au-delà de la simple précision, comme la diversité, la nouveauté, la sérendipité, et l'équité des recommandations.

\subsection{Résultats et Limitations des Systèmes Actuels}
\paragraph{Résultats Positifs :}
\begin{itemize}
    \item Amélioration significative de l'engagement utilisateur et des revenus pour de nombreuses plateformes.
    \item Grande variété de techniques adaptées à différents contextes.
    \item Progrès constants grâce à l'AA et au deep learning.
\end{itemize}

\paragraph{Limitations :}
\begin{itemize}
    \item \textbf{Sparsité et Démarrage à Froid :} Restent des défis majeurs.
    \item \textbf{Scalabilité :} Pour des milliards d'utilisateurs et d'items.
    \item \textbf{Évaluation :} Les métriques hors ligne ne corrèlent pas toujours avec la satisfaction utilisateur en ligne.
    \item \textbf{Biais (Popularity Bias, Unfairness) :} Tendance à sur-recommander les items populaires et potentiellement à créer des bulles de filtres ou des discriminations.
    \item \textbf{Interprétabilité des Recommandations :} Pourquoi cet item m'est-il recommandé ? (Lien avec la Partie I).
    \item \textbf{Prise en Compte du Contexte et des Séquences d'Interaction.}
    \item \textbf{Sécurité et Vie Privée :} Utilisation de données personnelles sensibles.
\end{itemize}

\subsection{Futur Works et Perspectives en Systèmes de Recommandation}
\begin{itemize}
    \item Recommandations plus explicables et contrôlables par l'utilisateur.
    \item Meilleure gestion de l'équité, de la diversité et de la nouveauté.
    \item Systèmes de recommandation conversationnels et interactifs.
    \item Intégration de connaissances externes (graphes de connaissance).
    \item Approches fédérées ou décentralisées pour la protection de la vie privée.
    \item Modélisation plus fine des dynamiques temporelles et des intentions utilisateur.
\end{itemize}

% --- CONCLUSION AND BIBLIOGRAPHY ---
\section{Conclusion Générale et Perspectives Croisées}
L'interprétabilité des modèles d'apprentissage automatique et les systèmes de recommandation, bien que distincts, partagent des défis et des perspectives communs. L'opacité des modèles d'AA, y compris ceux utilisés dans les systèmes de recommandation sophistiqués, nécessite des avancées en XAI pour renforcer la confiance, l'équité et la robustesse. Inversement, rendre les recommandations explicables peut améliorer l'expérience utilisateur, permettre un meilleur contrôle et favoriser la découverte.

Les enjeux éthiques sont prégnants dans les deux domaines : biais algorithmiques, responsabilité, protection de la vie privée. Les travaux futurs devront s'attacher à développer des solutions techniques qui intègrent ces considérations dès la conception. La recherche d'un équilibre entre performance, interprétabilité, personnalisation et respect des valeurs éthiques constituera une ligne directrice majeure pour l'évolution de l'apprentissage automatique.

Ce rapport a tenté de synthétiser l'état de l'art, les méthodologies et les défis de ces deux thématiques. Il apparaît clairement que de nombreuses questions restent ouvertes, offrant un terrain fertile pour la recherche doctorale et au-delà, visant à construire des systèmes d'IA plus intelligents, mais aussi plus responsables et alignés avec les attentes sociétales.

\newpage
% --- BIBLIOGRAPHY ---
% The .bib file content should be placed in a separate file named "references.bib"
% and then included with the command \bibliography{references}
% For this example, I will embed the .bib content here for completeness.
% In a real scenario, you would create a references.bib file.

\begin{filecontents}{references.bib}
@article{Doran2017,
  author    = {Doran, Derek and Schulz, Sarah and Besold, Tarek R.},
  title     = {What Does Explainable AI Really Mean? A New Conceptualization of Perspectives},
  journal   = {arXiv preprint arXiv:1710.00794},
  year      = {2017},
  note      = {Presented at the IJCAI 2017 Workshop on Explainable AI (XAI)}
}

@article{Burkart2019,
  author    = {Burkart, Nico and Huber, Marco F.},
  title     = {A Survey on the Explainability of Supervised Machine Learning},
  journal   = {Journal of Artificial Intelligence Research},
  volume    = {70},
  pages     = {245--317},
  year      = {2021},
  doi       = {10.1613/jair.1.12228}
}

@inproceedings{Ko2023Survey,
  author    = {Ko, Hyeyoung and Lee, Suyeon and Park, Yoonseo and Choi, Anna},
  title     = {A Survey of Recommendation Systems: Recommendation Models, Techniques, and Application Fields},
  booktitle = {Proceedings of the Future Information Technology Conference (FutureTech)},
  year      = {2023},
  note      = {Note: This is a placeholder citation. The actual publication details might differ. A common general survey is Adomavicius & Tuzhilin (2005).}
}

@incollection{Koren2009Advances,
  author    = {Koren, Yehuda and Bell, Robert and Volinsky, Chris},
  title     = {Matrix Factorization Techniques for Recommender Systems},
  booktitle = {Recommender Systems Handbook},
  editor    = {Ricci, Francesco and Rokach, Lior and Shapira, Bracha and Kantor, Paul B.},
  publisher = {Springer US},
  year      = {2011},
  pages     = {141--182},
  doi       = {10.1007/978-0-387-85820-3_5},
  note      = {A more common citation for their work on Netflix Prize is IEEE Computer, 2009, "Matrix Factorization Techniques for Recommender Systems"}
}

@article{Domingos2012Few,
  author    = {Domingos, Pedro},
  title     = {A few useful things to know about machine learning},
  journal   = {Communications of the ACM},
  volume    = {55},
  number    = {10},
  pages     = {78--87},
  year      = {2012},
  doi       = {10.1145/2347736.2347755}
}

@techreport{Solomonoff1997Algorithmic,
  author    = {Solomonoff, Ray J.},
  title     = {Algorithmic Probability -- Theory and Applications},
  institution = {IDSIA},
  year      = {1997},
  note      = {This is a later overview; foundational papers are earlier, e.g., 1964.}
}

@article{Wasserman2000Bayesian,
  author    = {Wasserman, Larry},
  title     = {Bayesian model selection and model averaging},
  journal   = {Journal of Mathematical Psychology},
  volume    = {44},
  number    = {1},
  pages     = {92--107},
  year      = {2000},
  doi       = {10.1006/jmps.1999.1278}
}

@inproceedings{Domingos1997WhyBagging,
  author    = {Domingos, Pedro M.},
  title     = {Why Does Bagging Work? A Bayesian Account and Its Implications},
  booktitle = {Proceedings of the Third International Conference on Knowledge Discovery and Data Mining (KDD'97)},
  pages     = {155--158},
  year      = {1997},
  publisher = {AAAI Press}
}

@article{Ribeiro2016LIME,
  author    = {Ribeiro, Marco Tulio and Singh, Sameer and Guestrin, Carlos},
  title     = {"Why Should I Trust You?": Explaining the Predictions of Any Classifier},
  journal   = {arXiv preprint arXiv:1602.04938},
  year      = {2016},
  note      = {Published in KDD 2016}
}

@inproceedings{Lundberg2017SHAP,
  author    = {Lundberg, Scott M. and Lee, Su-In},
  title     = {A Unified Approach to Interpreting Model Predictions},
  booktitle = {Advances in Neural Information Processing Systems 30 (NIPS 2017)},
  pages     = {4765--4774},
  year      = {2017}
}

@inproceedings{Simonyan2013Deep,
  author    = {Simonyan, Karen and Vedaldi, Andrea and Zisserman, Andrew},
  title     = {Deep Inside Convolutional Networks: Visualising Image Classification Models and Saliency Maps},
  booktitle = {Proceedings of the International Conference on Learning Representations (ICLR) Workshop},
  year      = {2014},
  note      = {arXiv preprint arXiv:1312.6034, 2013}
}

@article{DoshiVelez2017Rigorous,
  author    = {Doshi-Velez, Finale and Kim, Been},
  title     = {Towards A Rigorous Science of Interpretable Machine Learning},
  journal   = {arXiv preprint arXiv:1702.08608},
  year      = {2017},
  note      = {NIPS 2017 Workshop on Interpretable ML}
}

@inproceedings{Adebayo2018Sanity,
  author    = {Adebayo, Julius and Gilmer, Justin and Muelly, Michael and Goodfellow, Ian and Hardt, Moritz and Kim, Been},
  title     = {Sanity Checks for Saliency Maps},
  booktitle = {Advances in Neural Information Processing Systems 31 (NeurIPS 2018)},
  pages     = {9505--9515},
  year      = {2018}
}

@article{Adomavicius2005Toward,
  author    = {Adomavicius, Gediminas and Tuzhilin, Alexander},
  title     = {Toward the Next Generation of Recommender Systems: A Survey of the State-of-the-Art and Possible Extensions},
  journal   = {IEEE Transactions on Knowledge and Data Engineering},
  volume    = {17},
  number    = {6},
  pages     = {734--749},
  year      = {2005},
  doi       = {10.1109/TKDE.2005.99}
}

\end{filecontents}

\bibliography{references} % This command uses the .bib file

\end{document}
