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