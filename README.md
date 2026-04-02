```sql
-- Leia kõik unikaalsed kaupluste asukohad
SELECT DISTINCT store_location 
FROM sales 
WHERE store_location IS NOT NULL;

-- Mitu tehingut on igas linnas tehtud? 
SELECT store_location, COUNT(*) AS tehingute_arv
FROM sales
WHERE store_location IS NOT NULL
GROUP BY store_location
ORDER BY tehingute_arv DESC;

-- Milline linn on toonud kõige rohkem tulu?
SELECT store_location, SUM(total_price) AS kogukäive
FROM sales
WHERE store_location IS NOT NULL
GROUP BY store_location
ORDER BY kogukäive DESC;

-- Millised kauplused on ja mis andmed nende kohta on?
SELECT 
    store_location, 
    COUNT(*) AS tehingute_arv, 
    SUM(total_price) AS kogukäive
FROM sales
WHERE store_location IS NOT NULL
GROUP BY store_location;

-- Millistes linnades kauplused asuvad?
SELECT DISTINCT store_location 
FROM sales 
WHERE store_location IS NOT NULL;

# [urbanstyle-TOOTE-grupp] -- UrbanStyle.ltd 

## ALAÜLESANDE KAART D: Kaupluste andmed

| Nimi | Roll (Nädal 1) 
| :--- | :--- | :--- |
| Egle Laur | Kaupluste andmete uurija 
## Mina uurisin sales tabelit, kuna algselt planeeritud stores tabel andmebaasis puudus. 
## Leidsid, et kuigi eraldi kaupluste tabelit ei olnud, sain müügiandmete põhjal tuvastada 3 füüsilist asukohta: Tallinn, Tartu ja Pärnu. Märkasin, et online-müükide puhul on asukoha veerg tühi (NULL), mis on oluline eristus.
## See tähendab UrbanStyle’ile, et meil on küll olemas info müügikohtade kohta, kuid poodide täpsemaks analüüsiks (nt töötajate arv või pindala) on meil vaja luua eraldi keskne kaupluste register.

## Mis oli suurim üllatus? Suurim üllatus oligi see, et puudus stores tabel, mille andmeid analüüsida.
## Milline on meie soovitus Toomasele? Andmete korrastamine: Toomas peab esimesel võimalusel looma stores tabeli, kus on kirjas poodide aadressid, pindalad ja töötajate arv. See võimaldaks Toomasel arvutada müüki ruutmeetri kohta või tulu ühe töötaja kohta, mis on äri laiendamiseks hädavajalik info.
## Milliseid andmeid meil puudus? Meil puudus stores andmetega tabel.

## Meie eesmärk
Uuendame hiljem.
