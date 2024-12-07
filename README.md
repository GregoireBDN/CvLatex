# CV LaTeX - Grégoire BODIN

Ce dépôt contient mon CV professionnel créé avec LaTeX. Le CV est entièrement personnalisable et utilise une mise en page moderne.

## Prérequis

Pour modifier et compiler ce CV, vous aurez besoin des éléments suivants :

### Windows

1. Installez MiKTeX (distribution LaTeX) :
   - Téléchargez depuis [miktex.org](https://miktex.org/download)
   - Suivez l'assistant d'installation
2. Installez un éditeur LaTeX (au choix) :
   - TeXmaker : [texmaker.org](https://www.xm1math.net/texmaker/)
   - TeXstudio : [texstudio.org](https://www.texstudio.org/)
   - VS Code avec l'extension LaTeX Workshop

### Linux

```bash
# Ubuntu/Debian
sudo apt-get install texlive-full
sudo apt-get install texmaker

# Fedora
sudo dnf install texlive-scheme-full
sudo dnf install texmaker

# Arch Linux
sudo pacman -S texlive-most
sudo pacman -S texmaker
```

### macOS

1. Installez MacTeX :
   - Téléchargez depuis [tug.org/mactex](https://tug.org/mactex/)
   - Ou via Homebrew : `brew install --cask mactex`
2. Installez un éditeur LaTeX :
   - TeXmaker : `brew install --cask texmaker`
   - VS Code avec LaTeX Workshop : `brew install --cask visual-studio-code`

## Packages LaTeX requis

Les packages suivants sont nécessaires (normalement inclus dans les distributions complètes) :

- geometry - Pour la mise en page et les marges
- titlesec - Pour personnaliser les titres de section
- tabularx - Pour les tableaux à largeur fixe
- xcolor - Pour la coloration du texte
- enumitem - Pour personnaliser les listes
- fontawesome5 - Pour les icônes
- hyperref - Pour les liens et métadonnées
- eso-pic - Pour le texte flottant
- paracol - Pour la mise en page multi-colonnes
- sourcesanspro - Pour la police principale

## Compilation

1. Clonez le dépôt :

```bash
git clone https://github.com/GregoireBDN/cv-latex.git
cd cv-latex
```

2. Compilez le CV :

- Avec un éditeur LaTeX : ouvrez `CV.tex` et utilisez le bouton de compilation
- En ligne de commande :

```bash
# Compilation simple
pdflatex CV.tex

# Compilation complète (recommandée)
pdflatex CV.tex
pdflatex CV.tex  # Deuxième passage pour les références
```

Le fichier PDF sera généré dans le même dossier.

## Personnalisation

Le CV peut être personnalisé en modifiant :

### Informations personnelles

- Nom, titre et coordonnées dans la section `header`
- Photo de profil (optionnelle)

### Contenu

- Sections Formation, Expérience, et Compétences
- Ordre et titres des sections

### Style

- Couleurs via `\definecolor{primaryColor}`
- Mise en page via les paramètres de `geometry`
- Police et taille de texte
- Espacement et marges

## Structure des fichiers

```
.
├── CV.tex          # Fichier source principal
├── CV.pdf          # CV compilé
├── .gitignore      # Fichiers à ignorer par Git
└── README.md       # Documentation
```

## Résolution des problèmes courants

### Erreurs de compilation

- Vérifiez que tous les packages sont installés
- Exécutez `pdflatex` deux fois
- Consultez le fichier `.log` pour les messages d'erreur

### Problèmes de police

- Assurez-vous que `fontawesome5` est installé
- Pour Linux : `sudo apt-get install texlive-fonts-extra`
