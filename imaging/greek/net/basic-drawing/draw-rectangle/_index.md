---
date: 2026-02-12
description: Μάθετε πώς να δημιουργήσετε κενή εικόνα με το Aspose και πώς να σχεδιάσετε
  ορθογώνιο .NET με το Aspose.Imaging – ένας γρήγορος οδηγός για τη διαχείριση εικόνων
  στις .NET εφαρμογές σας.
linktitle: Draw Rectangle in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: Δημιουργία Κενής Εικόνας Aspose – Σχεδίαση Ορθογωνίων σε .NET
url: /el/net/basic-drawing/draw-rectangle/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Δημιουργία Κενής Εικόνας Aspose – Σχεδίαση Ορθογωνίων σε .NET

Η δημιουργία και η επεξεργασία εικόνων σε εφαρμογές .NET μπορεί να φαίνεται δύσκολη, αλλά με το Aspose.Imaging μπορείτε να **create blank image Aspose** με λίγες μόνο γραμμές κώδικα και στη συνέχεια να σχεδιάζετε σχήματα πάνω της. Σε αυτό το tutorial θα περάσουμε από όλη τη διαδικασία — από τη δημιουργία ενός κεντρικού καμβά μέχρι το σχεδιασμό ορθογωνίων—ώστε να μπορείτε να προσθέσετε γραφικά στα .NET projects σας αμέσως.

## Γρήγορες Απαντήσεις
- **Τι σημαίνει το “create blank image Aspose”;** Σημαίνει τη δημιουργία ενός κενών bitmap χρησιμοποιώντας το API του Aspose.Imaging.  
- **Πώς να σχεδιάσετε ορθογώνιο .net με Aspose;** Χρησιμοποιήστε τη μέθοδο `Graphics.DrawRectangle` μετά την αρχικοποίηση ενός αντικειμένου `Graphics`.  
- **Ποιο πακέτο NuGet απαιτείται;** `Aspose.Imaging` (τελευταία έκδοση).  
- **Μπορώ να αποθηκεύσω την εικόνα ως PNG, JPEG ή BMP;** Ναι – απλώς αλλάξτε τις επιλογές εικόνας (π.χ., `BmpOptions`, `JpegOptions`).  
- **Χρειάζομαι άδεια για ανάπτυξη;** Μια δωρεάν δοκιμή λειτουργεί για αξιολόγηση· απαιτείται εμπορική άδεια για παραγωγή.

## Τι είναι το “create blank image Aspose”;
Η δημιουργία μιας κενής εικόνας σημαίνει την εκχώρηση ενός buffer εικονοστοιχείων με καθορισμένο πλάτος, ύψος και μορφή εικονοστοιχείου. Το Aspose.Imaging διαχειρίζεται τις χαμηλού επιπέδου λεπτομέρειες, παρέχοντάς σας έναν έτοιμο για σχεδίαση καμβά χωρίς να χρειάζεται να ασχοληθείτε με το GDI+ ή το System.Drawing.

## Γιατί να χρησιμοποιήσετε το Aspose.Imaging για το σχεδιασμό ορθογωνίων σε .NET;
- **Cross‑platform** – λειτουργεί σε Windows, Linux και macOS.  
- **No native dependencies** – καθαρός διαχειριζόμενος κώδικας, ιδανικός για περιβάλλοντα διακομιστών.  
- **Rich drawing API** – υποστηρίζει πένες, πινέλα, anti‑aliasing και πολλούς τύπους σχημάτων.  
- **High performance** – βελτιστοποιημένο για μεγάλες εικόνες και επεξεργασία παρτίδων.

## Προαπαιτούμενα

1. **Aspose.Imaging for .NET** – κατεβάστε το από τη [download page](https://releases.aspose.com/imaging/net/).  
2. **Development Environment** – Visual Studio, VS Code ή οποιοδήποτε IDE συμβατό με .NET.  
3. **.NET runtime** – .NET 6+ ή .NET Framework 4.7.2+.  

Τώρα που έχουμε όλα έτοιμα, ας βουτήξουμε στον κώδικα.

## Πώς να δημιουργήσετε μια κενή εικόνα Aspose σε .NET;

### Βήμα 1: Εισαγωγή των απαιτούμενων namespaces

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Sources;
```

Αυτά τα namespaces σας δίνουν πρόσβαση στις βασικές κλάσεις απεικόνισης, τύπους πινέλων και επιλογές αποθήκευσης εικόνας.

### Βήμα 2: Δημιουργία μιας κενής εικόνας (του καμβά)

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

Σε αυτό το μπλοκ:

* Ορίζουμε την τοποθεσία εξόδου (`dataDir`).  
* Διαμορφώνουμε το `BmpOptions` για χρήση μορφής εικονοστοιχείου 32‑bit.  
* Δημιουργούμε μια **blank image** διαστάσεων 100 × 100 pixel.

### Βήμα 3: Πώς να σχεδιάσετε ορθογώνιο .net με Aspose.Imaging

```csharp
Graphics graphic = new Graphics(image);
graphic.Clear(Color.Yellow);
graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));
```

* `Graphics.Clear` γεμίζει τον καμβά με χρώμα φόντου (κίτρινο σε αυτό το παράδειγμα).  
* `DrawRectangle` σχεδιάζει δύο ορθογώνια—ένα με απλό κόκκινο πένυ, άλλο με μπλε συμπαγές πινέλο—για οπτική αντίθεση.

### Βήμα 4: Αποθήκευση της εικόνας

```csharp
image.Save();
```

Η κλήση του `Save` γράφει το bitmap στο σύστημα αρχείων χρησιμοποιώντας τις επιλογές που ορίστηκαν προηγουμένως.

## Κοινά Προβλήματα & Συμβουλές

| Πρόβλημα | Αιτία | Διόρθωση |
|----------|-------|----------|
| **Η κενή εικόνα εμφανίζεται μαύρη** | Το φόντο δεν έχει καθαριστεί | Καλέστε `graphic.Clear(Color.YourColor)` πριν το σχεδιάσετε. |
| **Εξαίρεση αρχείου δεν βρέθηκε** | `dataDir` δείχνει σε φάκελο που δεν υπάρχει | Βεβαιωθείτε ότι ο φάκελος υπάρχει ή χρησιμοποιήστε `Path.Combine` με `Environment.CurrentDirectory`. |
| **Λανθασμένα χρώματα** | Χρήση του `System.Drawing.Color` αντί του `Aspose.Imaging.Color` | Πάντα εισάγετε το `Aspose.Imaging.Color`. |
| **Καθυστέρηση απόδοσης σε μεγάλες εικόνες** | Χρήση του προεπιλεγμένου `BmpOptions` με υψηλό bits‑per‑pixel | Αλλάξτε σε `JpegOptions` ή `PngOptions` για συμπίεση. |

## Συχνές Ερωτήσεις (Εκτεταμένες)

**Q: Μπορώ να σχεδιάσω άλλα σχήματα εκτός από ορθογώνια;**  
A: Απολύτως. Το Aspose.Imaging παρέχει μεθόδους όπως `DrawEllipse`, `DrawLine` και `DrawPolygon`.

**Q: Είναι η βιβλιοθήκη δωρεάν για εμπορική χρήση;**  
A: Όχι, το Aspose.Imaging είναι εμπορικό προϊόν, αλλά μπορείτε να το αξιολογήσετε με μια δωρεάν δοκιμή διαθέσιμη [εδώ](https://releases.aspose.com/).

**Q: Λειτουργεί αυτό και σε Windows και σε web εφαρμογές;**  
A: Ναι, ο ίδιος κώδικας εκτελείται σε ASP.NET, Blazor και εφαρμογές κονσόλας.

**Q: Πώς αλλάζω τη μορφή εξόδου σε PNG;**  
A: Αντικαταστήστε το `BmpOptions` με `PngOptions` και προσαρμόστε την κατάληξη του αρχείου αναλόγως.

**Q: Πού μπορώ να βρω πιο λεπτομερή τεκμηρίωση;**  
A: Πρόσβαση στην πλήρη αναφορά API [εδώ](https://reference.aspose.com/imaging/net/) και συμμετοχή στην κοινότητα στο [Aspose.Imaging forum](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Τελευταία Ενημέρωση:** 2026-02-12  
**Δοκιμή Με:** Aspose.Imaging 24.12 for .NET  
**Συγγραφέας:** Aspose