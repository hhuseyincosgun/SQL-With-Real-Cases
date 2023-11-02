## Queries and Results


**Q1# Listing of employees who are still working in our company.**

Note: those with a blank exit date are those who continue to work

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

**Q2# The list of 10 male customers whose names start with A.**
