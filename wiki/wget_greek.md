# [Διανομή] Debian Almquist Shell (dash) wget Χρήση: Λήψη αρχείων από το διαδίκτυο

## Overview
Η εντολή `wget` είναι ένα εργαλείο γραμμής εντολών που χρησιμοποιείται για τη λήψη αρχείων από το διαδίκτυο. Υποστηρίζει διάφορα πρωτόκολλα, όπως HTTP, HTTPS και FTP, και είναι ιδανικό για την αυτοματοποίηση της διαδικασίας λήψης.

## Usage
Η βασική σύνταξη της εντολής `wget` είναι η εξής:

```bash
wget [options] [arguments]
```

## Common Options
- `-O <file>`: Καθορίζει το όνομα του αρχείου που θα αποθηκευτεί.
- `-c`: Συνεχίζει μια διακοπείσα λήψη.
- `-q`: Λειτουργία σιωπής, δεν εκτυπώνει μηνύματα.
- `--limit-rate=<rate>`: Περιορίζει την ταχύτητα λήψης.
- `-r`: Ενεργοποιεί την αναδρομική λήψη.

## Common Examples
- Λήψη ενός αρχείου:
  ```bash
  wget http://example.com/file.zip
  ```

- Λήψη ενός αρχείου με καθορισμένο όνομα:
  ```bash
  wget -O myfile.zip http://example.com/file.zip
  ```

- Συνεχίζοντας μια διακοπείσα λήψη:
  ```bash
  wget -c http://example.com/largefile.zip
  ```

- Λήψη αρχείων από μια ιστοσελίδα αναδρομικά:
  ```bash
  wget -r http://example.com/directory/
  ```

- Περιορισμός της ταχύτητας λήψης:
  ```bash
  wget --limit-rate=200k http://example.com/file.zip
  ```

## Tips
- Χρησιμοποιήστε την επιλογή `-q` για να μειώσετε την έξοδο κατά τη λήψη μεγάλων αρχείων.
- Για αναδρομική λήψη, βεβαιωθείτε ότι έχετε άδεια να κατεβάσετε περιεχόμενο από τον ιστότοπο.
- Ελέγξτε τα δικαιώματα του αρχείου μετά τη λήψη, ειδικά αν πρόκειται να το εκτελέσετε.