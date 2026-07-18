# ZéNí — Résumé en français

> ZéNí existe parce que le prochain problème de l'IA n'est plus seulement l'intelligence.
> C'est de rendre l'intelligence **utilisable, coordonnée et digne de confiance dans le travail réel.**

Ce dépôt est la **maison éditoriale publique** de ZéNí. Il existe pour aider les visiteurs — développeurs curieux, partenaires potentiels, journalistes, étudiants, investisseurs — à comprendre la vision, le positionnement et les matériaux publics de ZéNí. Ce résumé en français est conçu pour être autonome : en le lisant, vous repartirez avec une compréhension claire de ce qu'est ZéNí, du problème qu'il adresse, et de pourquoi il intervient à un moment pivot du développement de l'IA.

---

## Le positionnement, en une phrase

**ZéNí vise à rendre l'intelligence opérable — coordonnée, visible, gouvernée, et utilisable dans le travail réel.**

---

## Le problème que ZéNí aborde

Pendant une décennie, l'industrie de l'IA a traité le modèle comme le produit. Plus de paramètres, de meilleurs scores de benchmark, des démos plus impressionnantes — chaque génération de modèle a été présentée comme la destination.

Ce n'est pas la destination. Ça ne l'a jamais été.

Le modèle est un **moteur**. Nécessaire, coûteux, remarquable. Mais un moteur sans châssis, sans direction, sans freins, sans tableau de bord et sans route n'est pas une voiture — c'est une pièce de musée.

Le châssis manque. Nous le construisons.

Plus précisément : la **couche de coordination** qui transforme des modèles isolés en agents responsables, gouvernés, composables. Cette couche reste à structurer : de nombreux projets résolvent une partie du problème, mais aucun modèle opérationnel commun ne s'est imposé.

---

## Les concepts clés

### IA agentique

Pas un meilleur chatbot. Un système **qui agit**.

Un chatbot complète un tour de conversation. Un agent complète un flux de travail. La différence n'est pas cosmétique mais structurelle : un agent doit pouvoir prendre un but qu'il n'a pas formulé lui-même, décider de ses étapes intermédiaires, mobiliser des outils ou d'autres systèmes, et produire un résultat auditable.

Cela impose trois exigences que la plupart des démos "agentiques" actuelles éludent :

1. **Une description structurée de l'intention** — traduire "ce que veut l'utilisateur" en une spécification que des systèmes machine peuvent acheminer.
2. **Une théorie de qui d'autre existe** — un agent isolé peut répondre à des questions ; un agent dans un flux réel doit savoir quels autres agents, outils ou services sont accessibles, à quel coût, sous quelles contraintes.
3. **Une trace de ce qui s'est passé** — sans un journal vérifiable, l'IA agentique ne peut pas opérer dans des contextes sérieux. Conformité, débogage, amélioration des modèles, confiance des opérateurs en dépendent tous.

### Le Web Agentique

Le web a été conçu pour les humains. Les API ont été conçues pour des appelants qui attendent. Aucun des deux n'a été conçu pour des agents autonomes qui se découvrent mutuellement, négocient un travail, et laissent des reçus.

Le Web Agentique est le nom de cette couche d'infrastructure manquante. Elle exige :

- des **registres de capacités** indexant ce que les systèmes peuvent faire (et pas seulement où ils résident) ;
- des **identités signées** et des **attestations cryptographiques** au niveau du protocole, pas du logiciel applicatif ;
- des **invocations contraintes par des politiques** — chaque appel porte son budget, son jeton d'approbation, ses exigences de preuve ;
- des **locations de compétences** au lieu de possessions permanentes — les capacités sont prises en location pour une tâche puis libérées ;
- des **reçus par défaut** — chaque échange conséquent laisse une trace cryptographiquement chaînée ;
- une **allocation de modèles gouvernée** — le choix du modèle pour chaque étape est lui-même une décision auditable.

### MCP — Model Context Protocol

MCP est un protocole ouvert qui relie les applications d'IA à des systèmes externes. Un hôte établit des connexions clientes avec des serveurs qui peuvent exposer des outils, des ressources et des prompts réutilisables au moyen d'une interface commune.

MCP est l'**écartement de rail** de l'ère agentique. Ce n'est pas la locomotive — mais chaque train qui sera construit ensuite roulera dessus.

MCP a délibérément choisi de ne pas résoudre l'autorisation, la preuve, la découverte, la gouvernance des coûts, ni l'allocation de modèles. Cette retenue est ce qui rend le protocole adoptable. Mais cela signifie aussi que **MCP est nécessaire et non suffisant** : il faut une couche au-dessus.

C'est cette couche que ZéNí construit.

### Coordination, gouvernance, preuve, supervision humaine

Une IA digne de confiance dans le travail réel suppose quatre propriétés structurelles, pas optionnelles :

- **Coordination** — comment plusieurs systèmes se mettent d'accord pour atteindre un objectif commun ;
- **Gouvernance** — qui décide de ce qui est autorisé, par qui, sous quelles conditions ;
- **Preuve** — un enregistrement structuré, vérifiable et chaîné de ce qui s'est passé ;
- **Supervision humaine** — la capacité pour un opérateur d'inspecter, d'intervenir, d'approuver ou d'arrêter à n'importe quel moment.

Aucune de ces propriétés ne peut être ajoutée après coup. Soit le système les possède par conception, soit il ne les a pas.

---

## Pourquoi maintenant, pourquoi ZéNí

L'argument en trois étapes :

1. **Le modèle se banalise.** L'écart entre les meilleurs modèles fermés et ouverts se rétrécit chaque trimestre. Le modèle est en train de devenir le substrat, non plus le produit.
2. **La valeur remonte vers la couche opérationnelle.** Chaque transition de plateforme des quarante dernières années s'est jouée à la **couche immédiatement au-dessus** du substrat qui se banalisait. PC → systèmes d'exploitation. OS → navigateur. Navigateur → plateforme applicative. Plateforme applicative → SaaS. Cette fois : modèles → couche de coordination.
3. **La couche de coordination reste à structurer.** De nombreux acteurs en construisent des parties, mais la découverte, le routage, la gouvernance et la preuve ne sont pas encore réunis dans un modèle opérationnel commun.

ZéNí a commencé par le bon problème — la coordination, la confiance, la preuve — et non par un chatbot qu'il faudrait "agentifier" plus tard. Les décisions architecturales qui découlent de ce point de départ (la politique comme service back-end de première classe, MCP comme surface réelle d'interopérabilité, les reçus signés par défaut, l'allocation de modèles gouvernée) ne sont pas des ajouts — elles sont l'ossature.

---

## Ce que ce dépôt contient et ce qu'il ne contient pas

Ce dépôt est la **face publique** de ZéNí. C'est un artefact d'éducation, de positionnement et de contexte public.

Il contient : des essais sur l'IA agentique, le Web agentique, MCP ; un manifeste ; un glossaire et une FAQ ; les coordonnées de la fondatrice. Tout ce qui s'y trouve est conçu pour être citable, partageable, et utile à un visiteur qui veut comprendre.

Les systèmes produits et la couche éditoriale publique évoluent en parallèle. Ce dépôt se concentre sur l'éducation, le positionnement, le contexte public et les matériaux publics actuels.

**État actuel :** ZéNí est en préparation active de pilotes. Les surfaces produit connectées sont déployées, mais le système n'est pas disponible de manière générale. L'accent porte sur une utilisation structurée avec des opérateurs de startups.

---

## La fondatrice et contact

**Kelisi Ananke** — fondatrice unique. Harvard Master in Design Engineering. Basée à Cambridge, USA.

- LinkedIn : <https://www.linkedin.com/in/kelisi/>
- GitHub : <https://github.com/Kelisi808>

Pour toute prise de contact — investissement, pilote, partenariat, presse — passer par les canaux ci-dessus avec une note courte indiquant la nature de la conversation.

---

## Pour aller plus loin

Les essais complets en anglais se trouvent dans le dépôt :

- **[MANIFESTO.md](../MANIFESTO.md)** — le manifeste complet
- **[AGENTIC_AI.md](../AGENTIC_AI.md)** — IA agentique en profondeur
- **[AGENTIC_WEB.md](../AGENTIC_WEB.md)** — Web agentique en profondeur
- **[WHY_MCP_MATTERS.md](../WHY_MCP_MATTERS.md)** — pourquoi MCP compte
- **[WHY_ZENI.md](../WHY_ZENI.md)** — pourquoi ZéNí, pourquoi maintenant
- **[GLOSSARY.md](../GLOSSARY.md)** — glossaire
- **[FAQ.md](../FAQ.md)** — questions fréquentes
- **[Présentation éditoriale publique](../Z%C3%A9N%C3%AD%20Pitch%20Deck.html)** — l'introduction à lire dans le navigateur

> _« La prochaine question importante en IA n'est plus l'intelligence.
> C'est de rendre l'intelligence utilisable, coordonnée et digne de confiance dans le travail réel. »_
