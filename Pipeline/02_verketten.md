!SLIDE bullets
#Pakete bauen
* `suchmaschine_build_files.tar` Beispielprojekt einpflegen
* Job erstellen:
  - Repository klonen
  - tar entpacken
  - `debuild --no-tgz-check` ausführen

~~~SECTION:notes~~~
tar xvf $name.tar

~~~ENDSECTION~~~

!SLIDE bullets
#Jobs verketten
* In Beispielprojekt `Post-Build Action`:
  - 'Build other project'
  - Anderes Projekt eintragen
* `copy-artifacts` Plugin

!SLIDE bullets
#Komplexe Ketten
* `conditional-buildstep` Plugin
* Erlaubt 

