---
date: '2026-02-09'
description: Apprenez à convertir des JPEG en TIFF et à créer des images TIFF multi‑cadres
  à l'aide d'Aspose.Imaging pour .NET. Comprend la mise en place, la configuration
  de TiffOptions, le chargement d'images depuis un répertoire et la gestion des cadres.
keywords:
- create multi-frame tiff images
- Aspose.Imaging for .NET tutorial
- configure TiffOptions in .NET
title: Comment convertir JPEG en TIFF et créer des images TIFF multi‑cadres avec Aspose.Imaging
  pour .NET
url: /fr/net/animation-multi-frame-images/create-multi-frame-tiff-images-aspose-imaging-dotnet/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Comment convertir JPEG en TIFF et créer des images TIFF multi‑cadres avec Aspose.Imaging pour .NET

## Introduction

Vous souhaitez maîtriser l'**conversion de JPEG en TIFF** tout en créant des fichiers TIFF multi‑cadres à l'aide d'Aspose.Imaging pour .NET ? Ce tutoriel complet vous guidera à travers la configuration de votre environnement, la configuration de `TiffOptions`, le redimensionnement des fichiers JPEG et l'ajout de cadres à une image TIFF—le tout en toute simplicité. Que vous gériez des archives de documents ou que vous intégriez de l'imagerie de haute qualité dans des applications logicielles, ce guide est conçu pour optimiser votre flux de travail.

**Ce que vous apprendrez :**
- Comment installer Aspose.Imaging pour .NET
- Configurer `TiffOptions` pour des images noir‑et‑blanc en utilisant la compression CCITT Fax Group 3
- Charger et redimensionner des fichiers JPEG depuis un répertoire
- Ajouter des cadres à une image TIFF
- Enregistrer des images TIFF multi‑cadres

Passons aux prérequis pour commencer.

## Réponses rapides
- **Que signifie « convert JPEG to TIFF » ?** Cela consiste à prendre une image raster JPEG et à l'enregistrer au format TIFF, souvent avec une compression personnalisée ou plusieurs cadres.  
- **Quelle bibliothèque gère cela le mieux sous .NET ?** Aspose.Imaging pour .NET offre une API riche pour la conversion, le redimensionnement et la création de multi‑cadres.  
- **Ai‑je besoin d’une licence ?** Une version d'essai gratuite suffit pour l'évaluation ; une licence permanente supprime toutes les limitations d'évaluation.  
- **Puis‑je charger automatiquement les images depuis un répertoire ?** Oui — le tutoriel montre comment énumérer les fichiers JPEG et les traiter un par un.  
- **Le code est‑il compatible avec .NET 6+ ?** Absolument — l'exemple utilise les API .NET Core/5+ qui fonctionnent sous .NET 6 et versions ultérieures.

## Qu’est‑ce que « convert JPEG to TIFF » ?
Convertir JPEG en TIFF implique de décoder un fichier JPEG, éventuellement de le transformer (par ex. redimensionner ou changer la profondeur de couleur), puis d'encoder le résultat sous forme de fichier TIFF. Le TIFF prend en charge plusieurs cadres, la compression sans perte et les métadonnées que le JPEG ne possède pas, ce qui le rend idéal pour l'archivage et les scénarios multi‑pages.

## Pourquoi utiliser Aspose.Imaging pour cette conversion ?
- **Contrôle total** sur la compression, l'interprétation photométrique et le format de pixel.  
- **Prise en charge multi‑cadres** — vous pouvez regrouper plusieurs pages JPEG dans un même document TIFF.  
- **Multiplateforme** — fonctionne sous Windows, Linux et macOS avec .NET Core/5+.  
- **Aucune dépendance externe** — code purement géré, pas de DLL natives.

## Prérequis

Avant de créer des images TIFF avec Aspose.Imaging, assurez‑vous de disposer de ce qui suit :

### Bibliothèques et dépendances requises
- **Aspose.Imaging pour .NET** : installez cette bibliothèque via NuGet ou votre gestionnaire de paquets préféré.
  
### Exigences de configuration de l’environnement
- Un environnement de développement compatible C# et .NET Core/5+  
  
### Prérequis de connaissances
- Compréhension de base des concepts de programmation C#  
- Familiarité avec la manipulation de fichiers image sous .NET  

## Installation d’Aspose.Imaging pour .NET

Pour commencer, vous devez installer Aspose.Imaging. Voici comment :

**.NET CLI**
```shell
dotnet add package Aspose.Imaging
```

**Package Manager**
```powershell
Install-Package Aspose.Imaging
```

**NuGet Package Manager UI**  
Recherchez « Aspose.Imaging » et installez la dernière version.

### Étapes d’obtention de licence
- **Essai gratuit** : accédez à une version à fonctionnalités limitées pour tester les fonctionnalités.  
- **Licence temporaire** : obtenez‑la pour un essai prolongé sans limitations d’évaluation. Visitez [Temporary License](https://purchase.aspose.com/temporary-license/).  
- **Achat** : pour un accès complet, envisagez d’acheter une licence sur [Purchase Aspose.Imaging](https://purchase.aspose.com/buy).

### Initialisation et configuration de base

```csharp
// Initialize the library with your license
Aspose.Imaging.License license = new Aspose.Imaging.License();
license.SetLicense("Path to your license file");
```

## Comment convertir JPEG en TIFF et ajouter plusieurs cadres

Décomposons l’implémentation en sections gérables.

### Créer et configurer TiffOptions pour l’image TIFF

#### Vue d’ensemble
Créer un objet `TiffOptions` vous permet de définir des paramètres tels que la compression et l’interprétation photométrique, essentiels pour personnaliser vos fichiers TIFF.

#### Implémentation étape par étape

**1. Importer les espaces de noms nécessaires**  
Assurez‑vous d’inclure ces espaces de noms dans votre fichier :

```csharp
using Aspose.Imaging.FileFormats.Tiff;
using Aspose.Imaging.FileFormats.Tiff.Enums;
using Aspose.Imaging.ImageOptions;
```

**2. Configurer TiffOptions**  
Configurez l’objet `TiffOptions` avec des paramètres spécifiques pour une image noir‑et‑blanc utilisant la compression CCITT Fax Group 3.

```csharp
// Create TiffOptions with default settings
TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.Default);

// Set bits per sample to 1 (black and white)
outputSettings.BitsPerSample = new ushort[] { 1 };

// Use CCITT Fax Group 3 compression
outputSettings.Compression = TiffCompressions.CcittFax3;

// Define photometric interpretation as MinIsWhite
outputSettings.Photometric = TiffPhotometrics.MinIsWhite;

// Set source to an empty stream for creating new TIFF from scratch
outputSettings.Source = new Aspose.Imaging.Sources.StreamSource(new System.IO.MemoryStream());
```

### Créer et configurer TiffImage avec des dimensions spécifiques

#### Vue d’ensemble
Créer un `TiffImage` implique de définir des dimensions personnalisées, ce qui est crucial lors de la définition de la taille de chaque cadre TIFF.

**1. Définir les dimensions de l’image**

```csharp
int newWidth = 500; // Width for each TIFF frame
int newHeight = 500; // Height for each TIFF frame
string path = "@YOUR_OUTPUT_DIRECTORY\\AddFramesToTIFFImage_out.tif";
```

**2. Créer une instance de TiffImage**  
Initialisez le `TiffImage` avec les dimensions spécifiées et les paramètres de sortie.

```csharp
using (TiffImage tiffImage = (TiffImage)Aspose.Imaging.Image.Create(outputSettings, newWidth, newHeight))
{
    // Logic to add frames will be added here.
}
```

### Charger les fichiers JPEG depuis un répertoire et les redimensionner

#### Vue d’ensemble
Le chargement d’images JPEG, leur redimensionnement et leur préparation pour inclusion dans un fichier TIFF sont simplifiés avec Aspose.Imaging.

**1. Charger les images JPEG**

```csharp
string dataDir = "@YOUR_DOCUMENT_DIRECTORY"; // Directory containing input images

foreach (var file in Directory.GetFiles(dataDir, "*.jpg"))
{
    using (Aspose.Imaging.RasterImage ri = (Aspose.Imaging.RasterImage)Aspose.Imaging.Image.Load(file))
    {
        // Resize image to match TIFF frame dimensions
        ri.Resize(newWidth, newHeight, Aspose.Imaging.ResizeType.NearestNeighbourResample);
        
        // Additional logic for handling multiple frames will be added here.
    }
}
```

> **Astuce :** L’expression **load images from directory** décrit exactement ce que fait la boucle ci‑dessus — elle énumère chaque fichier JPEG du dossier cible.

### Ajouter un cadre à TiffImage et l’enregistrer

#### Vue d’ensemble
Ajouter des cadres à une image TIFF consiste à copier les pixels JPEG redimensionnés dans chaque cadre puis à enregistrer le TIFF multi‑cadres complet.

**1. Initialiser l’instance TiffImage**

```csharp
using (TiffImage tiffImage = (TiffImage)Aspose.Imaging.Image.Create(outputSettings, newWidth, newHeight))
{
    int index = 0; // Frame index tracker
    
    foreach (var file in Directory.GetFiles(dataDir, "*.jpg"))
    {
        using (Aspose.Imaging.RasterImage ri = (Aspose.Imaging.RasterImage)Aspose.Imaging.Image.Load(file))
        {
            ri.Resize(newWidth, newHeight, Aspose.Imaging.ResizeType.NearestNeighbourResample);
            
            TiffFrame frame = tiffImage.ActiveFrame;
            if (index > 0)
            {
                // Create a new frame for each subsequent image
                frame = new TiffFrame(new TiffOptions(outputSettings), newWidth, newHeight);
            }
            
            // Copy pixels from the resized JPEG into the TIFF frame
            frame.SavePixels(frame.Bounds, ri.LoadPixels(ri.Bounds));
            if (index > 0)
            {
                tiffImage.AddFrame(frame); // Add to TIFF image only after the first frame
            }
            index++;
        }
    }
    
    tiffImage.Save(path); // Save the final TIFF with all frames
}
```

## Applications pratiques

Voici quelques cas d’utilisation réels pour la création d’images TIFF multi‑cadres :

1. **Archivage de documents** — stockez les documents numérisés dans un seul fichier TIFF pour garantir l’intégrité des données et faciliter l’accès.  
2. **Imagerie médicale** — utilisez des formats TIFF compressés de haute qualité pour stocker des scans tels que IRM et CT.  
3. **Design graphique** — combinez plusieurs calques de conception dans un seul fichier pour une manipulation efficace dans les logiciels graphiques.  
4. **Photographie** — archivez des albums photo multi‑pages sous forme de fichiers uniques pour un partage et un stockage simplifiés.  
5. **Contrôle qualité industriel** — enregistrez des données d’inspection détaillées sur plusieurs cadres dans une image TIFF.

## Considérations de performance

### Conseils pour optimiser les performances
- **Gestion de la mémoire** — libérez rapidement les objets image (`using` statements) pour libérer les ressources.  
- **Traitement par lots** — traitez les images par lots si vous travaillez avec de grands ensembles de données afin de garder une utilisation de la mémoire prévisible.  
- **Compression efficace** — choisissez des paramètres de compression qui équilibrent qualité et vitesse selon votre scénario.

## Questions fréquentes

**Q : Puis‑je convertir JPEG en TIFF sans perte de qualité ?**  
R : Oui. En utilisant des options de compression sans perte (par ex. LZW ou CCITT Fax) et en conservant les données de pixel d’origine, la conversion peut être sans perte.

**Q : Dois‑je redimensionner les images avant de les ajouter comme cadres ?**  
R : Tous les cadres d’un TIFF doivent partager les mêmes dimensions, il est donc nécessaire de redimensionner chaque JPEG à la largeur et hauteur cibles.

**Q : Combien de cadres un fichier TIFF peut‑il contenir ?**  
R : Pratiquement illimité ; la contrainte dépend de la taille du fichier et de la mémoire disponible.

**Q : Le TIFF généré est‑il compatible avec les visionneuses courantes ?**  
R : L’exemple utilise la compression standard CCITT Fax Group 3, largement prise en charge par la plupart des visionneuses et éditeurs TIFF.

**Q : Et si je veux appliquer une compression différente pour les images couleur ?**  
R : Remplacez `TiffCompressions.CcittFax3` par `TiffCompressions.Lzw` ou `TiffCompressions.Jpeg` et ajustez `BitsPerSample` en conséquence.

## Conclusion

Ce tutoriel a couvert les étapes essentielles pour **convert JPEG to TIFF** et créer des images TIFF multi‑cadres à l’aide d’Aspose.Imaging pour .NET. De la configuration de `TiffOptions` à l’ajout de cadres, vous disposez désormais d’une base solide pour intégrer de l’imagerie de haute qualité dans vos applications.

**Prochaines étapes**  
- Expérimentez d’autres types de compression et profondeurs de couleur.  
- Explorez les fonctionnalités supplémentaires d’Aspose.Imaging comme la gestion des métadonnées ou la conversion PDF.  
- Consultez la [documentation officielle](https://reference.aspose.com/imaging/net/) pour des informations plus approfondies.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Dernière mise à jour :** 2026-02-09  
**Testé avec :** Aspose.Imaging pour .NET (dernière version stable)  
**Auteur :** Aspose