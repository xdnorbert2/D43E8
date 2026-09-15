4.1
SELECT cim, mufaj, ertekeles FROM filmek

4.2
SELECT id, cim, megjelenes_eve, hossz_perc FROM filmek

4.3
SELECT cim, korhatar, jegyar FROM filmek

4.4
SELECT cim, rendezo FROM filmek

4.5
SELECT * FROM filmek

5.1
SELECT cim, megjelenes_eve FROM filmek 
WHERE megjelenes_eve >= 2015
ORDER BY megjelenes_eve DESC	

5.2
SELECT cim, hossz_perc FROM filmek 
WHERE hossz_perc <= 120 
ORDER BY hossz_perc ASC

5.3
SELECT DISTINCT mufaj FROM filmek 

5.4
SELECT cim, jegyar FROM filmek
ORDER BY jegyar ASC	

5.5
SELECT cim, mufaj, ertekeles FROM filmek
WHERE ertekeles >= 7.5 && ertekeles <= 8.5
ORDER BY ertekeles DESC

6.1
SELECT cim, mufaj, ertekeles FROM filmek 
WHERE (mufaj = "Dráma" || mufaj = "Sci-fi") && ertekeles >= 7.5

6.2
SELECT cim, korhatar FROM filmek 
WHERE korhatar != 16
ORDER BY korhatar ASC	

6.3
SELECT cim, megjelenes_eve FROM filmek 
WHERE megjelenes_eve >= 2010 && megjelenes_eve <= 2020

6.4
SELECT cim, mufaj FROM filmek
WHERE cim LIKE "%a%"

6.5
SELECT cim, korhatar, jegyar, ertekeles FROM filmek
WHERE jegyar <= 2500 && magyar_szinkron = 1 && korhatar <= 12
ORDER BY ertekeles DESC

7.1
SELECT id, cim, rendezo FROM filmek 
WHERE rendezo IS NULL;

7.2
INSERT INTO filmek
(id, cim, mufaj, megjelenes_eve, hossz_perc, korhatar, ertekeles, jegyar, magyar_szinkron)
VALUES (13, 'Mars-expedíció', 'Sci-fi', 2026, 138, 12, 7.6, 3100, 0)

SELECT * FROM filmek
WHERE id = 13

7.3

UPDATE filmek
SET rendezo = "Nagy Viktor"
WHERE cim = "Mars-expedíció"

SELECT cim, rendezo FROM filmek
WHERE id = 13

7.4
UPDATE filmek
SET ertekeles = 8.1, magyar_szinkron = 1
WHERE cim = "Mars-expedíció"

SELECT cim, ertekeles, magyar_szinkron FROM filmek
WHERE id = 13

7.5
DELETE FROM filmek
WHERE id = 13

SELECT COUNT(*) FROM filmek
WHERE cim = "Mars-expedíció"

8.1
SELECT cim, megjelenes_eve FROM filmek
ORDER BY megjelenes_eve DESC LIMIT 4

8.2
SELECT cim, jegyar FROM filmek
ORDER BY jegyar DESC LIMIT 3

8.3
SELECT cim, hossz_perc, korhatar FROM filmek
WHERE korhatar <= 12
ORDER BY hossz_perc ASC LIMIT 2

8.4
SELECT cim, ertekeles FROM filmek
WHERE magyar_szinkron = 1
ORDER BY ertekeles DESC LIMIT 3

8.5
SELECT cim, mufaj, jegyar FROM filmek
WHERE mufaj IN ("Sci-fi", "Dráma", "Krimi")
ORDER BY jegyar ASC LIMIT 4

9.1
SELECT COUNT(*) AS filmek_szama
FROM filmek
WHERE magyar_szinkron = 1;

9.2
SELECT AVG(hossz_perc) AS atlagos_hossz
FROM filmek;

9.3
SELECT MAX(jegyar) AS legdragabb_jegyar
FROM filmek;

9.4
SELECT AVG(ertekeles) AS atlagos_ertekeles
FROM filmek
WHERE mufaj = 'Sci-fi';

9.5
SELECT SUM(jegyar) AS osszes_jegyar
FROM filmek
WHERE korhatar = 12;

10.1
SELECT cim, hossz_perc, ertekeles
FROM filmek
WHERE hossz_perc <= 130 AND ertekeles >= 7.0
ORDER BY ertekeles DESC
LIMIT 3;

10.2
SELECT cim, korhatar, ertekeles, jegyar
FROM filmek
WHERE korhatar <= 12 AND magyar_szinkron = 1 AND jegyar <= 2500
ORDER BY ertekeles DESC, jegyar ASC;

10.3
SELECT COUNT(*) AS filmek_szama
FROM filmek
WHERE megjelenes_eve > 2014 AND hossz_perc >= 120 AND ertekeles >= 7.5;

10.4
SELECT AVG(jegyar) AS atlagos_jegyar
FROM filmek
WHERE mufaj IN ('Sci-fi', 'Dráma', 'Krimi') AND ertekeles >= 7.5;

10.5
SELECT cim, mufaj, megjelenes_eve, hossz_perc, ertekeles, jegyar
FROM filmek
WHERE ertekeles >= 7.8 
  AND megjelenes_eve > 2010 
  AND hossz_perc <= 160 
  AND korhatar <> 16 
  AND magyar_szinkron = 1
ORDER BY ertekeles DESC, jegyar ASC
LIMIT 2;