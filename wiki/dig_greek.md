# [Δημιουργία] Debian Almquist Shell (dash) dig <Χρήση: Εύρεση πληροφοριών DNS>

## Overview
Η εντολή `dig` (Domain Information Groper) χρησιμοποιείται για την αναζήτηση πληροφοριών σχετικά με το Domain Name System (DNS). Επιτρέπει στους χρήστες να ελέγχουν την ανάλυση ονομάτων τομέα και να αποκτούν λεπτομέρειες για διάφορους τύπους εγγραφών DNS.

## Usage
Η βασική σύνταξη της εντολής `dig` είναι η εξής:

```bash
dig [options] [arguments]
```

## Common Options
- `@server`: Καθορίζει τον DNS server που θα χρησιμοποιηθεί για την αναζήτηση.
- `-t type`: Καθορίζει τον τύπο της εγγραφής που θέλετε να αναζητήσετε (π.χ. A, MX, TXT).
- `+short`: Εμφανίζει μια σύντομη μορφή της απάντησης.
- `+trace`: Ακολουθεί την πορεία της αναζήτησης για να δείξει πώς φτάνει στην απάντηση.

## Common Examples
### 1. Αναζήτηση διεύθυνσης IP για ένα τομέα
```bash
dig example.com
```

### 2. Αναζήτηση συγκεκριμένου τύπου εγγραφής (π.χ. MX)
```bash
dig -t MX example.com
```

### 3. Χρήση συγκεκριμένου DNS server
```bash
dig @8.8.8.8 example.com
```

### 4. Σύντομη μορφή απάντησης
```bash
dig +short example.com
```

### 5. Ακολουθία αναζήτησης
```bash
dig +trace example.com
```

## Tips
- Χρησιμοποιήστε την επιλογή `+short` για γρήγορη και καθαρή απάντηση, ειδικά όταν χρειάζεστε μόνο τις διευθύνσεις IP.
- Δοκιμάστε διαφορετικούς τύπους εγγραφών για να αποκτήσετε πλήρη εικόνα των πληροφοριών DNS ενός τομέα.
- Εάν έχετε προβλήματα με την ανάλυση, δοκιμάστε να χρησιμοποιήσετε έναν διαφορετικό DNS server, όπως ο Google DNS (8.8.8.8).