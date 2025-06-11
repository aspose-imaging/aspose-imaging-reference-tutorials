---
"date": "2025-06-03"
"description": "Maîtrisez la conversion SVG en PDF avec Aspose.Imaging .NET tout en préservant la qualité des polices. Apprenez la configuration des répertoires, l'intégration des polices et bien plus encore."
"title": "Conversion efficace de SVG en PDF grâce à la gestion des polices et aux techniques Aspose.Imaging .NET"
"url": "/fr/net/format-conversion-export/aspose-imaging-net-svg-to-pdf-conversion/"
"weight": 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Conversion efficace de SVG en PDF avec Aspose.Imaging .NET

## Introduction

À l'ère du numérique, la conversion de graphiques vectoriels en formats polyvalents comme le PDF est essentielle pour le partage et l'impression de documents. Préserver l'intégrité des polices lors de cette conversion peut s'avérer complexe. Ce tutoriel montre comment convertir facilement des fichiers SVG en PDF tout en préservant la qualité des polices grâce à Aspose.Imaging pour .NET.

**Ce que vous apprendrez :**
- Configuration des répertoires et exportation des fichiers SVG au format PDF.
- Techniques d'intégration ou d'exportation de polices dans des fichiers SVG.
- Implémentation d'un gestionnaire de rappel personnalisé pour la gestion des polices SVG pendant le processus d'enregistrement.

Grâce à ces compétences, vous pouvez garantir que vos documents sont professionnels et cohérents sur différentes plateformes. Commençons par configurer notre environnement !

## Prérequis

Avant de plonger dans le code, assurez-vous de disposer des éléments suivants :

### Bibliothèques requises
- **Aspose.Imaging pour .NET**:Essentiel pour gérer les conversions d'images.
- **Espace de noms System.IO**: Pour les opérations sur les fichiers et les répertoires.

### Configuration de l'environnement
Assurez-vous de disposer d'un environnement de développement compatible, comme Visual Studio ou tout autre IDE prenant en charge les projets .NET. Une connaissance des bases de la programmation C# est un atout.

## Configuration d'Aspose.Imaging pour .NET

Pour utiliser Aspose.Imaging dans votre projet, suivez ces étapes d'installation :

**Utilisation de .NET CLI :**
```bash
dotnet add package Aspose.Imaging
```

**Utilisation du gestionnaire de paquets :**
```powershell
Install-Package Aspose.Imaging
```

**Via l'interface utilisateur du gestionnaire de packages NuGet :**
Recherchez « Aspose.Imaging » et installez la dernière version.

### Acquisition de licence
- **Essai gratuit**: Commencez par un essai gratuit pour tester les fonctionnalités.
- **Permis temporaire**:Obtenez une licence temporaire pour une évaluation prolongée.
- **Achat**:Envisagez d'acheter si Aspose.Imaging répond à vos besoins.

#### Initialisation et configuration
Pour utiliser Aspose.Imaging, ajoutez-le comme dépendance à votre projet. Voici une configuration de base :

```csharp
using Aspose.Imaging;
```

Assurer la `Aspose.Imaging` L'espace de noms est inclus en haut de votre fichier pour accéder à ses classes et méthodes.

## Guide de mise en œuvre

Cette section décompose chaque fonctionnalité en étapes gérables.

### Configuration du répertoire et exportation SVG au format PDF

#### Aperçu
Convertissez un fichier SVG en PDF tout en vous assurant que les chemins de répertoire sont correctement configurés pour la sortie.

**Étape 1 : Assurez-vous que le répertoire de sortie existe**
```csharp
string SourceFolder = "YOUR_DOCUMENT_DIRECTORY";
string OutFolderName = "Out";
string OutFolder = Path.Combine(SourceFolder, OutFolderName);

if (!Directory.Exists(OutFolder))
{
    Directory.CreateDirectory(OutFolder);
}
```
*Explication*: Cet extrait de code vérifie si le répertoire de sortie existe et le crée si nécessaire.

**Étape 2 : Charger le SVG et exporter au format PDF**
```csharp
public void ReadAndExportToPdf(string inputFileName)
{
    string inputFile = Path.Combine(SourceFolder, inputFileName);
    string outFile = Path.Combine(OutFolder, inputFileName + ".pdf");
    
    using (Image image = Image.Load(inputFile))
    {
        image.Save(outFile,
            new PdfOptions { VectorRasterizationOptions = new SvgRasterizationOptions { PageSize = image.Size } });
    }
}
```
*Explication*: Le `PdfOptions` permet de configurer la rastérisation du contenu SVG, en garantissant que la taille de la page correspond aux dimensions de l'image d'origine.

### Enregistrement SVG avec options d'intégration de polices

#### Aperçu
Enregistrez un fichier SVG tout en contrôlant les paramètres d'intégration des polices pour maintenir la fidélité des polices.

**Étape 1 : Définir les répertoires de sortie et de polices**
```csharp
string FontFolderName = "fonts";
string FontFolder = Path.Combine(OutFolder, FontFolderName);

if (!Directory.Exists(FontFolder))
{
    Directory.CreateDirectory(FontFolder);
}
```
*Explication*: Assurez-vous que les répertoires sont configurés avant d'enregistrer les fichiers.

**Étape 2 : Enregistrer le fichier SVG avec des options de police personnalisées**
```csharp
public void Save(bool useEmbedded, string fileName, int expectedCountFonts)
{
    string fontStoreType = useEmbedded ? "Embedded" : "Stream";
    string inputFile = Path.Combine(SourceFolder, fileName);
    string outFileName = $"{Path.GetFileNameWithoutExtension(fileName)}_{fontStoreType}.svg";
    string outputFile = Path.Combine(OutFolder, outFileName);

    using (Image image = Image.Load(inputFile))
    {
        EmfRasterizationOptions emfRasterizationOptions = new EmfRasterizationOptions
        {
            BackgroundColor = Color.White,
            PageWidth = image.Width,
            PageHeight = image.Height
        };

        string testingFileName = Path.GetFileNameWithoutExtension(inputFile);
        string fontFolder = Path.Combine(FontFolder, testingFileName);

        image.Save(outputFile,
            new SvgOptions
            {
                VectorRasterizationOptions = emfRasterizationOptions,
                Callback = new SvgCallbackFontTest(useEmbedded, fontFolder)
                {
                    Link = FontFolderName + "/" + testingFileName
                }
            });
    }

    if (!useEmbedded)
    {
        string[] files = Directory.GetFiles(fontFolder);
        if (files.Length != expectedCountFonts)
        {
            throw new Exception($"Expected count font files = {expectedCountFonts}, Current count font files = {files.Length}");
        }
    }
}
```
*Explication*:Cette méthode vous permet de spécifier si les polices doivent être intégrées ou diffusées en continu, ce qui affecte la manière dont elles sont stockées et accessibles.

### Gestionnaire de rappel de police SVG personnalisé

#### Aperçu
Implémentez un gestionnaire personnalisé pour gérer les ressources de police lors de l'enregistrement SVG.

**Étape 1 : Implémenter la classe SvgCallbackFontTest**
```csharp
public class SvgCallbackFontTest : SvgResourceKeeperCallback
{
    private readonly string outFolder;
    private readonly bool useEmbeddedFont;
    private int fontCounter = 0;

    public string Link { get; set; }

    public SvgCallbackFontTest(bool useEmbeddedFont, string outFolder)
    {
        this.useEmbeddedFont = useEmbeddedFont;
        this.outFolder = outFolder;
        
        if (Directory.Exists(outFolder))
        {
            Directory.Delete(this.outFolder, true);
        }
    }

    public override void OnFontResourceReady(FontStoringArgs args)
    {
        if (this.useEmbeddedFont)
        {
            args.FontStoreType = FontStoreType.Embedded;
        }
        else
        {
            args.FontStoreType = FontStoreType.Stream;
            string fontFolder = this.outFolder;

            if (!Directory.Exists(fontFolder))
            {
                Directory.CreateDirectory(fontFolder);
            }

            string fName = args.SourceFontFileName;
            if (!File.Exists(fName))
            {
                fName = $"font_{this.fontCounter++}.ttf";
            }

            string fileName = Path.Combine(fontFolder, Path.GetFileName(fName));
            
            args.DestFontStream = new FileStream(fileName, FileMode.OpenOrCreate);
            args.DisposeStream = true;
            args.FontFileUri = $".{this.Link}/{Path.GetFileName(fName)}";
        }
    }
}
```
*Explication*Cette classe gère les ressources de polices en décidant de les intégrer directement ou de les stocker séparément. Elle garantit que les polices sont correctement référencées et enregistrées lors de l'exportation SVG.

## Applications pratiques

1. **Génération automatisée de rapports**:Utilisez Aspose.Imaging pour convertir les brouillons de conception en PDF pour une distribution cohérente.
2. **Édition numérique**Assurez un rendu de police de haute qualité lors de la conversion d'articles avec des graphiques intégrés de SVG en PDF.
3. **Partage de documents multiplateforme**: Maintenir l’intégrité visuelle des documents partagés entre différents systèmes d’exploitation.

## Considérations relatives aux performances

### Conseils pour optimiser les performances
- Utilisez des pratiques efficaces de gestion des fichiers, telles que l’élimination rapide des flux après utilisation.
- Réduisez l’utilisation de la mémoire en supprimant les objets et répertoires inutilisés une fois le traitement terminé.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}