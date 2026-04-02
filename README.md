
# MEESKOND: Tooteanalüüsi osakond |  NÄDAL: 1  |  TEGELANE: Toomas Kask

## ANDMEMAASTIK (Data Landscape):

## ALAÜLESANDE KAART D: Kaupluste andmed


Mina uurisin sales tabelit, kuna algselt planeeritud stores tabel andmebaasis puudus. 
Leidsid, et kuigi eraldi kaupluste tabelit ei olnud, sain müügiandmete põhjal tuvastada 3 füüsilist asukohta: Tallinn, Tartu ja Pärnu. Märkasin, et online-müükide puhul on asukoha veerg tühi (NULL), mis on oluline eristus.
See tähendab UrbanStyle’ile, et meil on küll olemas info müügikohtade kohta, kuid poodide täpsemaks analüüsiks (nt töötajate arv või pindala) on meil vaja luua eraldi keskne kaupluste register.

    - Sain vastuse küsimusele millised kauplused on ja mis andmed nende kohta on?
    - 

# Mis oli suurim üllatus? Suurim üllatus oligi see, et puudus stores tabel, mille andmeid analüüsida.
# Milline on meie soovitus Toomasele? Andmete korrastamine: Toomas peab esimesel võimalusel looma stores tabeli, kus on kirjas poodide aadressid, pindalad ja töötajate arv. See võimaldaks Toomasel arvutada müüki ruutmeetri kohta või tulu ühe töötaja kohta, mis on äri laiendamiseks hädavajalik info.
# Milliseid andmeid meil puudus? Meil puudus stores andmetega tabel.


[Supabase Snippet Unique Store Locations.csv](https://github.com/user-attachments/files/26436978/Supabase.Snippet.Unique.Store.Locations.csv)
Kaupluse asukoht | Tehingute_arv |Kogukäive
Pärnu            | 1618          | 438 183.08 €
Tartu            | 2708          | 783 468.61 €
Tallinn          | 5704          | 1 626 303.81 E
