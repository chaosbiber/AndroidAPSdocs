Καλώς ήρθατε στην τεκμηρίωση AndroidAPS
==============================================

AndroidAPS είναι ένα open source εφαρμογή για τους ανθρώπους που ζουν με ινσουλίνο-εξαρτώμενο διαβήτη, η οποία ενεργεί ως ένα τεχνητό πάγκρεας system (APS) σε Google Android smartphones. Τα κύρια συστατικά είναι διαφορετικοί αλγόριθμοι λογισμικού openAPS που στοχεύουν να κάνουν ό, τι κάνει το ζωντανό πάγκρεας: διατηρώντας τα επίπεδα του σακχάρου στο αίμα μέσα σε υγιή όρια χρησιμοποιώντας αυτοματοποιημένη δοσολογία ινσουλίνης (AID). Επιπλέον, χρειάζεστε τουλάχιστον μια υποστηριζόμενη από την FDA / CE εγκεκριμένη αντλία ινσουλίνης και έναν συνεχή μετρητή γλυκόζης. 

Η εφαρμογή ΔΕΝ χρησιμοποιεί αυτο-μάθηση στην τεχνητή νοημοσύνη. Αντ 'αυτού, οι υπολογισμοί του AndroidAPS βασίζονται στον ατομικό αλγόριθμο δοσολογίας και την πρόσληψη υδατανθράκων που ο χρήστης θέτει χειροκίνητα στο προφίλ θεραπείας του, αλλά επαληθεύονται από το σύστημα για λόγους ασφαλείας. 

Η εφαρμογή δεν παρέχεται στο Google Play - πρέπει να το κατασκευάσετε από τον πηγαίο κώδικα μόνοι σας για νομικούς λόγους.

Κύρια συστατικά είναι:

.. εικόνα::../images/modules-female.png
  :alt: Συστατικά

Για περισσότερες λεπτομέρειες, παρακαλούμε διαβάστε εδώ.

Ξεκινώντας
----------------
.. toctree::
   :maxdepth: 1
   :glob:
   
   Πρώτα η ασφάλεια <./Getting-Started/Safety-first.rst>
   Τι είναι ένα κλειστό σύστημα κυκλώματος <./Getting-Started/ClosedLoop.rst>
   Τι είναι ένα κλειστό σύστημα κυκλώματος με AndroidAPS <./Getting-Started/WhatisAndroidAPS.rst>  
   Wiki ενημερώσεις και αλλαγές <./Getting-Started/WikiUpdate.rst>
   
   
* `Τι χρειάζομαι 
-----------------------------------------
.. toctree::
   :maxdepth: 1
   :glob:
   
   Module <./Module/module.rst>

   
Πώς να Εγκαταστήσετε AndroidAPS
------------
.. toctree::
   :maxdepth: 1
   :glob:

   Χτίζοντας το APK <./Installing-AndroidAPS/Building-APK.md>
   Ενημέρωση σε νέα έκδοση ή υποκατάστημα <./Installing-AndroidAPS/Update-to-new-version.md>
   Install git <./Installing-AndroidAPS/git-install.rst>
   Troubleshooting Android Studio <./Installing-AndroidAPS/troubleshooting_androidstudio.rst>
   Release notes <./Installing-AndroidAPS/Releasenotes.rst>
   Dev υποκατάστημα <./Installing-AndroidAPS/Dev_branch.md>
   
   
Ρυθμίσεις συστατικών
---------------
.. toctree::
   :maxdepth: 1
   :glob:
   
   CGM/FGM <./Configuration/BG-Source.rst>
   xDrip Ρυθμίσεις <./Configuration/xdrip.md>
   Αντλίες <./Hardware/pumps.rst>
   Τηλέφωνα <./Hardware/Phoneconfig.rst>
   Ρύθμιση Nightscout <./Installing-AndroidAPS/Nightscout.md>
   Smartwatch  <./Hardware/Smartwatch.rst>
   

Ρύθμιση παραμέτρων 
---------------
.. toctree::
   :maxdepth: 1
   :glob:
   
   Config builder <./Configuration/Config-Builder.md>
   Προτιμήσεις <./Configuration/Preferences.md>
   
   
AndroidAPS Χρήση
------------
.. toctree::
   :maxdepth: 1
   :glob:
    
   AndroidAPS οθόνες <./Getting-Started/Screenshots.md>
   Στόχοι <./Usage/Objectives.rst>
   OpenAPS χαρακτηριστικά <./Usage/Open-APS-features.md>   
   Υπολογιστής COB <./Usage/COB-calculation.rst>
   Ανίχνευση ευαισθησίας <./Configuration/Sensitivity-detection-and-COB.md>
   Αλλαγή προφίλ <./Usage/Profiles.md>
   Προσωρινοί στόχοι <./Usage/temptarget.md>   
   Εκτεταμένη υδατάνθρακες <./Usage/Extended-Carbs.md>
   Αυτοματοποίηση <./Usage/Automation.rst>
  
 
Γενικές Συμβουλές 
---------------------
.. toctree::
   :maxdepth: 1
   :glob:
   
   Διασχίζοντας ζώνες ώρας με αντλίες <./Usage/Timezone-traveling.md>
   Πρόσβαση σε αρχεία καταγραφής <./Usage/Accessing-logfiles.md>
   Accu-Chek Combo συμβουλές για την βασική χρήση <./Usage/Accu-Chek-Combo-Tips-for-Basic-usage.md> 
   Εισαγωγή/Εξαγωγή Ρυθμίσεων <./Usage/ExportImportSettings.rst>
   

AndroidAPS για τα παιδιά
------------------
.. toctree::
   :maxdepth: 1
   :glob:
   
   * "Εξ αποστάσεως παρακολούθηση <./Children/Children.rst>
   SMS commands <./Children/SMS-commands2019.rst>
   

Για προχωρημένους 
----------
.. toctree::
   :maxdepth: 1
   :glob:
   
   Android auto <./Usage/Android-auto.md>
   Automation with 3rd party apps <./Usage/automationwithapp.md>
   

Αντιμετώπιση προβλημάτων
------------------------------------------
.. toctree::
   :maxdepth: 1
   :glob:
  
   NS-Client <./Usage/Troubleshooting-NSClient.md>
   Αναβάθμιση <./Installing-AndroidAPS/Update-to-new-version.html#troubleshooting>
   Αντλίες <./FGT/Troubleshootingpumps.rst>


Συχνές ερωτήσεις 
------------------------------------------
.. toctree::
   :maxdepth: 1
   :glob:
  
   Συχνές ΕΡΩΤΉΣΕΙΣ <./Getting-Started/FAQ.md>

   
Γλωσσάριο
------------------------------------------
.. toctree::
   :maxdepth: 1
   :glob:
  
   Γλωσσάρι <./Getting-Started/Glossary.md>
  

Πού να πάτε για βοήθεια 
------------
.. toctree::
   :maxdepth: 1
   :glob:

   Χρήσιμους πόρους για να διαβάσετε πριν ξεκινήσετε <./Where-To-Go-For-Help/Background-reading.md>
   Πού να πάτε για βοήθεια <./Where-To-Go-For-Help/Connect-with-other-users.md>
   Wiki ενημερώσεις και αλλαγές <./Getting-Started/WikiUpdate.rst>

Για Τους Κλινικούς Ιατρούς
------------
.. toctree::
   :maxdepth: 1
   :glob:
            
   Για Τους Κλινικούς Ιατρούς <./Resources/clinician-guide-to-AndroidAPS>


Πώς να βοηθήσετε
------------
.. toctree::
   :maxdepth: 1
   :glob:

   Πώς να βοηθήσετε <./Getting-Started/How-can-I-help.md>
   Πώς να μεταφράσει το app και το wiki <./μεταφράσεις.md>
   Πώς να επεξεργαστείτε το wiki <./make-a-PR>


.. σημείωση:: 
	** Αποποίηση ευθύνης και προειδοποίηση **

	* Όλες οι πληροφορίες, οι σκέψεις και ο κώδικας που περιγράφονται εδώ προορίζονται μόνο για πληροφοριακούς και εκπαιδευτικούς σκοπούς. Το Nightscout δεν πραγματοποιεί επί του παρόντος προσπάθεια συμμόρφωσης με το HIPAA. Χρησιμοποιήστε το Nightscout και το AndroidAPS με δική σας ευθύνη και μην χρησιμοποιείτε τις πληροφορίες ή τον κωδικό για να παίρνετε ιατρικές αποφάσεις.

	* Η χρήση του κώδικα από το github.com είναι χωρίς εγγύηση ή επίσημη υποστήριξη οποιασδήποτε μορφής. Ανατρέξτε στην ΑΔΕΙΑ ΑΠΟΣΤΟΛΗΣ αυτού του αποθετηρίου για λεπτομέρειες.

	* Όλα τα ονόματα των προϊόντων και των εταιρειών, τα εμπορικά σήματα, τα κατατεθέντα εμπορικά σήματα και τα καταχωρημένα λογότυπα υπηρεσίας αποτελούν ιδιοκτησία των αντίστοιχων κατόχων τους. Η χρήση τους είναι για ενημερωτικούς σκοπούς και δεν συνεπάγεται καμία προσχώρηση ή έγκριση από αυτούς.

	Παρακαλώ σημειώστε - αυτό το έργο δεν έχει καμία σχέση και δεν υποστηρίζεται από: `SOOIL <http://www.sooil.com/eng/>` _, `Dexcom <http://www.dexcom.com/>` _, «Accu-Chek<http://www.accu-chek.com/>, Roche Diabetes Care <2/>» _. ή Medtronic <http://www.medtronic.com/>'_
