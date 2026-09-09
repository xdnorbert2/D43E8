4.1
SELECT * FROM tanulok

4.2
SELECT nev FROM tanulok

4.3
SELECT nev, osztaly FROM tanulok

4.4
SELECT nev, atlag, hianyzas FROM tanulok

4.5
SELECT id, nev, varos, email FROM tanulok


5.1
SELECT nev FROM tanulok
WHERE	osztaly = "10.A"

5.2
SELECT * FROM tanulok
WHERE	atlag >= 4

5.3
SELECT DISTINCT varos FROM tanulok

5.4
SELECT nev, atlag FROM tanulok
ORDER BY atlag DESC;

5.5
SELECT nev, atlag FROM tanulok
WHERE varos = "Budapest"
ORDER BY atlag DESC;

6.1
SELECT nev, eletkor, atlag FROM tanulok
WHERE eletkor >= 17 && atlag >= 4
ORDER BY atlag DESC;

6.2
SELECT nev, varos FROM tanulok
WHERE varos = "Budapest" || varos = "Érd"

6.3
SELECT nev, osztaly FROM tanulok
WHERE	osztaly != "10.A"

6.4
SELECT nev, osztaly, atlag FROM tanulok
WHERE	osztaly = "10.A" || osztaly = "10.B" && atlag >= 3.5
ORDER BY atlag DESC;

6.5
SELECT nev, varos, osztaly, atlag FROM tanulok
WHERE varos = "Budapest" || varos = "Érd" && atlag >= 4 && osztaly != "11.B"
ORDER BY atlag DESC;