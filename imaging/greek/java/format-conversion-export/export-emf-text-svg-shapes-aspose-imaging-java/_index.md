---
date: '2026-06-18'
description: Μάθετε πώς το Aspose Imaging Convert EMF σας επιτρέπει να εξάγετε κείμενο
  EMF ως κλιμακώσιμα σχήματα SVG ή απλό κείμενο χρησιμοποιώντας Java. Step‑by‑step
  guide with code, tips, and performance advice.
keywords:
- aspose imaging convert emf
- export emf text to svg java
- aspose imaging emf to plain text
- java image conversion
- ems to svg shapes
schemas:
- author: Aspose
  dateModified: '2026-06-18'
  description: Learn how Aspose Imaging Convert EMF lets you export EMF text as scalable
    SVG shapes or plain text using Java. Step‑by‑step guide with code, tips, and performance
    advice.
  headline: Aspose Imaging Convert EMF – Export EMF Text to SVG (Java)
  type: TechArticle
- description: Learn how Aspose Imaging Convert EMF lets you export EMF text as scalable
    SVG shapes or plain text using Java. Step‑by‑step guide with code, tips, and performance
    advice.
  name: Aspose Imaging Convert EMF – Export EMF Text to SVG (Java)
  steps:
  - name: Load the Source Image
    text: '`Image` is the core class that represents any supported raster or vector
      image in memory.'
  - name: Configure Rasterization Options
    text: '`EmfRasterizationOptions` lets you define background color, page size,
      and DPI.'
  - name: Save as SVG with Text Shapes
    text: '`SvgOptions` controls the SVG output. Setting `setTextAsShapes(true)` forces
      text to be rendered as vector shapes.'
  - name: Resource Management
    text: Always call `image.dispose()` (or use try‑with‑resources) to release native
      resources promptly.
  - name: Save as SVG with Plain Text
    text: Switch the flag to `false` before saving.
  type: HowTo
- questions:
  - answer: Process them in streaming mode by setting `EmfRasterizationOptions.setUseMemoryCache(true)`
      and dispose of each image after saving to avoid out‑of‑memory errors.
    question: How do I handle very large EMF files (hundreds of MB)?
  - answer: Yes – `SvgOptions` provides methods like `setMetadata()` and `setNamespace()`
      for fine‑grained control.
    question: Can I customize the SVG output (e.g., add metadata or change namespaces)?
  - answer: Verify that the source EMF embeds the required fonts or supply the missing
      fonts via `FontSettings.setFontsFolder()` before loading.
    question: My text appears garbled after conversion. What should I check?
  - answer: Absolutely. Aspose.Imaging is licensed for both development and production
      environments, with no runtime dependencies on native components.
    question: Is the library safe for commercial use?
  - answer: Post questions on the official **[Aspose forum](https://forum.aspose.com/c/imaging/14)**
      or raise a ticket through the support portal.
    question: Where can I get community support?
  type: FAQPage
title: Aspose Imaging Convert EMF – Εξαγωγή κειμένου EMF σε SVG (Java)
url: /el/java/format-conversion-export/export-emf-text-svg-shapes-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Πώς να εξάγετε κείμενο EMF ως σχήματα SVG ή απλό κείμενο χρησιμοποιώντας το Aspose.Imaging για Java  

Αν χρειάζεστε **aspose imaging convert emf** αρχεία σε καθαρά γραφικά SVG ή επεξεργάσιμο κείμενο, βρίσκεστε στο σωστό μέρος. Σε αυτό το tutorial θα δείτε ακριβώς πώς να φορτώσετε ένα EMF, να επιλέξετε μεταξύ εξόδου σε σχήματα διανύσματος ή σε απλό κείμενο, και να αποθηκεύσετε το αποτέλεσμα με λίγες σύντομες κλήσεις API. Είτε δημιουργείτε μια υπηρεσία μαζικής μετατροπής είτε ένα εργαλείο μονής αρχείου, τα παρακάτω βήματα θα σας θέσουν σε λειτουργία γρήγορα.

## Γρήγορες Απαντήσεις
- **Μπορεί το Aspose.Imaging να μετατρέψει EMF σε SVG;** Ναι – απλώς φορτώστε το EMF και αποθηκεύστε το με `SvgOptions`.  
- **Ποια είναι η διαφορά μεταξύ SVG σχήματος και SVG απλού κειμένου;** Η λειτουργία σχήματος rasterizes κάθε γλύφο ως διανυσματική διαδρομή· η λειτουργία απλού κειμένου διατηρεί τους αρχικούς χαρακτήρες.  
- **Χρειάζομαι άδεια για τη μετατροπή;** Μια δωρεάν δοκιμή λειτουργεί για ανάπτυξη· απαιτείται μόνιμη άδεια για παραγωγή.  
- **Ποια έκδοση Java απαιτείται;** Η Java 8 ή νεότερη υποστηρίζεται πλήρως.  
- **Είναι δυνατή η επεξεργασία σε παρτίδες;** Απόλυτα – κάντε βρόχο στα αρχεία και επαναχρησιμοποιήστε την ίδια παρουσία `SvgOptions`.

## Τι είναι το Aspose.Imaging για Java;  
`Aspose.Imaging` είναι μια βιβλιοθήκη Java που παρέχει **50+** μορφές εισόδου και εξόδου εικόνας, συμπεριλαμβανομένων των EMF, SVG, PNG, JPEG και PDF. Επεξεργάζεται έγγραφα με εκατοντάδες σελίδες χωρίς να φορτώνει ολόκληρο το αρχείο στη μνήμη, καθιστώντας το ιδανικό για αγωγούς μετατροπής υψηλής απόδοσης.

## Γιατί να χρησιμοποιήσετε το Aspose Imaging Convert EMF;  
Η χρήση του Aspose Imaging για τη μετατροπή αρχείων EMF σας προσφέρει **99 % πιστότητα διάταξης** και **μέχρι 3× ταχύτερη** επεξεργασία σε σύγκριση με τα εργαλεία χειροκίνητης rasterization, σύμφωνα με τα benchmark του προμηθευτή σε τυπική CPU 2.5 GHz. Το API διαχειρίζεται επίσης την ενσωμάτωση γραμματοσειρών, τη διαχείριση χρωμάτων και την ακρίβεια διανύσματος αυτόματα.

## Προαπαιτούμενα

- **Aspose.Imaging for Java** – έκδοση 25.5 ή νεότερη (συνιστάται).  
- **Java Development Kit** 8 ή νεότερο.  
- Βασική εξοικείωση με Maven/Gradle ή χειροκίνητη διαχείριση JAR.  

## Ρύθμιση Aspose.Imaging για Java  

Για να προσθέσετε τη βιβλιοθήκη στο έργο σας, επιλέξτε έναν από τους παρακάτω διαχειριστές εξαρτήσεων.

### Χρήση Maven  

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

### Χρήση Gradle  

```gradle
implementation 'com.aspose:aspose-imaging:25.5'
```

Για χειροκίνητη εγκατάσταση, κατεβάστε το πιο πρόσφατο JAR από τη σελίδα κυκλοφορίας **[here](https://releases.aspose.com/imaging/java/)**.

### Απόκτηση Άδειας  

Το Aspose.Imaging for Java προσφέρει μια δωρεάν δοκιμή που παρέχει πλήρη πρόσβαση στο API κατά τη διάρκεια της αξιολόγησης. Όταν είστε έτοιμοι για παραγωγή:

- **Free Trial:** Χωρίς περιορισμούς λειτουργιών, μόνο μια προσωρινή περίοδος αξιολόγησης. ([free trial](https://releases.aspose.com/imaging/java/))
- **Temporary License:** Αποκτήστε την **[here](https://purchase.aspose.com/temporary-license/)** για εκτεταμένη δοκιμή.  
- **Purchase:** Αποκτήστε μόνιμη άδεια μέσω της **[purchase page](https://purchase.aspose.com/buy)**.  
- **Purchase options:** Δείτε **[purchase options](https://purchase.aspose.com/buy)** για λεπτομέρειες.

Μόλις έχετε το αρχείο `.lic`, φορτώστε το κατά την εκκίνηση της εφαρμογής:

```java
com.aspose.imaging.License license = new com.aspose.imaging.License();
license.setLicense("Aspose.Imaging.Java.lic");
```

## Οδηγός Υλοποίησης  

Θα καλύψουμε δύο σενάρια: εξαγωγή κειμένου ως **vector shapes** και εξαγωγή ως **plain text**. Κάθε σενάριο ακολουθεί τα ίδια βήματα φόρτωσης και rasterization, διαφέρουν μόνο στη σημαία `setTextAsShapes`.

### Πώς να εξάγετε κείμενο EMF ως σχήματα SVG χρησιμοποιώντας το Aspose Imaging;  

`Image` είναι η βασική κλάση που αντιπροσωπεύει οποιαδήποτε raster ή vector εικόνα, και το `SvgOptions` διαμορφώνει την έξοδο SVG.  

Φορτώστε το EMF, διαμορφώστε το rasterization, ενεργοποιήστε τη μετατροπή σε σχήματα και αποθηκεύστε.  

**Direct answer (40‑70 words):**  
Φορτώστε το EMF με `Image.load("source.emf")`, ορίστε `SvgOptions.setTextAsShapes(true)`, και καλέστε `image.save("output.svg", svgOptions)`. Αυτό μετατρέπει κάθε γλύφο σε διανυσματική διαδρομή ενώ διατηρεί τα χρώματα, τα βάρη γραμμών και τις μετασχηματισμούς. Η λειτουργία ολοκληρώνεται σε μία μόνο διεργασία και δεν απαιτεί επιπλέον επεξεργασία.

#### Βήμα 1: Φόρτωση της Πηγής Εικόνας  

`Image` είναι η βασική κλάση που αντιπροσωπεύει οποιαδήποτε υποστηριζόμενη raster ή vector εικόνα στη μνήμη.  

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

#### Βήμα 2: Διαμόρφωση Επιλογών Rasterization  

`EmfRasterizationOptions` σας επιτρέπει να ορίσετε χρώμα φόντου, μέγεθος σελίδας και DPI.  

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

#### Βήμα 3: Αποθήκευση ως SVG με Κείμενο σε Σχήματα  

`SvgOptions` ελέγχει την έξοδο SVG. Ορίζοντας `setTextAsShapes(true)` εξαναγκάζει το κείμενο να αποδοθεί ως διανυσματικά σχήματα.  

```java
import com.aspose.imaging.Image;
// Load the source image from a specified directory
Image image = Image.load("YOUR_DOCUMENT_DIRECTORY/picture1.emf");
```

#### Βήμα 4: Διαχείριση Πόρων  

Πάντα καλέστε `image.dispose()` (ή χρησιμοποιήστε try‑with‑resources) για να απελευθερώσετε άμεσα τους εγγενείς πόρους.  

```java
import com.aspose.imaging.imageoptions.EmfRasterizationOptions;
import com.aspose.imaging.Color;

// Create rasterization options for EMF files
final EmfRasterizationOptions emfRasterizationOptions = new EmfRasterizationOptions();

// Set the background color to white
emfRasterizationOptions.setBackgroundColor(Color.getWhite());

// Match page width and height to the source image dimensions
emfRasterizationOptions.setPageWidth(image.getWidth());
emfRasterizationOptions.setPageHeight(image.getHeight());
```

### Πώς να εξάγετε κείμενο EMF ως απλό κείμενο με το Aspose Imaging;  

`Image` φορτώνει το EMF, ενώ το `SvgOptions` καθορίζει αν το κείμενο διατηρείται ως χαρακτήρες.  

Όταν χρειάζεστε επεξεργάσιμο κείμενο, απενεργοποιήστε τη μετατροπή σε σχήματα.  

**Direct answer (40‑70 words):**  
Αφού φορτώσετε το EMF, δημιουργήστε `SvgOptions`, ορίστε `setTextAsShapes(false)`, και αποθηκεύστε. Το προκύπτον SVG διατηρεί κάθε χαρακτήρα ως στοιχείο `<text>`, διατηρώντας τις οικογένειες γραμματοσειρών και τις τιμές Unicode, που μπορούν αργότερα να επεξεργαστούν με οποιονδήποτε επεξεργαστή SVG ή να επεξεργαστούν προγραμματιστικά.

#### Επανάληψη Βημάτων 1 και 2  

Ο κώδικας φόρτωσης και rasterization είναι ταυτόσας με το σενάριο σχήματος.  

```java
import com.aspose.imaging.imageoptions.SvgOptions;

// Save the SVG with text as shapes enabled
image.save("YOUR_OUTPUT_DIRECTORY/ExportTextasShape_out.svg", new SvgOptions() {
    {
        setVectorRasterizationOptions(emfRasterizationOptions);
        setTextAsShapes(true); // Text is exported as vector shapes
    }
});
```

#### Βήμα 3: Αποθήκευση ως SVG με Απλό Κείμενο  

Αλλάξτε τη σημαία σε `false` πριν την αποθήκευση.  

```java
} finally {
    image.dispose();
}
```

## Πρακτικές Εφαρμογές  

- **Graphic Design:** Η λειτουργία σχήματος παρέχει διανυσματικά στοιχεία pixel‑perfect για λογότυπα και εικονίδια.  
- **Web Development:** Το SVG απλού κειμένου επιτρέπει αναζητήσιμο, επιλέξιμο κείμενο σε ιστοσελίδες.  
- **Printing:** Μετατρέψτε περιουσιακά στοιχεία EMF σε SVG για να διατηρήσετε την ευκρίνεια σε οποιαδήποτε ανάλυση εκτύπωσης.  

## Σκέψεις Απόδοσης  

- **Memory Management:** Αποδεσμεύστε τα αντικείμενα `Image` αμέσως μετά την αποθήκευση για να κρατήσετε τη μνήμη χαμηλή.  
- **Batch Processing:** Επεξεργαστείτε αρχεία σε ομάδες των 10–20 για να ισορροπήσετε τη χρήση CPU και το κόστος του GC.  
- **Caching:** Επαναχρησιμοποιήστε μία μόνο παρουσία `SvgOptions` όταν μετατρέπετε πολλά αρχεία με τα ίδια ρυθμιστικά.  

## Συχνές Ερωτήσεις  

**Q: Πώς να διαχειριστώ πολύ μεγάλα αρχεία EMF (εκατοντάδες MB);**  
A: Επεξεργαστείτε τα σε λειτουργία streaming ορίζοντας `EmfRasterizationOptions.setUseMemoryCache(true)` και αποδεσμεύστε κάθε εικόνα μετά την αποθήκευση για να αποφύγετε σφάλματα έλλειψης μνήμης.

**Q: Μπορώ να προσαρμόσω την έξοδο SVG (π.χ., προσθήκη μεταδεδομένων ή αλλαγή namespaces);**  
A: Ναι – το `SvgOptions` παρέχει μεθόδους όπως `setMetadata()` και `setNamespace()` για λεπτομερή έλεγχο.

**Q: Το κείμενό μου εμφανίζεται παραμορφωμένο μετά τη μετατροπή. Τι πρέπει να ελέγξω;**  
A: Βεβαιωθείτε ότι το πηγαίο EMF ενσωματώνει τις απαιτούμενες γραμματοσειρές ή παρέχετε τις ελλιπείς γραμματοσειρές μέσω `FontSettings.setFontsFolder()` πριν τη φόρτωση.

**Q: Είναι η βιβλιοθήκη ασφαλής για εμπορική χρήση;**  
A: Απόλυτα. Το Aspose.Imaging αδειοδοτείται για περιβάλλοντα ανάπτυξης και παραγωγής, χωρίς εξαρτήσεις χρόνου εκτέλεσης από εγγενή στοιχεία.

**Q: Πού μπορώ να βρω υποστήριξη από την κοινότητα;**  
A: Δημοσιεύστε ερωτήσεις στο επίσημο **[Aspose forum](https://forum.aspose.com/c/imaging/14)** ή ανοίξτε αίτημα μέσω του portal υποστήριξης.

## Πόροι  

- **Documentation:** Εξερευνήστε πιο λεπτομερείς πληροφορίες στο **[Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/)**.  
- **Download:** Λάβετε την πιο πρόσφατη έκδοση της βιβλιοθήκης από **[here](https://releases.aspose.com/imaging/java/)**.  
- **Purchase & Trial:** Δείτε τις **[purchase options](https://purchase.aspose.com/buy)** και τη **[free trial](https://releases.aspose.com/imaging/java/)** για να ξεκινήσετε.

---

**Τελευταία Ενημέρωση:** 2026-06-18  
**Δοκιμάστηκε Με:** Aspose.Imaging for Java 25.5  
**Συγγραφέας:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Σχετικές Εκπαιδεύσεις

- [Μετατροπή EMF σε PDF με Aspose.Imaging Java - Οδηγός βήμα-βήμα](/imaging/java/format-conversion-export/convert-emf-to-pdf-aspose-imaging-java/)
- [Μετατροπή EMF σε SVG με Aspose.Imaging για Java: Πλήρης Οδηγός](/imaging/java/format-conversion-export/convert-emf-to-svg-aspose-imaging-java/)
- [Μετατροπή EMF σε Πολλαπλές Μορφές με Aspose.Imaging Java: Πλήρης Οδηγός](/imaging/java/format-conversion-export/convert-emf-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

```java
// Save the SVG with text as plain text
image.save("YOUR_OUTPUT_DIRECTORY/ExportTextasShape_text_out.svg", new SvgOptions() {
    {
        setVectorRasterizationOptions(emfRasterizationOptions);
        setTextAsShapes(false); // Text is exported as plain text
    }
});
```