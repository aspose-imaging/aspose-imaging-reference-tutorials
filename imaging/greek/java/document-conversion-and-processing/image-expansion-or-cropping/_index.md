---
date: 2026-05-03
description: Μάθετε πώς να περικόψετε μια εικόνα με το Aspose.Imaging για Java, συμπεριλαμβανομένης
  της περικοπής σε ορθογώνιο και της επέκτασης του καμβά. Οδηγός βήμα‑βήμα για προγραμματιστές.
keywords:
- how to crop image
- crop and expand image
- aspose imaging crop
- java image processing tutorial
- expand image canvas java
linktitle: Ανάπτυξη ή περικοπή εικόνας
second_title: Aspose.Imaging Java Image Processing API
title: Πώς να περικόψετε μια εικόνα σε ορθογώνιο με το Aspose.Imaging για Java
url: /el/java/document-conversion-and-processing/image-expansion-or-cropping/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να Κόψετε Εικόνα σε Ορθογώνιο με Aspose.Imaging για Java

Στον σημερινό ταχύτατα εξελισσόμενο ψηφιακό κόσμο, η γνώση **πώς να κόψετε εικόνα** γρήγορα και αξιόπιστα αποτελεί βασική απαίτηση για οποιοδήποτε Java‑βασισμένο ροή εργασίας εικόνας. Είτε περικόπτετε φωτογραφίες που ανέβηκαν από χρήστες για μια διαδικτυακή υπηρεσία, είτε δημιουργείτε συνεπείς μικρογραφίες για έναν κατάλογο e‑commerce, είτε προετοιμάζετε πόρους για μια καμπάνια μάρκετινγκ, το Aspose.Imaging για Java παρέχει ένα καθαρό, υψηλής απόδοσης API για να ολοκληρώσετε τη δουλειά. Σε αυτό το tutorial θα περάσουμε βήμα‑βήμα τη διαδικασία περικοπής ενός ορθογωνίου από μια εικόνα και την επέκταση του καμβά της εικόνας — ιδανικό για όποιον θέλει να κυριαρχήσει τις τεχνικές επεξεργασίας εικόνας σε Java.

## Γρήγορες Απαντήσεις
- **Ποια βιβλιοθήκη είναι η καλύτερη για περικοπή εικόνας Java;** Aspose.Imaging for Java.  
- **Μπορώ να περικόψω σε οποιοδήποτε ορθογώνιο;** Ναι – ορίστε οποιοδήποτε X, Y, πλάτος και ύψος.  
- **Χρειάζομαι άδεια για ανάπτυξη;** Μια δωρεάν δοκιμή λειτουργεί για δοκιμές· απαιτείται άδεια για παραγωγή.  
- **Είναι δυνατή η επέκταση μιας εικόνας;** Απόλυτα – μπορείτε να αυξήσετε το μέγεθος του καμβά πριν την περικοπή.  
- **Ποια έκδοση Java υποστηρίζεται;** Java 8 και νεότερες.

## Τι είναι η «crop image to rectangle»;
Η περικοπή μιας εικόνας σε ορθογώνιο σημαίνει την εξαγωγή ενός υπο‑τμήματος του αρχικού bitmap που ορίζεται από μια ορθογώνια περιοχή (X‑offset, Y‑offset, πλάτος, ύψος). Το υπόλοιπο της εικόνας απορρίπτεται, αφήνοντάς σας με μια νέα, μικρότερη εικόνα που περιέχει μόνο την περιοχή που χρειάζεστε.

## Γιατί να χρησιμοποιήσετε Aspose.Imaging για Java;
- **Χωρίς εξωτερικές εξαρτήσεις** – pure Java, works on any platform.  
- **Ευρεία υποστήριξη μορφών** – JPEG, PNG, BMP, TIFF, and more.  
- **Αποθήκευση υψηλής απόδοσης** – `cacheData()` reduces I/O overhead.  
- **Απλό API** – one‑line calls for loading, defining a rectangle, and saving.

## Προαπαιτούμενα
- **Java Development Environment** – JDK 8+ installed and configured.  
- **Aspose.Imaging for Java** – download from the [website](https://releases.aspose.com/imaging/java/).  
- **Basic Java Knowledge** – familiarity with classes, try‑with‑resources, and file paths.  
- **Image to Work With** – any JPEG/PNG you’d like to crop or expand.

## Εισαγωγή Πακέτων
First, point the code to the folder that holds your source images. This snippet stays unchanged from the original tutorial.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ConvertingImages/";
```

Αντικαταστήστε το `"Your Document Directory"` με την απόλυτη διαδρομή στο μηχάνημά σας.

## Βήμα 1: Φόρτωση της Εικόνας
Loading the image is the foundation for any manipulation. We also call `cacheData()` to keep the bitmap in memory for fast subsequent operations.

```java
try (RasterImage rasterImage = (RasterImage) Image.load(dataDir + "aspose-logo.jpg"))
{
    rasterImage.cacheData();
}
```

> **Pro tip:** Use a `try‑with‑resources` block (as shown) to ensure the image is automatically closed, preventing memory leaks.

## Βήμα 2: Ορισμός της Περιοχής για Περικοπή
Here we create a `Rectangle` that represents the exact area you want to keep. The rectangle can start outside the original bounds – Aspose.Imaging will automatically expand the canvas (useful for the **expand image canvas java** scenario).

```java
// Create an instance of Rectangle class and define X, Y, Width, and Height of the rectangle
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

- **X / Y** – negative values shift the rectangle left/up, causing the canvas to expand.  
- **Width / Height** – size of the cropped region.

## Βήμα 3: Αποθήκευση της Περικομμένης (ή Επεκταμένης) Εικόνας
Finally, write the result to disk. The `save` method takes the destination path, image format options, and the rectangle we defined.

```java
rasterImage.save("Your Document Directory" + "Grayscaling_out.jpg", new JpegOptions(), destRect);
```

The output file `Grayscaling_out.jpg` now contains the **crop image to rectangle** result. If the rectangle extended beyond the original image, the extra area is filled with a default background (transparent for PNG, black for JPEG).

## Πώς να Κόψετε Εικόνα με Aspose.Imaging για Java
This section reiterates the core steps in a concise checklist so you can quickly reference them while coding:

1. **Set the data directory** – point to the folder containing source images.  
2. **Load the image** with `Image.load()` and call `cacheData()`.  
3. **Create a `Rectangle`** that defines the crop region (or canvas expansion).  
4. **Save** the new image using `rasterImage.save()` and pass the rectangle.

## Περικοπή και Επέκταση Εικόνας – Πραγματικές Περιπτώσεις Χρήσης
| Σενάριο | Γιατί Είναι Σημαντικό |
|----------|----------------|
| **Δημιουργία μικρογραφιών** | Γρήγορη εξαγωγή κεντρικής περιοχής για συνεπή μέγεθος. |
| **Περικοπή εικόνας προφίλ χρήστη** | Εξασφάλιση τετράγωνης ή ορθογώνιας περιοχής avatar. |
| **Επέκταση καμβά πριν την προσθήκη υδατογραφήματος** | Προσθήκη χώρου γύρω από την εικόνα χωρίς παραμόρφωση του αρχικού. |
| **Μαζική επεξεργασία σαρωμένων εγγράφων** | Περικοπή περιθωρίων σε μία διεργασία. |

## Επίλυση Προβλημάτων & Συμβουλές
- **Image not loading?** Verify the file path and ensure the image format is supported.  
- **Unexpected black borders after expansion?** Set a background color in `JpegOptions` or use PNG for transparency.  
- **Performance concerns with large images?** Increase the Java heap size (`-Xmx`) or process images in smaller batches.  
- **Common pitfall:** Forgetting to call `cacheData()` can lead to slower I/O on subsequent operations.

## Συχνές Ερωτήσεις

**Q: What image formats does Aspose.Imaging for Java support?**  
A: JPEG, PNG, BMP, TIFF, GIF, ICO, PSD, and many more. See the official docs for the full list.

**Q: Can I perform other image manipulations with Aspose.Imaging for Java?**  
A: Absolutely! Resizing, rotation, filtering, and format conversion are all available.

**Q: Is Aspose.Imaging for Java suitable for web applications?**  
A: Yes. The library is thread‑safe and works well in servlet containers and Spring Boot services.

**Q: How can I get support for Aspose.Imaging for Java?**  
A: Visit the [forum](https://forum.aspose.com/) for community help, or open a support ticket with a valid license.

**Q: Is there a free trial available for Aspose.Imaging for Java?**  
A: Yes, you can explore the library with a free trial. Download it from [here](https://releases.aspose.com/).

## Συμπέρασμα
You’ve now learned **how to crop image** to a rectangle and even **expand image canvas** using the powerful Aspose.Imaging API. By mastering these fundamentals you can build robust image‑processing pipelines, improve UI responsiveness, and deliver polished visual content across any Java application.

---

**Τελευταία Ενημέρωση:** 2026-05-03  
**Δοκιμή Με:** Aspose.Imaging for Java 24.11 (latest at time of writing)  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}