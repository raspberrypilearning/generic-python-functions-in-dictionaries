### Χρήση συναρτήσεων σε λεξικά

Τα λεξικά μπορούν να αποθηκεύσουν όλους τους τύπους δεδομένων, γεγονός που τα καθιστά χρήσιμα για πολλά πράγματα.

Μπορείς να αποθηκεύσεις προσαρμοσμένες ή έτοιμες συναρτήσεις και μεθόδους μέσα σε ένα λεξικό. Υπάρχουν πολλές φορές που αυτό θα φανεί χρήσιμο, για παράδειγμα όταν, σε άλλη γλώσσα προγραμματισμού, θα χρησιμοποιούσες μια δήλωση **CASE**.

Ρίξε μια ματιά στον κώδικα παρακάτω. Είναι ένα παράδειγμα ενός συστήματος μενού, όπου εκτελούνται διάφορες συναρτήσεις ανάλογα με το αν ο χρήστης πληκτρολογεί τις τιμές 1, 2 ή 3.

```python
def option1():
  print('Επέλεξες 1')

def option2():
  print('Επέλεξες 2')

def option3():
  print('Επέλεξες 3')

choice = input():

if choice == '1':
  option1()
elif choice == '2':
  option2()
elif choice == '3':
  option3()
```

Αντί να χρησιμοποιήσεις δηλώσεις `if` και `elif`, μπορείς να χρησιμοποιήσεις ένα λεξικό συναρτήσεων. Για παράδειγμα:

```python
options = {'1': option1, '2': option2, '3': option3}
```

Αυτό έχει τώρα τις πιθανές εισόδους του χρήστη ως κλειδιά και τις συναρτήσεις που καλούνται ως τιμές. Με μια επιπλέον γραμμή, μπορεί να ζητηθεί η επιλογή του χρήστη και να καλείται η κατάλληλη συνάρτηση.

```python
options[input('Επίλεξε 1, 2 or 3 ')]()
```

Έτσι, ο ολοκληρωμένος κώδικας μοιάζει ως εξής:

```python
def option1():
  print('Επέλεξες 1')


def option2():
  print('Επέλεξες 2')


def option3():
  print('Επέλεξες 3')


options = {'1': option1, '2': option2, '3': option3}

options[input('Επίλεξε 1, 2 or 3 ')]()
```
