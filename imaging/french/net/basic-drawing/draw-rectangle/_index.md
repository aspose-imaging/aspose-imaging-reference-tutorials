---
date: 2026-02-12
description: Apprenez comment créer une image vierge avec Aspose et comment dessiner
  un rectangle en .NET avec Aspose.Imaging – un guide rapide pour la manipulation
  d'images dans vos applications .NET.
linktitle: Draw Rectangle in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: Créer une image vierge avec Aspose – Dessiner des rectangles en .NET
url: /fr/net/basic-drawing/draw-rectangle/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Créer une image vierge Aspose – Dessiner des rectangles en .NET

Créer et manipuler des images dans les applications .NET peut sembler intimidant, mais avec Aspose.Imaging vous pouvez **créer une image vierge Aspose** en quelques lignes de code seulement, puis dessiner des formes dessus. Dans ce tutoriel, nous parcourrons l’ensemble du processus — de la configuration d’une toile vierge au dessin de rectangles—afin que vous puissiez commencer à ajouter des graphiques à vos projets .NET immédiatement.

## Réponses rapides
- **Que signifie « create blank image Aspose » ?** Cela signifie générer un bitmap vide en utilisant l’API Aspose.Imaging.  
- **Comment dessiner un rectangle .net avec Aspose ?** Utilisez la méthode `Graphics.DrawRectangle` après avoir initialisé un objet `Graphics`.  
- **Quel package NuGet est requis ?** `Aspose.Imaging` (dernière version).  
- **Puis-je enregistrer l’image au format PNG, JPEG ou BMP ?** Oui – il suffit de changer les options d’image (par ex., `BmpOptions`, `JpegOptions`).  
- **Ai‑je besoin d’une licence pour le développement ?** Un essai gratuit suffit pour l’évaluation ; une licence commerciale est requise pour la production.

## Qu’est‑ce que « create blank image Aspose » ?
Créer une image vierge consiste à allouer un tampon de pixels avec une largeur, une hauteur et un format de pixel définis. Aspose.Imaging gère les détails de bas niveau, vous offrant une toile prête à être dessinée sans avoir à manipuler GDI+ ou System.Drawing.

## Pourquoi utiliser Aspose.Imaging pour dessiner des rectangles en .NET ?
- **Cross‑platform** – fonctionne sous Windows, Linux et macOS.  
- **No native dependencies** – code purement géré, parfait pour les environnements serveur.  
- **Rich drawing API** – prend en charge les stylos, les pinceaux, l’anti‑aliasing et de nombreux types de formes.  
- **High performance** – optimisé pour les images volumineuses et le traitement par lots.

## Prérequis

1. **Aspose.Imaging for .NET** – téléchargez‑le depuis la [page de téléchargement](https://releases.aspose.com/imaging/net/).  
2. **Environnement de développement** – Visual Studio, VS Code ou tout IDE compatible .NET.  
3. **Runtime .NET** – .NET 6+ ou .NET Framework 4.7.2+.  

Maintenant que tout est configuré, plongeons dans le code.

## Comment créer une image vierge Aspose en .NET ?

### Étape 1 : Importer les espaces de noms requis

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Sources;
```

Ces espaces de noms vous donnent accès aux classes d’imagerie de base, aux types de pinceaux et aux options d’enregistrement d’image.

### Étape 2 : Créer une image vierge (la toile)

```csharp
string dataDir = "Your Document Directory";  // Set the path to your document directory
using (FileStream stream = new FileStream(dataDir, FileMode.Create))
{
    BmpOptions saveOptions = new BmpOptions();
    saveOptions.BitsPerPixel = 32;
    saveOptions.Source = new StreamSource(stream);

    using (Image image = Image.Create(saveOptions, 100, 100))
    {
        // Your drawing code will go here
        image.Save();
    }
}
```

Dans ce bloc, nous :
* Définissons l’emplacement de sortie (`dataDir`).  
* Configurons `BmpOptions` pour utiliser un format de pixel 32 bits.  
* Créons une **image vierge** de 100 × 100 pixels.  

### Étape 3 : Comment dessiner un rectangle .net avec Aspose.Imaging

```csharp
Graphics graphic = new Graphics(image);
graphic.Clear(Color.Yellow);
graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));
```

* `Graphics.Clear` remplit la toile avec une couleur d’arrière‑plan (jaune dans cet exemple).  
* `DrawRectangle` dessine deux rectangles — l’un avec un stylo rouge simple, l’autre avec un pinceau bleu plein — pour un contraste visuel.

### Étape 4 : Enregistrer l’image

```csharp
image.Save();
```

L’appel à `Save` écrit le bitmap sur le système de fichiers en utilisant les options définies précédemment.

## Problèmes courants & astuces

| Problème | Raison | Solution |
|----------|--------|----------|
| **L'image vierge apparaît noire** | Arrière‑plan non effacé | Appelez `graphic.Clear(Color.YourColor)` avant de dessiner. |
| **Exception fichier introuvable** | `dataDir` pointe vers un dossier inexistant | Assurez‑vous que le répertoire existe ou utilisez `Path.Combine` avec `Environment.CurrentDirectory`. |
| **Couleurs incorrectes** | Utilisation de `System.Drawing.Color` au lieu de `Aspose.Imaging.Color` | Importez toujours `Aspose.Imaging.Color`. |
| **Ralentissement de performance sur les grandes images** | Utilisation des `BmpOptions` par défaut avec un grand nombre de bits‑par‑pixel | Passez à `JpegOptions` ou `PngOptions` pour la compression. |

## Questions fréquentes (étendues)

**Q : Puis‑je dessiner d’autres formes que des rectangles ?**  
R : Absolument. Aspose.Imaging fournit des méthodes comme `DrawEllipse`, `DrawLine` et `DrawPolygon`.

**Q : La bibliothèque est‑elle gratuite pour une utilisation commerciale ?**  
R : Non, Aspose.Imaging est un produit commercial, mais vous pouvez l’évaluer avec un essai gratuit disponible [ici](https://releases.aspose.com/).

**Q : Cela fonctionne‑t‑il à la fois sur Windows et les applications web ?**  
R : Oui, le même code s’exécute sous ASP.NET, Blazor et les applications console.

**Q : Comment changer le format de sortie en PNG ?**  
R : Remplacez `BmpOptions` par `PngOptions` et ajustez l’extension du fichier en conséquence.

**Q : Où puis‑je trouver une documentation plus détaillée ?**  
R : Accédez à la référence complète de l’API [ici](https://reference.aspose.com/imaging/net/) et rejoignez la communauté sur le [forum Aspose.Imaging](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Dernière mise à jour :** 2026-02-12  
**Testé avec :** Aspose.Imaging 24.12 for .NET  
**Auteur :** Aspose