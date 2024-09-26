= Aktenkontolokalisierung

* Jedes Aktenkonto liegt auf einem der beiden Aktensysteme
* Das richtige Aktensystem bringt man mit der Lokalisierung des Aktenkontos in Erfahrung (getRecordStatus())
* Ist ein Aktenkonto einmal lokalisiert, MUSS die Information, in welchem Aktensystem das Konto liegt, gecached werden
* Achtung: Das Aktensystem für ein Konto ändert sich sehr selten, aber es kann sich   ändern
**Aktenumzug (Wechsel der Krankenkasse)
**In diesem Fall (Fehler beim Zugriff auf das Aktenkonto) muss getRecordStatus() erneut aufgerufen werden (auf dem zweiten Aktensystem)
* Tipp:
** Wenn ein Versicherter einer bestimmten Krankenkasse bei einem bestimmten Aktensystem liegt, liegen auch die anderen Aktenkonten derselben Krankenkasse bei demselben Aktensystem
** Es reicht also in aller Regel sogar aus, zu cachen, welche "IK-Nummer" (Krankenkasse) ihre Konten auf welchem Aktensystem verwaltet, um ein bestimmtes Aktenkonto zu lokalisieren
* FQDNs:
** RU-DEV
*** IBM: epa-as-1.dev.epa4all.de
*** BITMARCK: epa-as-2.dev.epa4all.de
** RU-REF
*** IBM: epa-as-1.ref.epa4all.de
*** BITMARCK: epa-as-2.ref.epa4all.de
