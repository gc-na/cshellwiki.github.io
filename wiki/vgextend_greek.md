# [Λίνουξ] Bash vgextend Χρήση: Επέκταση ενός Volume Group

## Overview
Η εντολή `vgextend` χρησιμοποιείται για την επέκταση ενός Volume Group (VG) σε Linux, προσθέτοντας επιπλέον Physical Volumes (PVs) σε αυτό. Αυτό επιτρέπει την αύξηση της διαθέσιμης χωρητικότητας του Volume Group.

## Usage
Η βασική σύνταξη της εντολής είναι η εξής:

```bash
vgextend [options] [arguments]
```

## Common Options
- `-d`, `--debug`: Ενεργοποιεί την εκτύπωση πληροφοριών για την αποσφαλμάτωση.
- `-h`, `--help`: Εμφανίζει την βοήθεια για την εντολή.
- `-n`, `--no-really`: Αποτρέπει την εκτέλεση της εντολής, χρησιμοποιείται για δοκιμές.
- `-v`, `--verbose`: Εμφανίζει λεπτομερείς πληροφορίες κατά την εκτέλεση.

## Common Examples
1. **Επέκταση ενός Volume Group με ένα Physical Volume:**
   ```bash
   vgextend my_volume_group /dev/sdb1
   ```

2. **Επέκταση ενός Volume Group με πολλαπλά Physical Volumes:**
   ```bash
   vgextend my_volume_group /dev/sdb1 /dev/sdc1
   ```

3. **Επέκταση ενός Volume Group και εμφάνιση λεπτομερειών:**
   ```bash
   vgextend -v my_volume_group /dev/sdb1
   ```

## Tips
- Βεβαιωθείτε ότι τα Physical Volumes που προσθέτετε είναι διαθέσιμα και σωστά διαμορφωμένα.
- Χρησιμοποιήστε την επιλογή `-v` για να παρακολουθείτε την πρόοδο της εντολής και να εντοπίζετε τυχόν σφάλματα.
- Πριν από την επέκταση, ελέγξτε την κατάσταση του Volume Group με την εντολή `vgdisplay` για να βεβαιωθείτε ότι είναι έτοιμο για επέκταση.