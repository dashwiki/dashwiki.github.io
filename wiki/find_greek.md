# [Διανομή] Debian Almquist Shell (dash) find χρήση: [εύρεση ονομάτων αρχείων]

## Επισκόπηση
Η εντολή `find` χρησιμοποιείται για την αναζήτηση αρχείων και καταλόγων σε ένα σύστημα αρχείων με βάση διάφορα κριτήρια, όπως το όνομα, το μέγεθος, την ημερομηνία τροποποίησης και άλλα χαρακτηριστικά.

## Χρήση
Η βασική σύνταξη της εντολής είναι η εξής:

```
find [options] [arguments]
```

## Κοινές Επιλογές
- `-name`: Αναζητά αρχεία με συγκεκριμένο όνομα.
- `-type`: Καθορίζει τον τύπο του αρχείου (π.χ. `f` για κανονικά αρχεία, `d` για καταλόγους).
- `-mtime`: Αναζητά αρχεία που τροποποιήθηκαν σε συγκεκριμένο χρονικό διάστημα.
- `-size`: Αναζητά αρχεία με συγκεκριμένο μέγεθος.
- `-exec`: Εκτελεί μια εντολή σε κάθε αρχείο που βρέθηκε.

## Κοινά Παραδείγματα
- Αναζήτηση αρχείων με συγκεκριμένο όνομα:
    ```bash
    find /path/to/directory -name "file.txt"
    ```

- Αναζήτηση καταλόγων:
    ```bash
    find /path/to/directory -type d -name "folder_name"
    ```

- Αναζήτηση αρχείων που τροποποιήθηκαν τις τελευταίες 7 ημέρες:
    ```bash
    find /path/to/directory -mtime -7
    ```

- Αναζήτηση αρχείων μεγαλύτερων από 1GB:
    ```bash
    find /path/to/directory -size +1G
    ```

- Εκτέλεση εντολής σε κάθε αρχείο που βρέθηκε:
    ```bash
    find /path/to/directory -name "*.log" -exec rm {} \;
    ```

## Συμβουλές
- Χρησιμοποιήστε την επιλογή `-print` για να εμφανίσετε τα αποτελέσματα της αναζήτησης, αν δεν είναι η προεπιλεγμένη συμπεριφορά.
- Για να αποφύγετε την αναζήτηση σε συγκεκριμένους καταλόγους, μπορείτε να χρησιμοποιήσετε την επιλογή `-prune`.
- Ελέγξτε προσεκτικά τις εντολές που εκτελείτε με `-exec`, καθώς μπορεί να επηρεάσουν πολλά αρχεία.