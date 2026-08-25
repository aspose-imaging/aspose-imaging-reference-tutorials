---
date: '2026-06-28'
description: Μάθετε πώς να μετατρέψετε ODP σε PNG χρησιμοποιώντας το Aspose.Imaging
  for Java, ορίστε προσαρμοσμένες γραμματοσειρές και απενεργοποιήστε τις συστημικές
  γραμματοσειρές για ακριβή απόδοση.
keywords:
- how to convert odp
- maven aspose imaging
- aspose imaging license
- disable system fonts
- java convert presentation image
schemas:
- author: Aspose
  dateModified: '2026-06-28'
  description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  headline: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts
    & Export Guide
  type: TechArticle
- description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  name: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts & Export
    Guide
  steps:
  - name: '**Free Trial** – No license required, limited features.'
    text: '**Free Trial** – No license required, limited features.'
  - name: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
    text: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
  - name: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
    text: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
  - name: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
    text: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
  - name: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
    text: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
  - name: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
    text: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
  type: HowTo
- questions:
  - answer: Aspose.Imaging for Java works with JDK 8 and newer; JDK 11 is recommended
      for long‑term support.
    question: What is the minimum Java version required?
  - answer: Yes, set `rasterizationOptions.setPageNumber(specificSlideIndex)` before
      calling `save`.
    question: Can I convert only selected slides?
  - answer: Load the file with `LoadOptions` that includes the password, then proceed
      with the same font settings.
    question: How do I handle password‑protected ODP files?
  - answer: It marginally improves speed because the engine skips the lookup of system
      fonts, especially noticeable on machines with large font collections.
    question: Does disabling system fonts affect performance?
  - answer: Explore the official [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/)
      for additional scenarios such as batch conversion and image transformations.
    question: Where can I find more code samples?
  type: FAQPage
title: Πώς να μετατρέψετε ODP σε PNG με το Aspose.Imaging for Java – Οδηγός προσαρμοσμένων
  γραμματοσειρών & εξαγωγής
url: /el/java/format-conversion-export/export-odp-to-png-aspose-imaging-java-custom-fonts/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Πώς να Μετατρέψετε ODP σε PNG με το Aspose.Imaging για Java – Προσαρμοσμένες Γραμματοσειρές & Οδηγός Εξαγωγής

Σε σύγχρονες εφαρμογές Java, η μετατροπή αρχείων OpenDocument Presentation (ODP) σε εικόνες PNG υψηλής ποιότητας είναι μια συχνή απαίτηση—ιδιαίτερα όταν χρειάζεται να διατηρηθεί η ταυτότητα της μάρκας μέσω προσαρμοσμένων γραμματοσειρών. Αυτό το tutorial δείχνει **πώς να μετατρέψετε ODP** σε PNG χρησιμοποιώντας το Aspose.Imaging για Java, σας καθοδηγεί στη ρύθμιση ενός φακέλου προσαρμοσμένων γραμματοσειρών, στην απενεργοποίηση των εναλλακτικών γραμματοσειρών του συστήματος, και στην λεπτομερή ρύθμιση των επιλογών rasterization για βέλτιστη απόδοση.

**Τι Θα Μάθετε**
- Πώς να ορίσετε προσαρμοσμένο φάκελο γραμματοσειρών για τη μετατροπή ODP.  
- Πώς να απενεργοποιήσετε τις εναλλακτικές γραμματοσειρές του συστήματος ώστε να χρησιμοποιούνται μόνο οι επιλεγμένες γραμματοσειρές σας.  
- Πώς να εξάγετε ένα αρχείο ODP σε PNG με ακριβείς διαστάσεις και ρυθμίσεις γραμματοσειράς.  
- Συμβουλές για βελτίωση της ταχύτητας και της χρήσης μνήμης κατά την επεξεργασία μεγάλων παρουσιάσεων.

## Γρήγορες Απαντήσεις
- **Μπορώ να χρησιμοποιήσω το Maven για να προσθέσω το Aspose.Imaging;** Ναι, προσθέστε την εξάρτηση Maven και εκτελέστε `mvn install`.  
- **Χρειάζομαι άδεια για παραγωγή;** Απαιτείται έγκυρη άδεια Aspose.Imaging για απεριόριστη χρήση.  
- **Θα γίνουν σεβαστές οι προσαρμοσμένες γραμματοσειρές μου;** Ορίστε το φάκελο γραμματοσειρών και απενεργοποιήστε τις εναλλακτικές του συστήματος για να τις επιβάλλετε.  
- **Ποιοι τύποι εικόνας υποστηρίζονται;** Το Aspose.Imaging υποστηρίζει πάνω από 120 raster και vector μορφές, συμπεριλαμβανομένων PNG, JPEG, TIFF, και WebP.  
- **Είναι το API thread‑safe;** Ναι, οι περισσότερες κλάσεις του Aspose.Imaging είναι ασφαλείς για ταυτόχρονη χρήση όταν δημιουργείτε ξεχωριστές στιγμιότυπες ανά νήμα.

## Τι είναι το “how to convert odp”;
*“How to convert odp”* αναφέρεται στη διαδικασία μετασχηματισμού ενός αρχείου OpenDocument Presentation σε άλλη μορφή—συνήθως PNG—διατηρώντας τη διάταξη, τις γραμματοσειρές και την οπτική πιστότητα. Το Aspose.Imaging για Java παρέχει μια ροή εργασίας με μία μέθοδο που διαχειρίζεται αυτή τη μετατροπή χωρίς την ανάγκη εξωτερικών εργαλείων, επιτρέποντας στους προγραμματιστές να ενσωματώσουν τη μετατροπή απευθείας στις εφαρμογές τους με ελάχιστο κώδικα.

## Γιατί να Χρησιμοποιήσετε το Aspose.Imaging για Java;
Το Aspose.Imaging υποστηρίζει **πάνω από 120 μορφές εξόδου** και μπορεί να rasterize αρχεία ODP πολλαπλών σελίδων χωρίς να φορτώνει ολόκληρο το έγγραφο στη μνήμη, μειώνοντας τη μέγιστη χρήση RAM έως και 70 % σε μεγάλες παρουσιάσεις. Η βιβλιοθήκη προσφέρει επίσης ενσωματωμένη διαχείριση γραμματοσειρών, εξαλείφοντας την ανάγκη για μηχανές rendering τρίτων.

## Προαπαιτούμενα
- **Libraries**: Aspose.Imaging for Java ≥ 25.5.  
- **JDK**: Version 8 or newer.  
- **IDE**: IntelliJ IDEA, Eclipse, or any Java‑compatible editor.  
- **Basic Knowledge**: Java I/O, object‑oriented programming, and image concepts.

## Οδηγίες Εγκατάστασης

### Maven
Προσθέστε την παρακάτω εξάρτηση στο `pom.xml` σας και εκτελέστε `mvn clean install`:

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

### Gradle
Συμπεριλάβετε τη βιβλιοθήκη στο αρχείο `build.gradle` σας και ανανεώστε το έργο:

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### Άμεση Λήψη
Κατεβάστε το πιο πρόσφατο JAR από το [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

## Βήματα Απόκτησης Άδειας
Για να ξεκλειδώσετε πλήρη λειτουργικότητα, εφαρμόστε προσωρινή ή μόνιμη άδεια:

1. **Δωρεάν Δοκιμή** – Δεν απαιτείται άδεια, περιορισμένες λειτουργίες.  
2. **Προσωρινή Άδεια** – Ζητήστε μία στην [Aspose website](https://purchase.aspose.com/temporary-license/).  
3. **Αγορά** – Αγοράστε συνδρομή ή μόνιμη άδεια από τη [Aspose purchase page](https://purchase.aspose.com/buy).

Αρχικοποιήστε τη βιβλιοθήκη με το αρχείο άδειας σας:

```java
License license = new License();
license.setLicense("path/to/your/license/file");
```

## Πώς να ορίσετε προσαρμοσμένο φάκελο γραμματοσειρών για τη μετατροπή ODP;
`FontSettings` είναι μια κλάση που διαχειρίζεται πόρους γραμματοσειρών για το Aspose.Imaging. Φορτώστε τις προσαρμοσμένες γραμματοσειρές σας πριν ξεκινήσει οποιαδήποτε επεξεργασία εικόνας. Αυτό εξασφαλίζει ότι κάθε διαφάνεια χρησιμοποιεί τις ακριβείς γραμματοσειρές που παρέχετε.

Ορίστε τη διαδρομή του φακέλου γραμματοσειρών χρησιμοποιώντας το `FontSettings` του Aspose.Imaging:

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.examples.Utils;

  String dataDir = Utils.getSharedDataDir() + "otg/";
  FontSettings.setFontsFolder(Path.combine(dataDir, "fonts"));
  ```

*Αγκύρωση ορισμού*: `FontSettings.setFontsFolder` ενημερώνει το Aspose.Imaging πού να ψάξει για γραμματοσειρές TrueType και OpenType στο σύστημα αρχείων.

## Πώς να απενεργοποιήσετε τις εναλλακτικές γραμματοσειρές του συστήματος κατά τη μετατροπή ODP;
Η απενεργοποίηση των εναλλακτικών του συστήματος αναγκάζει τη μηχανή απόδοσης να αγνοήσει τις γραμματοσειρές που είναι εγκατεστημένες στο λειτουργικό σύστημα, εξασφαλίζοντας ότι χρησιμοποιούνται μόνο οι γραμματοσειρές που παρέχετε. Αυτό εξαλείφει τις απρόσμενες αντικαταστάσεις γραμματοσειρών που μπορούν να αλλάξουν την οπτική εμφάνιση των διαφανειών σας.

Απενεργοποιήστε τις εναλλακτικές του συστήματος με την παρακάτω κλήση:

```java
  import com.aspose.imaging.FontSettings;

  FontSettings.setGetSystemAlternativeFont(false);
  ```

*Αγκύρωση ορισμού*: `FontSettings.setGetSystemAlternativeFont(false)` αναγκάζει τη μηχανή να χρησιμοποιεί μόνο τις γραμματοσειρές που βρίσκονται στον φάκελο που ορίσατε, εξαλείφοντας τις απρόσμενες αντικαταστάσεις.

## Πώς να εξάγετε ένα αρχείο ODP σε PNG με καθορισμένη γραμματοσειρά;
`RasterizationOptions` ορίζει πώς οι διανυσματικές σελίδες rasterize σε bitmap εικόνες. Συνδυάζοντας τη ρύθμιση γραμματοσειρών με τις ρυθμίσεις rasterization, μπορείτε να ελέγξετε DPI, χρώμα φόντου και μέγεθος σελίδας για κάθε εξαγόμενο PNG.

Εφαρμόστε τη μέθοδο εξαγωγής όπως φαίνεται παρακάτω:

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.Image;
  import com.aspose.imaging.imageoptions.OdgRasterizationOptions;
  import com.aspose.imaging.imageoptions.PngOptions;

  private static void exportToPng(String filePath, String defaultFontName, String outfileName) {
      FontSettings.setDefaultFontName(defaultFontName);
      try (Image document = Image.load(filePath)) {
          PngOptions saveOptions = new PngOptions();
          
          OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
          rasterizationOptions.setPageWidth(1000); // Set the page width for rendering
          rasterizationOptions.setPageHeight(1000);  // Set the page height for rendering

          saveOptions.setVectorRasterizationOptions(rasterizationOptions);
          document.save(outfileName, saveOptions);
      }
  }

  ```

*Αγκύρωση ορισμού*: Η κλάση `RasterizationOptions` ελέγχει DPI, μέγεθος σελίδας και χρώμα φόντου για τα παραγόμενα αρχεία PNG.

### Συνηθισμένα Πιθανά Προβλήματα & Λύσεις
- **Απουσία αρχείων γραμματοσειρών** – Επαληθεύστε ότι κάθε `.ttf` ή `.otf` που αναφέρεται στο ODP υπάρχει στον φάκελο που ορίσατε.  
- **Λανθασμένες διαδρομές αρχείων** – Χρησιμοποιήστε απόλυτες διαδρομές ή επιλύστε σχετικές διαδρομές σε σχέση με το `System.getProperty("user.dir")`.  
- **Ανεπαρκή δικαιώματα** – Βεβαιωθείτε ότι η διαδικασία Java μπορεί να διαβάσει το φάκελο γραμματοσειρών και να γράψει στον φάκελο εξόδου.

## Πρακτικές Εφαρμογές
1. **Διαφάνειες με συνεπή εταιρική ταυτότητα** – Εξάγετε παρουσιάσεις ως PNG για δημοσίευση στο web διατηρώντας τις εταιρικές γραμματοσειρές.  
2. **Αυτοματοποιημένη δημιουργία αναφορών** – Μετατρέψτε κάθε διαφάνεια σε εικόνα για ένταξη σε PDF αναφορές ή ενημερωτικά email.  
3. **Δημιουργία αρχείου κληρονομιάς** – Αποθηκεύστε το περιεχόμενο ODP ως PNG για να εξασφαλίσετε μελλοντική προσβασιμότητα χωρίς την ανάγκη προβολέων ODP.

## Σκέψεις Απόδοσης
- Χρησιμοποιήστε την πιο πρόσφατη έκδοση του Aspose.Imaging για να επωφεληθείτε από βελτιώσεις rasterization πολλαπλών νημάτων (έως 2× ταχύτερη σε CPU 8 πυρήνων).  
- Τυλίξτε την επεξεργασία εικόνας σε μπλοκ try‑with‑resources για να εγγυηθείτε την έγκαιρη απελευθέρωση των εγγενών πόρων.  
- Προσαρμόστε τις `RasterizationOptions` (π.χ., χαμηλότερο DPI) όταν επεξεργάζεστε χιλιάδες διαφάνειες για να ισορροπήσετε την ποιότητα και τη χρήση μνήμης.

## Συχνές Ερωτήσεις

**Q: Ποια είναι η ελάχιστη έκδοση Java που απαιτείται;**  
A: Το Aspose.Imaging για Java λειτουργεί με JDK 8 και νεότερα· το JDK 11 συνιστάται για μακροπρόθεσμη υποστήριξη.

**Q: Μπορώ να μετατρέψω μόνο επιλεγμένες διαφάνειες;**  
A: Ναι, ορίστε `rasterizationOptions.setPageNumber(specificSlideIndex)` πριν καλέσετε `save`.

**Q: Πώς να διαχειριστώ αρχεία ODP με κωδικό πρόσβασης;**  
A: Φορτώστε το αρχείο με `LoadOptions` που περιλαμβάνει τον κωδικό πρόσβασης, έπειτα προχωρήστε με τις ίδιες ρυθμίσεις γραμματοσειρών.

**Q: Επηρεάζει η απενεργοποίηση των γραμματοσειρών του συστήματος την απόδοση;**  
A: Βελτιώνει ελαφρώς την ταχύτητα επειδή η μηχανή παραλείπει την αναζήτηση των γραμματοσειρών του συστήματος, κάτι που είναι εμφανές σε μηχανήματα με μεγάλες συλλογές γραμματοσειρών.

**Q: Πού μπορώ να βρω περισσότερα παραδείγματα κώδικα;**  
A: Εξερευνήστε την επίσημη [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/) για επιπλέον σενάρια όπως μαζική μετατροπή και μετασχηματισμούς εικόνας.

## Πρόσθετοι Πόροι
- [Aspose.Imaging για Java εκδόσεις](https://releases.aspose.com/imaging/java/)  
- [Aspose.Imaging Εκδόσεις](https://releases.aspose.com/imaging/java/)  
- [Ξεκινήστε τη Δωρεάν Δοκιμή](https://releases.aspose.com/imaging/java/)  
- [Τεκμηρίωση Aspose.Imaging](https://reference.aspose.com/imaging/java/)  
- [Φόρουμ Aspose.Imaging](https://forum.aspose.com/c/imaging/14)  
- [Αγορά Άδειας Aspose](https://purchase.aspose.com/buy)  
- [Αίτηση για Προσωρινή Άδεια](https://purchase.aspose.com/temporary-license/)  

---

**Τελευταία Ενημέρωση:** 2026-06-28  
**Δοκιμάστηκε Με:** Aspose.Imaging για Java 25.5  
**Author:** Aspose

## Σχετικά Μαθήματα

- [Μετατροπή ODG σε PNG με Aspose.Imaging για Java: Πλήρης Οδηγός](/imaging/java/format-conversion-export/convert-odg-to-png-aspose-imaging-java/)
- [Αποτελεσματική Μετατροπή Εικόνας σε Java με Aspose.Imaging: Πλήρης Οδηγός](/imaging/java/format-conversion-export/mastering-image-conversion-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}