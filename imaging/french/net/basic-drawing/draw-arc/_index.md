---
date: 2026-02-09
description: Apprenez à tracer un arc avec Aspose.Imaging pour .NET, y compris comment
  enregistrer un fichier BMP, définir la taille de l'image et définir l'arrière‑plan
  graphique. Guide étape par étape pour générer des images BMP.
linktitle: Draw Arc in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: Comment tracer un arc avec Aspose.Imaging pour .NET
url: /fr/net/basic-drawing/draw-arc/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Comment tracer un arc avec Aspose.Imaging pour .NET

Dans le domaine du traitement d'images, **how to draw arc** est une tâche courante qui peut ajouter du style visuel à n'importe quel graphique. Avec Aspose.Imaging pour .NET, vous pouvez générer des images BMP, définir la taille de l'image et tracer un arc avec un crayon en quelques lignes de C#. À la fin de ce tutoriel, vous saurez exactement comment tracer un arc, définir le fond graphique et enregistrer le fichier BMP résultant sans effort.

## Réponses rapides
- **Quel est le résultat du code ?** Une image BMP de 100 × 100 pixels avec un fond jaune et un arc noir.  
- **Quelle bibliothèque est utilisée ?** Aspose.Imaging pour .NET.  
- **Ai‑je besoin d’une licence ?** Un essai gratuit suffit pour le développement ; une licence commerciale est requise en production.  
- **Puis‑je modifier la taille de l’image ?** Oui – modifiez les paramètres `width` et `height` dans l’appel `Image.Create`.  
- **Le format de sortie est‑il fixe ?** L’exemple enregistre un fichier BMP, mais tout format supporté par Aspose.Imaging peut être utilisé.

## Qu’est‑ce que « how to draw arc » dans Aspose.Imaging ?
Tracer un arc signifie rendre un segment de ligne courbe défini par un rectangle englobant, un angle de départ et un angle d’extension. Aspose.Imaging fournit la méthode `Graphics.DrawArc`, qui vous permet **draw arc with pen** et de contrôler chaque aspect visuel.

## Pourquoi utiliser Aspose.Imaging pour cette tâche ?
- **Contrôle total** sur les dimensions de l'image, la profondeur de couleur et le format de fichier.  
- **Aucune dépendance externe** – tout fonctionne sur du .NET pur.  
- **Haute performance** pour générer un grand nombre de graphiques côté serveur.  

## Prérequis

Avant de plonger dans le code, assurez‑vous de disposer de ce qui suit :

1. **Aspose.Imaging pour .NET** – téléchargez‑le depuis le site officiel [here](https://releases.aspose.com/imaging/net/).  
2. **Un environnement de développement .NET** (Visual Studio, VS Code ou tout compilateur C#).  

Maintenant que nos prérequis sont prêts, commençons à dessiner !

## Importation des espaces de noms nécessaires

Pour travailler avec Aspose.Imaging, vous devez importer les espaces de noms pertinents :

### Étape 1 : Importer les espaces de noms

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.FileFormats.Bmp;
using Aspose.Imaging.Sources;
using System;
using System.Drawing;
using System.IO;
```

Ces instructions `using` vous donnent accès aux classes de création d'images, de gestion graphique et d'E/S de fichiers.

## Comment tracer un arc avec Aspose.Imaging pour .NET

Nous allons diviser le processus en trois étapes claires : créer l'image, préparer la surface graphique et enfin tracer l'arc.

### Étape 1 : Configurer l’image (définir la taille de l’image & générer une image BMP)

```csharp
// Specify the directory where you want to save the image
string dataDir = "Your Document Directory";

// Create an instance of FileStream to save the image
using (FileStream stream = new FileStream(dataDir + "DrawingArc_out.bmp", FileMode.Create))
{
    // Create an instance of BmpOptions and set its properties
    BmpOptions saveOptions = new BmpOptions();
    saveOptions.BitsPerPixel = 32;

    // Set the source for BmpOptions and create an instance of Image
    saveOptions.Source = new StreamSource(stream);
    using (Image image = Image.Create(saveOptions, 100, 100))
    {
```

Ici, nous **set image size** à 100 × 100 pixels et configurons les options BMP. Le `FileStream` garantit que nous **save BMP file** à l'emplacement souhaité.

### Étape 2 : Initialiser Graphics et définir le fond graphique

```csharp
        // Create and initialize an instance of Graphics class and clear the graphics surface
        Graphics graphic = new Graphics(image);
        graphic.Clear(Color.Yellow);
```

L'objet `Graphics` nous permet de peindre sur l'image. En appelant `Clear(Color.Yellow)` nous **set graphics background** à un jaune vif, faisant ressortir l'arc.

### Étape 3 : Définir les paramètres de l’arc et tracer l’arc avec un crayon

```csharp
        // Define the parameters for the arc
        int width = 100;
        int height = 200;
        int startAngle = 45;
        int sweepAngle = 270;

        // Draw the arc
        graphic.DrawArc(new Pen(Color.Black), 0, 0, width, height, startAngle, sweepAngle);

        // Save the changes
        image.Save();
    }
    stream.Close();
}
```

- `width` et `height` définissent le rectangle englobant, définissant effectivement **set image size** pour l'arc.  
- L'objet `Pen` est ce qui nous permet **draw arc with pen** en noir.  
- Après le tracé, `image.Save()` écrit le **BMP file** sur le disque.

## Problèmes courants & conseils

- **Arc invisible ?** Assurez‑vous que la couleur du crayon contraste avec le fond (par ex., noir sur jaune).  
- **Dimensions incorrectes ?** N'oubliez pas que le rectangle englobant de l'arc peut être plus grand que l'image ; ajustez `width`/`height` ou la taille de l'image en conséquence.  
- **Conseil de performance :** Réutilisez une seule instance `Graphics` si vous devez tracer plusieurs formes sur la même image.

## FAQ

### Q1 : Où puis‑je trouver la documentation d’Aspose.Imaging pour .NET ?

R1 : Vous pouvez consulter la documentation [here](https://reference.aspose.com/imaging/net/) pour des informations complètes sur Aspose.Imaging pour .NET.

### Q2 : Comment télécharger Aspose.Imaging pour .NET ?

R2 : Vous pouvez télécharger Aspose.Imaging pour .NET depuis le site web [here](https://releases.aspose.com/imaging/net/).

### Q3 : Existe‑t‑il une version d’essai gratuite d’Aspose.Imaging pour .NET ?

R3 : Oui, vous pouvez obtenir une version d’essai gratuite [here](https://releases.aspose.com/) pour essayer Aspose.Imaging pour .NET.

### Q4 : Ai‑je besoin d’une licence temporaire pour Aspose.Imaging pour .NET ?

R4 : Si vous avez besoin d’une licence temporaire, vous pouvez en obtenir une [here](https://purchase.aspose.com/temporary-license/).

### Q5 : Où puis‑je obtenir du support ou poser des questions sur Aspose.Imaging pour .NET ?

R5 : Vous pouvez visiter le forum Aspose.Imaging pour le support et les discussions [here](https://forum.aspose.com/).

---

**Dernière mise à jour :** 2026-02-09  
**Testé avec :** Aspose.Imaging 24.11 pour .NET  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}