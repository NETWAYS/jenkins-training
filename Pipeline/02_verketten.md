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

~~~SECTION:notes~~~
Schlägt fehl wegen mangelnder files

~~~ENDSECTION~~~

!SLIDE bullets
* Missing access control?
* `Authorize Project` Plugin
  - `Conifgure Jenkins`
  - `Global Security`  
  - `Access Control for Builds`
  - `Run as User who Triggere Build`

~~~SECTION:notes~~~
Reines Sicherheits Feature.
Der user unter dem ein Build läuft wird nun beim start des builds und nicht beim
configurieren festgelegt

Daran denken das Jenkins selber entpsrechende Rechte braucht um etwa den user
zu wechseln

~~~ENDSECTION~~~

!SLIDE bullets
#Jobs verketten
* `Clone Workspace SCM Plug-in`
* `Multiple SCMs plugin`

~~~SECTION:notes~~~
Im 1. job als post built action archivieren, im 2. job als scm holen
~~~ENDSECTION~~~

!SLIDE bullets
#Komplexe Ketten
* `conditional-buildstep` Plugin
* Erlaubt boolsche Kontrollstrukturen

