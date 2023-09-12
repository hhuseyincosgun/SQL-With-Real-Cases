# 📁 Case #1 - Customer Information
![Cover](https://github.com/hhuseyincosgun/Learning-SQL-With-Real-Cases/assets/21257660/8ff07d2b-380d-417c-9c3f-ddae00f38719)


## 📋 Table of Contents
- [About](#about)
- [Relational Database Diagram](#relational-database-diagram)
- [Queries and Solutions](#queries-and-solutions)

Please note that all the information regarding the case study has been sourced from the following link: [here](https://www.udemy.com/course/alistirmalarla-sql-ogreniyorum/). 

If you have any questions, reach out to me on:
[LinkedIn](https://www.linkedin.com/in/hasanhuseyincosgun/),
[Medium](https://medium.com/@hhuseyincosgun),
[Kaggle](https://www.kaggle.com/huseyincosgun).
***

## About
We will make SQL queries with a data set containing customer information. There is a lot of different information in the data set, which includes different types of data.

***

## Relational Database Diagram

![db](https://github.com/hhuseyincosgun/Learning-SQL-With-Real-Cases/assets/21257660/b600377b-4af9-4f24-ae0c-8b0efebce307)
***

## Queries and Solutions


**Q1# List all the information of 10 customers whose names start with the letter 'A'.**

Query results are limited to 10.
````sql
SELECT TOP 10 * FROM CUSTOMERS
WHERE CUSTOMERNAME LIKE 'A%'
````
#### Answer:
| ID  | CUSTOMERNAME         | TCNUMBER    | GENDER | EMAIL                 | BIRTHDATE  | CITYID | DISTRICTID | TELNR1       | TELNR2       |
| --- | -------------------- | ----------- | ------ | --------------------- | ---------- | ------ | ---------- | ------------ | ------------ |
| 6   | Ahmet İNCİKAPI       | 6722155596  | E      | a_incikapi@miuul.com  | 28.05.1991 | 53     | 225        | (532)2414618 | (538)8459085 |
| 7   | Arif TEMELOĞLU       | 43691911318 | E      | a_temeloglu@miuul.com | 11.12.1967 | 40     | 638        | (554)5504524 | (534)6379277 |
| 9   | Ali Eymen DEVE       | 80011834707 | E      | a_eymen@miuul.com     | 23.01.1985 | 39     | 463        | (533)8082176 | (538)4811026 |
| 35  | Ayhan ÖZÇİL          | 3328037338  | E      | a_ozcil@miuul.com     | 8.11.1963  | 10     | 114        | (543)2007274 | (534)1062665 |
| 36  | Azad ÖNÜR            | 65514513990 | E      | a_onvr@miuul.com      | 23.03.1989 | 55     | 722        | (532)7551426 | (542)2487070 |
| 45  | Azra TÜTNCÜ          | 26491895261 | K      | a_tvtncv@miuul.com    | 1.01.1977  | 73     | 815        | (534)6093597 | (537)4311757 |
| 49  | Ada VAPUR            | 11963169229 | K      | a_vapur@miuul.com     | 18.01.1949 | 37     | 569        | (532)6239599 | (532)9787325 |
| 54  | Aslıhan DOLAY        | 79576777794 | K      | a_dolay@miuul.com     | 8.01.1957  | 19     | 734        | (554)8938397 | (544)5597413 |
| 55  | Abdurrahman ALTINGÖZ | 55960130916 | E      | a_altingoz@miuul.com  | 7.08.1999  | 37     | 720        | (544)6667247 | (538)2796190 |
| 100 | Adil KINALI          | 62403300353 | E      | a_kinali@miuul.com    | 29.04.1995 | 21     | 675        | (542)5082498 | (533)8398360 |
|     |
***
**Q2# The list of 10 male customers whose names start with A.**

Query results are limited to 10.
````sql
SELECT TOP 10 * FROM CUSTOMERS
WHERE CUSTOMERNAME LIKE 'A%'
AND GENDER='E'
````
#### Answer:
| ID  | CUSTOMERNAME         | TCNUMBER    | GENDER | EMAIL                 | BIRTHDATE  | CITYID | DISTRICTID | TELNR1       | TELNR2       |
| --- | -------------------- | ----------- | ------ | --------------------- | ---------- | ------ | ---------- | ------------ | ------------ |
| 6   | Ahmet İNCİKAPI       | 6722155596  | E      | a_incikapi@miuul.com  | 28.05.1991 | 53     | 225        | (532)2414618 | (538)8459085 |
| 7   | Arif TEMELOĞLU       | 43691911318 | E      | a_temeloglu@miuul.com | 11.12.1967 | 40     | 638        | (554)5504524 | (534)6379277 |
| 9   | Ali Eymen DEVE       | 80011834707 | E      | a_eymen@miuul.com     | 23.01.1985 | 39     | 463        | (533)8082176 | (538)4811026 |
| 35  | Ayhan ÖZÇİL          | 3328037338  | E      | a_ozcil@miuul.com     | 8.11.1963  | 10     | 114        | (543)2007274 | (534)1062665 |
| 36  | Azad ÖNÜR            | 65514513990 | E      | a_onvr@miuul.com      | 23.03.1989 | 55     | 722        | (532)7551426 | (542)2487070 |
| 55  | Abdurrahman ALTINGÖZ | 55960130916 | E      | a_altingoz@miuul.com  | 7.08.1999  | 37     | 720        | (544)6667247 | (538)2796190 |
| 100 | Adil KINALI          | 62403300353 | E      | a_kinali@miuul.com    | 29.04.1995 | 21     | 675        | (542)5082498 | (533)8398360 |
| 145 | Ayhan KARAMARLI      | 51329958677 | E      | a_karamarli@miuul.com | 2.12.1957  | 39     | 598        | (544)6372815 | (532)5308665 |
| 190 | Azad ERGÜNEŞ         | 60171995213 | E      | a_ergvnes@miuul.com   | 19.07.1990 | 14     | 408        | (538)3718436 | (537)4538516 |
| 224 | Azad KAYAR           | 12138400338 | E      | a_kayar@miuul.com     | 22.03.1981 | 37     | 174        | (553)8521332 | (555)7492984 |
|     |
***
**Q3# 5 Customers born between 1990 and 1995. (These years are included).**

Query results are limited to 5.

Solution-1:
````sql
SELECT TOP 5 * FROM CUSTOMERS
WHERE BIRTHDATE >= '1990-01-01'
AND BIRTHDATE <= '1995-12-31'
````

Solution-2:
````sql
SELECT TOP 5 * FROM CUSTOMERS
WHERE BIRTHDATE BETWEEN '1990-01-01' AND '1995-12-31'
````

Solution-3:
````sql
SELECT TOP 5 * FROM CUSTOMERS
WHERE YEAR(BIRTHDATE) BETWEEN 1990 AND 1995
````
#### Answer:
| ID | CUSTOMERNAME     | TCNUMBER    | GENDER | EMAIL                  | BIRTHDATE  | CITYID | DISTRICTID | TELNR1       | TELNR2       |
| -- | ---------------- | ----------- | ------ | ---------------------- | ---------- | ------ | ---------- | ------------ | ------------ |
| 6  | Ahmet İNCİKAPI   | 6722155596  | E      | a_incikapi@miuul.com   | 28.05.1991 | 53     | 225        | (532)2414618 | (538)8459085 |
| 8  | Elif ÖZÇELİKBAŞ  | 84870496920 | K      | e_ozcelikbas@miuul.com | 6.06.1993  | 73     | 815        | (536)9014627 | (544)3937372 |
| 13 | Dilan DOKUYUCU   | 74659763913 | K      | d_dokuyucu@miuul.com   | 21.01.1993 | 25     | 333        | (538)8929868 | (534)4275461 |
| 14 | Selim ÖZBAY      | 77720855989 | E      | s_ozbay@miuul.com      | 2.10.1992  | 73     | 815        | (535)5906635 | (533)4273519 |
| 30 | Bülent KAÇAROĞLU | 21971116249 | E      | b_kacaroglu@miuul.com  | 9.01.1995  | 42     | 311        | (554)6844639 | (541)5324664 |
|    |

**Q4# Listing 5 people living in Istanbul using JOIN.**

````sql
SELECT TOP 5 C.*, CT.CITY FROM CUSTOMERS C
INNER JOIN CITIES CT ON C.CITYID = CT.ID
WHERE CT.CITY = 'İSTANBUL'
````
#### Answer:
| ID  | CUSTOMERNAME      | TCNUMBER    | GENDER | EMAIL                 | BIRTHDATE  | CITYID | DISTRICTID | TELNR1       | TELNR2       | CITY     |
| --- | ----------------- | ----------- | ------ | --------------------- | ---------- | ------ | ---------- | ------------ | ------------ | -------- |
| 15  | Yasin AĞAGÜL      | 32764684197 | E      | y_agagvl@miuul.com    | 19.10.1979 | 34     | 897        | (532)6102663 | (537)3381012 | İSTANBUL |
| 88  | Sebahat CİLALITAŞ | 65960134490 | K      | s_cilalitas@miuul.com | 30.09.1978 | 34     | 64         | (535)7019065 | (532)2408341 | İSTANBUL |
| 97  | Deniz BENDER      | 31619199155 | E      | d_bender@miuul.com    | 4.04.1986  | 34     | 134        | (542)4181722 | (536)4621320 | İSTANBUL |
| 101 | Çağla BEĞEN       | 85581395736 | K      | c_begen@miuul.com     | 22.12.1991 | 34     | 81         | (535)1338012 | (533)8331511 | İSTANBUL |
| 127 | Nurettin GAYRETLİ | 2822523822  | E      | n_gayretli@miuul.com  | 27.04.1950 | 34     | 84         | (532)7969080 | (536)7322740 | İSTANBUL |

*Number of customers from Istanbul(34):*
````sql
SELECT COUNT(CITYID) FROM CUSTOMERS 
WHERE CITYID=34
````
Output:
| 47 |
| -- |

**Q5# Listing 5 people living in Istanbul using SUBQUERY.**
````sql
SELECT 
TOP 5 * FROM CUSTOMERS C
WHERE C.CITYID IN (SELECT ID FROM CITIES WHERE CITY IN ('İSTANBUL'))
````

#### Answer:
| ID  | CUSTOMERNAME      | TCNUMBER    | GENDER | EMAIL                 | BIRTHDATE  | CITYID | DISTRICTID | TELNR1       | TELNR2       |
| --- | ----------------- | ----------- | ------ | --------------------- | ---------- | ------ | ---------- | ------------ | ------------ |
| 15  | Yasin AĞAGÜL      | 32764684197 | E      | y_agagvl@miuul.com    | 19.10.1979 | 34     | 897        | (532)6102663 | (537)3381012 |
| 88  | Sebahat CİLALITAŞ | 65960134490 | K      | s_cilalitas@miuul.com | 30.09.1978 | 34     | 64         | (535)7019065 | (532)2408341 |
| 97  | Deniz BENDER      | 31619199155 | E      | d_bender@miuul.com    | 4.04.1986  | 34     | 134        | (542)4181722 | (536)4621320 |
| 101 | Çağla BEĞEN       | 85581395736 | K      | c_begen@miuul.com     | 22.12.1991 | 34     | 81         | (535)1338012 | (533)8331511 |
| 127 | Nurettin GAYRETLİ | 2822523822  | E      | n_gayretli@miuul.com  | 27.04.1950 | 34     | 84         | (532)7969080 | (536)7322740 |
|     |

**Q6# How many customers are there in which city?.**

````sql
SELECT CT.CITY, COUNT(C.ID) AS CUSTOMERCOUNT FROM CUSTOMERS C
INNER JOIN CITIES CT ON CT.ID=C.CITYID
GROUP BY CT.CITY
````
| CITY           | CUSTOMERCOUNT |
| -------------- | ------------- |
| ADANA          | 16            |
| ADIYAMAN       | 11            |
| AFYONKARAHİSAR | 19            |
| AĞRI           | 13            |
| AKSARAY        | 12            |


Sort by number of customers:
````sql
SELECT TOP 10 *,
(SELECT COUNT(*) FROM CUSTOMERS WHERE CITYID=CT.ID) AS CUSTOMERCOUNT
FROM CITIES CT
ORDER BY 3 DESC
````

| ID | CITY       | CUSTOMERCOUNT |
| -- | ---------- | ------------- |
| 73 | ŞIRNAK     | 110           |
| 34 | İSTANBUL   | 47            |
| 6  | ANKARA     | 29            |
| 27 | GAZİANTEP  | 25            |
| 35 | İZMİR      | 24            |
| 37 | KASTAMONU  | 23            |
| 16 | BURSA      | 22            |
| 19 | ÇORUM      | 22            |
| 10 | BALIKESİR  | 20            |
| 21 | DİYARBAKIR | 20            |

**Q7# Cities with more than 20 customers.**

Solution-1:
````sql
SELECT CT.CITY, COUNT(C.ID) AS CUSTOMERCOUNT FROM CUSTOMERS C 
INNER JOIN CITIES CT ON CT.ID=C.CITYID
GROUP BY CT.CITY
HAVING  COUNT(C.ID) > 20
ORDER BY CUSTOMERCOUNT DESC
````

Solution-2:
````sql
SELECT * ,
(SELECT COUNT(*) FROM CUSTOMERS WHERE CITYID=C.ID)
FROM CITIES C
WHERE 
(SELECT COUNT(*) FROM CUSTOMERS WHERE CITYID=C.ID)> 20 
ORDER BY 3 DESC
````

| CITY      | CUSTOMERCOUNT |
| --------- | ------------- |
| ŞIRNAK    | 110           |
| İSTANBUL  | 47            |
| ANKARA    | 29            |
| GAZİANTEP | 25            |
| İZMİR     | 24            |
| KASTAMONU | 23            |
| BURSA     | 22            |
| ÇORUM     | 22            |
         
**Q8# Find the number of male and female customers for each city.**

````sql
SELECT 
CT.CITY, C.GENDER, COUNT(C.ID) AS CUSTOMERCOUNT
FROM CUSTOMERS C
INNER JOIN CITIES CT ON CT.ID=C.CITYID
GROUP BY CT.CITY, C.GENDER
ORDER BY CT.CITY, C.GENDER
````

| CITY           | GENDER | CUSTOMERCOUNT |
| -------------- | ------ | ------------- |
| ADANA          | E      | 10            |
| ADANA          | K      | 6             |
| ADIYAMAN       | E      | 7             |
| ADIYAMAN       | K      | 4             |
| AFYONKARAHİSAR | E      | 6             |
| AFYONKARAHİSAR | K      | 13            |
| AĞRI           | E      | 7             |
| AĞRI           | K      | 6             |
| AKSARAY        | E      | 7             |
| AKSARAY        | K      | 5             |

**Q9# Show the information on how many male and female customers there are in each city in separate columns.**
````sql
SELECT TOP 10 CITY,
(SELECT COUNT(*) FROM CUSTOMERS WHERE CITYID=C.ID AND GENDER='E') AS MALECOUNT,
(SELECT COUNT(*) FROM CUSTOMERS WHERE CITYID=C.ID AND GENDER='K') AS FEMALECOUNT
FROM CITIES C
````

| CITY           | MALECOUNT | FEMALECOUNT |
| -------------- | --------- | ----------- |
| ADANA          | 10        | 6           |
| ADIYAMAN       | 7         | 4           |
| AFYONKARAHİSAR | 6         | 13          |
| AĞRI           | 7         | 6           |
| AMASYA         | 3         | 2           |
| ANKARA         | 13        | 16          |
| ANTALYA        | 8         | 5           |
| ARTVİN         | 5         | 7           |
| AYDIN          | 7         | 8           |
| BALIKESİR      | 11        | 9           |

**Q10# Add a new field for the age group to the Customers table. Field name AGEGROUP datatype Varchar(50).**

````sql
ALTER TABLE CUSTOMERS ADD AGEGROUP VARCHAR(50)
````
**Q11# Update the AGEGROUP field you added to the Customers table as 20-35, 36-45, 46-55, 55-65 and over 65.**
````sql
SELECT TOP 10 CUSTOMERNAME,AGEGROUP, DATEDIFF(YEAR, BIRTHDATE, GETDATE()) AS AGE

FROM CUSTOMERS
UPDATE CUSTOMERS SET AGEGROUP='20-35 Age'
WHERE DATEDIFF(YEAR, BIRTHDATE, GETDATE()) BETWEEN 20 AND 35

UPDATE CUSTOMERS SET AGEGROUP='36-45 Age'
WHERE DATEDIFF(YEAR, BIRTHDATE, GETDATE()) BETWEEN 36 AND 45

UPDATE CUSTOMERS SET AGEGROUP='46-55 Age'
WHERE DATEDIFF(YEAR, BIRTHDATE, GETDATE()) BETWEEN 46 AND 55

UPDATE CUSTOMERS SET AGEGROUP='56-65 Age'
WHERE DATEDIFF(YEAR, BIRTHDATE, GETDATE()) BETWEEN 56 AND 65

UPDATE CUSTOMERS SET AGEGROUP='65 Over'
WHERE DATEDIFF(YEAR, BIRTHDATE, GETDATE()) > 65
````
| CUSTOMERNAME          | AGEGROUP  | AGE |
| --------------------- | --------- | --- |
| Sevda AKÇAN           | 56-65 Age | 59  |
| Sebahat ŞERALI        | 65 Over   | 80  |
| Irmak HAMİDİ          | 46-55 Age | 50  |
| Tuğçe AKKOÇ           | 56-65 Age | 65  |
| Necdet ERÇAM          | 36-45 Age | 37  |
| Ahmet İNCİKAPI        | 20-35 Age | 32  |
| Arif TEMELOĞLU        | 56-65 Age | 56  |
| Elif ÖZÇELİKBAŞ       | 20-35 Age | 30  |
| Ali Eymen DEVE        | 36-45 Age | 38  |
| Muhammed Ali ABDULLAH | 36-45 Age | 36  |

**Q12# soru-24.**
