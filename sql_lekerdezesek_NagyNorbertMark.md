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

7.1
SELECT id, nev, email FROM tanulok
WHERE email IS NULL 

7.2
INSERT INTO tanulok (id, nev, osztaly, eletkor, varos, atlag, hianyzas, osztondijas)
VALUES (9, "Kovács Emma", "10.A", 16, "Budapest", 4.0, 3, 0)
SELECT * FROM tanulok
WHERE nev = "Kovács Emma"

7.3
SELECT id, nev, email FROM tanulok 
WHERE nev = "Kovács Emma"

7.4
UPDATE tanulok
SET atlag = 4.5, osztondijas = 1
WHERE nev = "Kovács Emma"

7.5
DELETE FROM tanulok
WHERE id = 9
SELECT COUNT(*) FROM tanulok

8.1
SELECT id, nev FROM tanulok ORDER BY id LIMIT 3

8.2
SELECT nev, atlag FROM tanulok ORDER BY atlag DESC LIMIT 3

8.3
SELECT nev, hianyzas FROM tanulok ORDER BY hianyzas LIMIT 2

8.4
SELECT nev, atlag FROM tanulok
WHERE varos = "Budapest"
ORDER BY atlag DESC LIMIT 3

8.5
SELECT nev, osztaly, atlag FROM tanulok 
WHERE osztaly = "11.A" || osztaly = "11.B"
ORDER BY atlag DESC LIMIT 2

9.1
SELECT COUNT(*) FROM tanulok

9.2
SELECT MIN(hianyzas) FROM tanulok

9.3
SELECT MAX(atlag) FROM tanulok

9.4
SELECT COUNT(hianyzas) FROM tanulok

9.5
SELECT AVG(atlag) FROM tanulok
WHERE varos = "Budapest"

10.1
SELECT nev, atlag FROM tanulok
WHERE atlag >= 4
ORDER BY atlag DESC LIMIT 3

10.2
SELECT nev, eletkor, varos, atlag FROM tanulok
WHERE eletkor >= 17 & varos = "Budapest" || varos = "Érd"
ORDER BY atlag LIMIT 3

10.3
SELECT COUNT(nev) FROM tanulok 
WHERE osztondijas = 0 & hianyzas >= 10

10.4
SELECT AVG(atlag) FROM tanulok
WHERE osztaly = "10.A" & hianyzas <= 6 

10.5
SELECT nev, varos, osztaly, atlag, hianyzas FROM tanulok 
WHERE varos = "Budapest" || varos = "Érd" & atlag >= 4 & hianyzas <= 8 & osztaly != "11.B"
ORDER BY atlag DESC LIMIT 2
