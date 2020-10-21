% Markdown: quoi? pourquoi? comment?
% Atelier présenté pour les *Chercheuses badass*
% 21 octobre 2020

---

# Plan de l'atelier
1. **Quoi?**: L'idée derrière Markdown
2. **Comment?**: La *syntaxe* Markdown
3. **Pourquoi?**: Mon utilisation de MD

---

# Qu'est-ce que Markdown
- langage de **balisage** (*markup language*)
	- langage de balisage **léger** (*lightweight*)
- créé en 2004 (John Gruber et Aaron Swartz)
- caractéristiques:
	- facilité
	- lisibilité
	- (ex)portabilité

---

# Qu'est-ce que c'est?

## Ce que je veux:
- métadonnées du titre (Hola), sur l'autrice (Emilie Drouin) de la page et la date (Octobre 2020)
- Une ligne de texte avec de l'*italique* et du **gras**

## Ce que j'écris en markdown:

    % Hola
    % Emilie Drouin
    % Octobre 2020
    *Hola!* Mon nom est **Emilie**.

ou même, si l'on n'a pas besoin des métadonnées (titre, autrice, date):

    *Hola!* Mon nom est **Emilie**.

## Ce que j'obtiens:

*Hola!* Mon nom est **Emilie**.

---

# Qu'est-ce que ce n'est pas...

Ce n'est ni du HTML, ni LaTeX, qui sont d'autres langages de balisage.

## Ce n'est pas du HTML

Pour obtenir "*Hola!* Mon nom est **Emilie**.":

	<html>
		<head>
			<title>Hola</title>
			<meta name="author" content="Emilie Drouin">
			<meta name="date" content="Octobre 2020">
		</head>
		<body>
			<p><i>Hola!</i> Mon nom est <b>Emilie</b>.</p>
		</body>
	</html>

HTML est conçu pour le web.

---

## Ce n'est pas LaTeX

Pour obtenir "*Hola!* Mon nom est **Emilie**.":

    \documentclass{article}
    \title{Hola}
    \author{Emilie Drouin}
    \date{Octobre 2020}
    \begin{document}
       \maketitle
       \textit{Hola!} Mon nom est \textbf{Emilie}.
    \end{document}

LaTeX est beaucoup utilisé pour la rédaction (articles, livres, thèses) orientée vers une publication par impression (papier ou écran, par exemple PDF).

---

# Pis Word?????????? Ça va tellement bien Word!!

Liberté et indépendance

---

## Liberté
- la question du "libre"
	- le *par* et *pour* la communauté
	- accès libre (*open access*) en publication savante... et ensuite?
	- informatique libre
		- logiciels libres, gratuits, propriétaires???
			- propriétaire = Endnote (Clarivate Analytics), Mendeley (acheté par Elsevier); Word (Microsoft), Pages (Apple), Google Doc (Google); Internet Explorer (Microsoft), Safari (Apple), Chrome (Google); Windows (Microsoft); macOS et iOS (Apple\*); Android (Google\*)
			- libre = Zotero; LibreOffice; Firefox (Mozilla Foundation); Noyau Linux
		- LibreOffice comme alternative (libre) à Word

---

## Indépendance
- la question des outils et des formats
	- les formats
		- .docx
		- .odt
		- .txt
		- .md
		- ...
	- les outils
		- la dépendance aux outils
		- l'interopérabilité (compatibilité/portabilité)

---

## Dans les entrailles d'un .docx

![Comparaison entre l'interface de LibreOffice et le xml extrait du même un .docx.](Images/docx.png)

---

## Dans les entrailles d'une recette.md

![Comparaison entre la syntaxe Markdown et le document produit](Images/croustade.png)

---

## Retour sur les caractéristiques de Markdown

1. facilité
	- facile à écrire, facile à lire
2. simplicité
	- juste le nécessaire: repérage (titres), organisation (listes)
3. (ex)portabilité
	- lisible en l'état (en plein texte - *plain text*); ne requiert pas d'outil (logiciel) spécifique

---

## Hein?? pas d'outil spécifique?

Markdown est une **syntaxe** qui ne dépend pas d'un logiciel, ni pour l'écriture, ni pour la lecture (car il est **lisible en l'état**, c'est-à-dire que la **syntaxe** est si **légère** qu'elle n'interfère pas lors de la lecture humaine).

### On écrit/lit ça où, du Markdown?
- éditeurs plein-texte (format: .txt) ou des éditeurs de texte génériques
  - de base dans chaque système d'exploitation (*OS*): Bloc-notes / *Notepad* (Microsoft), TextEdit (Apple), gedit (de base dans Linux mais multi plate-forme)
  - plus complets et plus complexes: Atom (libre, multi plate-forme), NotePad++ (libre, pour Windows), Sublime Texte (propriétaire, multi plate-forme)
  - ultra léger: Geany (libre, multi plate-forme)
- éditeurs Markdown (format: .md)
	- *parser* (analyseurs syntaxiques)
	- outils plus complexes et plus puissants

---

## Des formats et des outils: langages et éditeurs
![Distinguer Markdown du *plain text*, et les éditeurs plein-texte des éditeurs Markdown](Images/markdown_vs_plaintext.png)

---

# "Que tu le manges avec une fourchette ou une cuillère, l'important, ce n'est pas l'ustensile, c'est le gâteau!"

-\ moi-même



AH. Alors il y en a, des outils! Oui, mais le fichier Markdown ***n'en dépend pas***; il est aussi lisible *à l'extérieur* de ces outils (logiciels), et à l'inverse, il peut être écrit hors du logiciel puis lu (*parsé*, interprété) à l'intérieur.

Bénéfices de cette indépendance face aux outils: changement d'*OS* (Windows <-> Mac <-> Linux); partage d'un fichier ou co-écriture inter-OS; pérennité!

---

# La syntaxe Markdown


## Qu'est-ce que Markdown permet?

Markdown permet un certain degré de mise en forme très facile à faire *on the fly*: gras, italique, titres et sous-titres, listes à puces.

---

### Emphase
*Italique*: ``*italique*`` ou ``_italique_`` (1 underscore)  
**Gras**: ``**gras**`` ou ``__gras__`` (2 underscores)  
***Gras et Italique***: ``***gras-italique***`` ou ``___gras-italique___`` (3 underscores)  

### Niveaux de titres (*Headings*)
Titre 1: ``# Titre 1``  
Titre 2: ``## Titre 2``  
Titre 6: ``###### Titre 6``  

- relève d'un balisage **sémantique**
	- on ne demande pas une *apparence* précise (taille 16, caractère gras!); plutôt, on indique de quel niveau de titre ça relève (autrement dit, le *sens* ou la *fonction* de ce contenu)
	- semblable aux Titres dans Word/LibreOffice (mais beaucoup plus rapide/facile à taper!)

### Listes à puces
- listes numérotées:
	- utiliser des chiffres (``1.``, ``2.``...)
	- les chiffres indentés (en utilisant une tabulation, et recommençant la numérotation) deviendront des sous-points
- listes non-ordonnées:
	- en utilisant des symboles: tiret (``-``), astérisque (``*``) ou signe d'addition (``+``)

### Mise en page
- Changement de paragraphe: laisser une ligne vide  
- Retour à la ligne (sans changer de paragraphe): terminer une ligne par un double espacement *forcera* le retour à la ligne
- Utiliser un caractère qui donnerait autrement du code: mettre un backslash (``\``) avant
- ###### Quand tu ~~corrige ton erreur~~ changes d'idée: ``~~barré~~``