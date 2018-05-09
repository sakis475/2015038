# ΤΕΛΙΚΗ ΑΝΑΦΟΡΑ - Τεχνολογία Λογισμικού
Πιπλικάτσης Αθανάσιος
Π2015038
3ο έτος

## Σύνοψη

Στο μάθημα Τεχνολογία λογισμικού κληθήκαμε να επιλέξουμε και να δουλέψουμε πάνω σε μια εργασία από τις διαθέσιμες που υπήρχαν. Εγώ διάλεξα την  ["Οπτικοποίηση δεδομένων χορηγιών (UK)"](https://github.com/ioniodi/D3js-uk-political-donations) . Στη παρόν σελίδα γίνονται κάποιες αναφορές σχετικά με το έργο τα εργαλεία τις τεχνικές σχετικά με την εργασία. Τα οποία κατά κύριο λόγω είναι βασισμένα στα προηγούμενα παραδοτέα.


## Σύντομη εισαγωγή

Μια τέτοια σελίδα σκοπό έχει την παρουσίασει στατιστικών δεδομένων καθώς και πορισμάτων που μπορεί να προκύψει από αυτά. Η συγκεκριμένη σελίδα παρουσιάζει γραφικά κάποιες χρηματικές δωρεές εταιριών, ομάδων, προσώπων προς τα τρία κόμματα της Αγγλίας. Καθώς και επιχειρεί να δώσει και κάποιες πληροφορίες. Όπως το ποσοστό δημόσιων και ιδιωτικών συνεισφορών, σύνολο χρημάτων ανά κατηγορία κτλπ... Για την γραφική αναπαράσταση έχει χρησιμοποιηθεί η βιβλιοθήκη D3.js ([Data Driven Documents](https://d3js.org/)) που ουσιαστικά είναι ένα συνονθύλευμα διαφορετικών βιβλιοθηκών.  Η βιβλιοθήκη d3 έχει κάνει εφικτή και πιο εύκολη τη γραφική αναπαράσταση στοιχείων. Επιπλέον μπορεί να φέρει τα δεδομένα σε τέτοια μορφή που να είναι πιο ελκυστικά στο μάτι του χρήστη, άρα λογικό και επακόλουθο είναι να ανέβει και η επισκεψιμότητα της εκάστοτε σελίδας. Στη συνέχεια γίνεται μια ανάλυση όλων των έργων που υλοποιήθηκαν και των μέσων που διετέλεσαν στην ολοκλήρωση τους.


## Σύντομη ανάλυση σχετικών έργων, εργαλείων και μέθοδος, τεχνικές ανάπτυξης

**Παραδοτέο 1**

Ο σύνδεσμος της εφαρμογής με pretty format **https://sakis475.github.io/D3js-uk-political-donations** 
Πραγματοποιήθηκε με το config gh-pages αρχείο [_config.yml](https://github.com/sakis475/D3js-uk-political-donations/blob/paradoteo1/_config.yml)

Τα χρώματα των κύκλων καθώς και τα επιμέρους 3 πεδία της ομαδοποίησης Split by party έχουν αλλάξει σε κόκκινο, πράσινο, μπλε.
Στο αρχείο [chart.js](https://github.com/sakis475/D3js-uk-political-donations/blob/paradoteo1/chart.js) *line- 28* για τους κύκλους και [style.css](https://github.com/sakis475/D3js-uk-political-donations/blob/paradoteo1/style.css) *line-166-179* για τα πεδία ομαδοποίησης.

Για να ακούγετε ήχος όταν πατιέτε ένα κουμπί, πρόσθεσα το *soundButton.mp3* 
και το event onclick [index.html](https://github.com/sakis475/D3js-uk-political-donations/blob/paradoteo1/index.html) *line-40-60*

Για να ανοίγει google search, τον donator, σε νέο παράθυρο όταν πατιέτε ένας κύκλος. Στο αρχείο [chart.js](https://github.com/sakis475/D3js-uk-political-donations/blob/paradoteo1/chart.js) προσθέθηκε νέα function με όνομα *mouseClick* *(line-448)* και γίνεται trigger όταν κάνουμε click σε κάποιο κύκλο *(line-116)*

Για να γίνετε μεγένθυνση σε κείμενο πρόσθεσα css ιδιότητες για κάθε element του html, [style.css](https://github.com/sakis475/D3js-uk-political-donations/blob/paradoteo1/style.css) *(line-8-115)*
![enter image description here](https://github.com/sakis475/sw/blob/paradoteo1/projects/2015038/zoomtext.png?raw=true)

Όταν ο χρήστης έχει το ποντίκι πάνω από ένα κύκλο για πάνω από 0,3 δεύτερα ακούγετε το όνομα του donator και το ποσό της δωρεάς του. Για αυτή τη λειτουργηκότητα χρησιμοποίησα μια δωρεάν βιβλιοθήκη: http://www.masswerk.at/mespeak/ 
Και προσθέθηκε ο κώδικας στο [chart.js](https://github.com/sakis475/D3js-uk-political-donations/blob/paradoteo1/chart.js) *(line-421-424 & line-441-444)*

Τέλος προσθέθηκε ένα επιπλέον view, το Split by amount, όπου χωρίζω τις δωρεές σε 5 τάξης μεγέθους και δίπλα αναφέρω το ποσοστό του αθροίσματος των δωρεών σε σχέση με το συνολικό ποσό της εκάστοτε τάξης μεγέθους που ανήκει σε ένα κόμμα. Για λόγους απλότητας υπολόγισα μια φορά τα στοιχεία με sql και τα έβαλα hard-typed στο html αρχείο, έτσι και αλλιώς τα δεδομένα δεν αλλάζουν οπότε δεν χρειάζετε να υπολογίζονται κάθε φορά που φορτώνετε η σελίδα.
![](https://github.com/sakis475/sw/blob/paradoteo1/projects/2015038/splitbyamount.png?raw=true)

To csv αρχείο [2015038.csv](https://github.com/ioniodi/D3js-uk-political-donations/blob/master/participants/2015038.csv)

Το pull request στο κοινό αποθετήριο του κώδικα: 
https://github.com/ioniodi/D3js-uk-political-donations/pull/32

**Παραδοτέο 2**

Υλοποιήθηκε η δυναμική επέκταση των δωρητών (Lastly Visited). Σε κάθε mouseOver κύκλου επεκτείνεται δυναμικά μια κάθετη λίστα από τον πιο πρόσφατο μέχρι τον παλαιότερο δωρητή. Η λίστα κρατάει μάξιμουμ 12 δωρητές και μεταθέτει το δωρητή στην κορυφή σε περίπτωση που υπάρχει ήδη στη λίστα.

![enter image description here](https://github.com/sakis475/sw/blob/paradoteo2/projects/2015038/dynPic.png?raw=true)

Στο αρχείο [chart.js](https://github.com/sakis475/D3js-uk-political-donations/blob/paradoteo2/chart.js) στη γραμμή 416-447 προστέθηκε κώδικας για αναγνώριση έγκυρου url και προσθήκης εικονιδίου στη λίστα.
Έπειτα στη γραμμή 517 γίνεται το "render" της Lastly Visited λίστας.

Διαπιστώθηκε πρόβλημα με το Chrome όσο αφορά τη meSpeak(φωνητική λειτουργία), κάποιες φορές δεν παίζει ο ήχος επειδή δεν το επιτρέπει το chrome. Αλλά με το Firefox δουλεύει μια χαρά.

Τέλος φτιάχτηκε το text animation του profil μου όπως φαίνεται εδώ στη θέση 31
https://sakis475.github.io/D3js-uk-political-donations/participants/

![enter image description here](https://raw.githubusercontent.com/sakis475/sw/paradoteo2/projects/2015038/logotipo.png)

στο index αρχείο έχω χρησιμοποιήσει τη θέση 31, 
ο κώδικας στο προσωπικό μου αποθετήριο:
[https://github.com/sakis475/.../participants/index.html](https://github.com/sakis475/D3js-uk-political-donations/blob/paratodeo2_profileAnimation/participants/index.html)

## Συμπεράσματα

Εν συντομία, έχουν πραγματοποιηθεί πλήθος αλλαγών/βελτιώσεων, που κυμαίνονται από μικροαλλαγές, βοηθητικά εργαλεία για ευπαθείς ομάδες (φωνητικές λειτουργίες, μεγεθυντικός φακός) μέχρι και προσθήκη δυναμικής λίστας πρόσφατης επισκεψιμότητας δωρητών. Σκοπός ήταν να φέρουν τη σελίδα σε μια καινούργια κατάσταση αυξημένης λειτουργικότητας και καλαισθησίας. Επιπλέον έχει προσθεθεί και νέα ομαδοποίηση δεδομένων ανάλογα τον τύπο δωρητή, προσφέροντας περισσότερη πληροφορία για τον αναγνώστη.
