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
