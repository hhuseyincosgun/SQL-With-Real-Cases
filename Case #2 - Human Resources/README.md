## Queries and Results


**Q1# Listing of employees who are still working in our company.**

````sql
SELECT NAME_, SURNAME, INDATE, OUTDATE 
FROM PERSON
WHERE OUTDATE IS NULL;
````
#### Result:
| NAME_            | SURNAME          | INDATE     | OUTDATE |
| ---------------- | ---------------- | ---------- | ------- |
| Erdem            | İSTİK            | 28.07.2018 | NULL    |
| Bünyamin         | OKTAYOĞLU        | 29.03.2015 | NULL    |
| Anıl             | HİÇDURMAZ        | 13.06.2018 | NULL    |
| Çiğdem           | GÜLSU            | 13.07.2016 | NULL    |
| Zerda            | KÜTÜKOĞLU        | 28.04.2019 | NULL    |
| Münevver         | MUTAF            | 26.08.2016 | NULL    |
| Nazar            | KAYNAKÇI         | 21.04.2016 | NULL    |
| Naime            | SULTANOĞLU       | 13.04.2017 | NULL    |
| Fevzi            | DURAKLI          | 3.03.2016  | NULL    |
| Canan            | İZYURDU          | 26.08.2019 | NULL    |
| Sultan           | ÇATIKKAŞ         | 5.07.2015  | NULL    |
| Mevlüt           | BAŞDAN           | 21.08.2016 | NULL    |

***

**Q2# Listing the total distribution of the employees currently working in the company by department according to gender.**

````sql
SELECT D.DEPARTMENT,
CASE
    WHEN GENDER = 'E' THEN 'Erkek'
    ELSE 'Kadın'
END AS GENDER,
COUNT(*) PERSONCOUNT
FROM PERSON P
JOIN DEPARTMENT D ON D.ID = P.DEPARTMENTID
WHERE P.OUTDATE IS NULL
GROUP BY D.DEPARTMENT,P.GENDER
ORDER BY D.DEPARTMENT;
````

#### Result:
| DEPARTMENT          | GENDER | PERSONCOUNT |
| ------------------- | ------ | ----------- |
| BİLGİ TEKNOLOJİLERİ | Erkek  | 65          |
| BİLGİ TEKNOLOJİLERİ | Kadın  | 74          |
| FİNANS              | Erkek  | 63          |
| FİNANS              | Kadın  | 72          |
| İLETİŞİM            | Erkek  | 50          |
| İLETİŞİM            | Kadın  | 60          |
| İNSAN KAYNAKLARI    | Erkek  | 66          |
| İNSAN KAYNAKLARI    | Kadın  | 75          |
| MUHASEBE            | Erkek  | 63          |
| MUHASEBE            | Kadın  | 76          |
| PAZARLAMA           | Erkek  | 66          |
| PAZARLAMA           | Kadın  | 73          |

***

**Q3# Showing the result in columns unlike the query above.**

````sql
SELECT *, 
(SELECT COUNT(*) FROM PERSON WHERE DEPARTMENTID = D.ID AND GENDER = 'E' AND OUTDATE IS NULL) AS MALE_PERSONCOUNT,
(SELECT COUNT(*) FROM PERSON WHERE DEPARTMENTID = D.ID AND GENDER = 'K' AND OUTDATE IS NULL) AS FEMALE_PERSONCOUNT,
(SELECT COUNT(*) FROM PERSON WHERE DEPARTMENTID = D.ID AND OUTDATE IS NULL) AS TOTAL_COUNT
FROM DEPARTMENT D
ORDER BY D.DEPARTMENT;
````

#### Result:
| ID | DEPARTMENT          | MALE_PERSONCOUNT | FEMALE_PERSONCOUNT | TOTAL_COUNT |
| -- | ------------------- | ---------------- | ------------------ | ----------- |
| 7  | BİLGİ TEKNOLOJİLERİ | 65               | 74                 | 139         |
| 4  | FİNANS              | 63               | 72                 | 135         |
| 9  | İLETİŞİM            | 50               | 60                 | 110         |
| 6  | İNSAN KAYNAKLARI    | 66               | 75                 | 141         |
| 5  | MUHASEBE            | 63               | 76                 | 139         |
| 3  | PAZARLAMA           | 66               | 73                 | 139         |
| 2  | PLANLAMA            | 66               | 82                 | 148         |
| 8  | SATINALMA           | 67               | 73                 | 140         |
| 10 | SATIŞ               | 58               | 54                 | 112         |
| 1  | YÖNETİM             | 9                | 7                  | 16          |
|    |

***

**Q4# The hiring of a new chief for the planning department is planned. query that returns min, max and average chef salary.
(including employees leaving the company).**



#### Solution - 1:
````sql
SELECT POS.POSITION, 
	MIN(SALARY) MIN_SALARY, 
	MAX(SALARY) MAX_SALARY, 
	ROUND(AVG(SALARY),0) AVG_SALARY
FROM PERSON PER
JOIN POSITION POS ON POS.ID = PER.POSITIONID
WHERE POS.POSITION = 'PLANLAMA ŞEFİ'
GROUP BY POS.POSITION;
````
#### Solution - 2:
````sql
SELECT 
POS.POSITION, 
  (SELECT MIN(SALARY) FROM PERSON WHERE POSITIONID=POS.ID) AS MIN_SALARY,
  (SELECT MAX(SALARY) FROM PERSON WHERE POSITIONID=POS.ID) AS MAX_SALARY,
  (SELECT ROUND(AVG(SALARY),0) FROM PERSON WHERE POSITIONID=POS.ID) AS AVG_SALARY
FROM POSITION POS
WHERE POS.POSITION = 'PLANLAMA ŞEFİ';
````

#### Result:
| POSITION      | MIN_SALARY | MAX_SALARY | AVG_SALARY |
| ------------- | ---------- | ---------- | ---------- |
| PLANLAMA ŞEFİ | 7926       | 10427      | 9240       |

***

**Q5# List the number of employees currently working in each position and their average salaries.**

#### Solution - 1:
````sql
SELECT POS.POSITION, COUNT(*) PERSONCOUNT,
	ROUND(AVG(SALARY),0) AVG_SALARY
FROM PERSON PER
JOIN POSITION POS ON POS.ID = PER.POSITIONID
WHERE OUTDATE IS NULL
GROUP BY POS.POSITION
ORDER BY AVG(SALARY) DESC;
````

#### Solution - 2:
````sql
SELECT 
POS.POSITION, 
(SELECT COUNT(*) FROM PERSON WHERE POSITIONID=POS.ID AND OUTDATE IS NULL) AS PERSONCOUNT,
(SELECT ROUND(AVG(SALARY),0) FROM PERSON WHERE POSITIONID=POS.ID AND OUTDATE IS NULL) AS AVG_SALARY
FROM POSITION POS
ORDER BY AVG_SALARY DESC;
````
| POSITION                        | PERSONCOUNT | AVG_SALARY |
| ------------------------------- | ----------- | ---------- |
| TEKNİK GMY                      | 1           | 19910      |
| GENEL MÜDÜR                     | 1           | 19576      |
| İK'DAN SORUMLU GMY              | 1           | 19048      |
| PLANLAMA MÜDÜRÜ                 | 1           | 17700      |
| İDARİ MALİ İŞLERDEN SORUMLU GMY | 2           | 15754      |
| SATIŞ MÜDÜRÜ                    | 3           | 15515      |
| SATINALMA MÜDÜRÜ                | 4           | 15262      |
| MUHASEBE MÜDÜRÜ                 | 2           | 15027      |
| İNSAN KAYNAKLARI MÜDÜRÜ         | 2           | 14836      |
| BİLGİ TEKNOLOJİLERİ MÜDÜRÜ      | 1           | 14573      |
| PAZARLAMA MÜDÜRÜ                | 3           | 14103      |
| PLANLAMA MÜDÜR YRD.             | 2           | 13860      |


***

