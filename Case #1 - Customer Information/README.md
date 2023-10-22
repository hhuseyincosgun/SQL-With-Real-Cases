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

**Q12# Customers tablosunda müşterinin yaşına göre hesaplayarak toplam müşteri sayılarını yazdırınız.**

Solution-1:
````sql
SELECT AGEGROUP, COUNT(*) AS CUSTOMERCOUNT
FROM CUSTOMERS
GROUP BY AGEGROUP
ORDER BY CUSTOMERCOUNT DESC
````

| AGEGROUP  | CUSTOMERCOUNT |
| --------- | ------------- |
| 65 Over   | 266           |
| 20-35 Age | 207           |
| 46-55 Age | 163           |
| 56-65 Age | 161           |
| 36-45 Age | 154           |

Solution-2: 

````sql
SELECT 
CASE
	WHEN DATEDIFF(YEAR, BIRTHDATE, GETDATE()) BETWEEN 20 AND 35 THEN '20-35'
	WHEN DATEDIFF(YEAR, BIRTHDATE, GETDATE()) BETWEEN 36 AND 45 THEN '36-45'
	WHEN DATEDIFF(YEAR, BIRTHDATE, GETDATE()) BETWEEN 46 AND 55 THEN '46-55'
	WHEN DATEDIFF(YEAR, BIRTHDATE, GETDATE()) BETWEEN 56 AND 65 THEN '56-65'
	WHEN DATEDIFF(YEAR, BIRTHDATE, GETDATE()) > 65 THEN '65 Over'
END AGEGROUP,
COUNT(*) CUSTOMERCOUNT
FROM CUSTOMERS
GROUP BY
 CASE
	WHEN DATEDIFF(YEAR, BIRTHDATE, GETDATE()) BETWEEN 20 AND 35 THEN '20-35'
	WHEN DATEDIFF(YEAR, BIRTHDATE, GETDATE()) BETWEEN 36 AND 45 THEN '36-45'
	WHEN DATEDIFF(YEAR, BIRTHDATE, GETDATE()) BETWEEN 46 AND 55 THEN '46-55'
	WHEN DATEDIFF(YEAR, BIRTHDATE, GETDATE()) BETWEEN 56 AND 65 THEN '56-65'
	WHEN DATEDIFF(YEAR, BIRTHDATE, GETDATE()) > 65 THEN '65 Over'
END

ORDER BY AGEGROUP
````
Solution-3:
````sql
SELECT AGEGROUP2, COUNT(TMP.ID) AS CUSTOMERCOUNT FROM
(
SELECT *, 
CASE
	WHEN DATEDIFF(YEAR, BIRTHDATE, GETDATE()) BETWEEN 20 AND 35 THEN '20-35'
	WHEN DATEDIFF(YEAR, BIRTHDATE, GETDATE()) BETWEEN 36 AND 45 THEN '36-45'
	WHEN DATEDIFF(YEAR, BIRTHDATE, GETDATE()) BETWEEN 46 AND 55 THEN '46-55'
	WHEN DATEDIFF(YEAR, BIRTHDATE, GETDATE()) BETWEEN 56 AND 65 THEN '56-65'
	WHEN DATEDIFF(YEAR, BIRTHDATE, GETDATE()) > 65 THEN '65 Over'
END AGEGROUP2
FROM CUSTOMERS
) TMP
GROUP BY AGEGROUP2
ORDER BY AGEGROUP2 
````
**Q13# İstanbul şehrinde yaşayıp Kadıköy dışında olanları listeleyiniz.**

Solution-1:
````sql
SELECT TOP 10 * FROM CUSTOMERS C
WHERE C.DISTRICTID IN (SELECT ID FROM DISTRICTS WHERE DISTRICT NOT IN ('KADIKÖY'))
AND C.CITYID IN (SELECT ID FROM CITIES WHERE CITY IN ('İSTANBUL'))
````
Solution-2:
````sql
SELECT * FROM CUSTOMERS C
INNER JOIN CITIES CT ON CT.ID = C.CITYID
INNER JOIN DISTRICTS D ON D.ID = C.DISTRICTID
WHERE CT.CITY = 'İSTANBUL' AND D.DISTRICT != 'KADIKÖY'
````

| ID  | CUSTOMERNAME          | TCNUMBER    | GENDER | EMAIL                  | BIRTHDATE  | CITYID | DISTRICTID | TELNR1       | TELNR2       | AGEGROUP  |
| --- | --------------------- | ----------- | ------ | ---------------------- | ---------- | ------ | ---------- | ------------ | ------------ | --------- |
| 15  | Yasin AĞAGÜL          | 32764684197 | E      | y_agagvl@miuul.com     | 19.10.1979 | 34     | 897        | (532)6102663 | (537)3381012 | 36-45 Age |
| 88  | Sebahat CİLALITAŞ     | 65960134490 | K      | s_cilalitas@miuul.com  | 30.09.1978 | 34     | 64         | (535)7019065 | (532)2408341 | 36-45 Age |
| 97  | Deniz BENDER          | 31619199155 | E      | d_bender@miuul.com     | 4.04.1986  | 34     | 134        | (542)4181722 | (536)4621320 | 36-45 Age |
| 101 | Çağla BEĞEN           | 85581395736 | K      | c_begen@miuul.com      | 22.12.1991 | 34     | 81         | (535)1338012 | (533)8331511 | 20-35 Age |
| 127 | Nurettin GAYRETLİ     | 2822523822  | E      | n_gayretli@miuul.com   | 27.04.1950 | 34     | 84         | (532)7969080 | (536)7322740 | 65 Over   |
| 139 | Yeliz KÜÇÜKALP        | 65432369284 | K      | y_kvcvkalp@miuul.com   | 26.02.1965 | 34     | 488        | (555)9613650 | (543)1071715 | 56-65 Age |
| 164 | Eylül GÜLÜ            | 56388773535 | K      | e_gvlv@miuul.com       | 24.08.1969 | 34     | 3          | (537)5953916 | (532)4647711 | 46-55 Age |
| 174 | Müzeyyen OCAKÇI       | 89589164667 | K      | m_ocakci@miuul.com     | 19.02.1972 | 34     | 707        | (543)1576124 | (505)9181537 | 46-55 Age |
| 199 | Muhammed Emin TEKKAYA | 87271968026 | E      | m_emin@miuul.com       | 19.04.1984 | 34     | 897        | (542)2911632 | (535)9881318 | 36-45 Age |
| 208 | Neslihan KILIÇÇEKER   | 53734331933 | K      | n_kilicceker@miuul.com | 4.10.1982  | 34     | 707        | (543)1432619 | (505)2287257 | 36-45 Age |
|     |

**Q13# Cities tablosundan "Ankara" kaydını sildiğimizi varsayalım. Bu durumda şehri "Ankara" olan müşterilerin şehir alanı boş gelecektir. Şehir alanı boş olan müşterileri listeleyen sorguyu yazınız.**

````sql
UPDATE CITIES SET CITIES = NULL WHERE ID= 6
````

````sql
 SELECT TOP 10 * FROM CUSTOMERS C
 WHERE C.CITYID  = ( SELECT CT.ID FROM CITIES CT WHERE CT.CITIES IS NULL)
````

````sql
SET IDENTITY_INSERT CITIES ON -- ID değerimixz identity_insert off modundaydı önce onu açmamız lazım.
INSERT INTO CITIES(ID,CITIES)
VALUES(6,'ANKARA')
SET IDENTITY_INSERT CITIES OFF -- ID için idendity_insert değerini kapattık.
````
#### Steps

INSERT INTO tabloya bir veya birden çok kayıt ekler. Bu ekleme sorgusu olarak adlandırılır.

IDENTITY_INSERT veritabanına veri girişi yaparken identity olan kolona veri girebilmemizi sağlar.

#### Cevap:
| ID  | CUSTOMERNAME              | TCNUMBER    | GENDER | EMAIL                | BIRTHDATE  | CITYID | DISTRICTID | TELNR1       | TELNR2       | AGEGROUP    |
| --- | ------------------------- | ----------- | ------ | -------------------- | ---------- | ------ | ---------- | ------------ | ------------ | ----------- |
| 112 | Aslı GÜNE                 | 63618747382 | K      | a_gvne@miuul.com     | 6.05.1994  | 6      | 157        | (505)6442992 | (532)8235020 | 20-35 YAŞ   |
| 135 | Güllü SALUR               | 76464619181 | K      | g_salur@miuul.com    | 24.01.1998 | 6      | 128        | (533)7408614 | (535)5992618 | 20-35 YAŞ   |
| 160 | Rukiye ÜNGÖR              | 1490087423  | K      | r_vngor@miuul.com    | 7.07.1956  | 6      | 756        | (554)1519484 | (538)7692165 | 65 YAŞ ÜSTÜ |
| 180 | Güler BEŞKAYA             | 87951772201 | K      | g_beskaya@miuul.com  | 21.07.1998 | 6      | 756        | (553)8215027 | (555)8771930 | 20-35 YAŞ   |
| 188 | Sefa CANGAR               | 17673520419 | E      | s_cangar@miuul.com   | 31.07.1958 | 6      | 361        | (554)1434188 | (533)3133445 | 55-65 YAŞ   |
| 209 | İzzet CANKURU             | 76469454575 | E      | i_cankuru@miuul.com  | 11.12.1978 | 6      | 257        | (555)3724345 | (541)4935289 | 36-45 YAŞ   |
| 225 | Seval ÖZKANLI             | 52599001986 | K      | s_ozkanli@miuul.com  | 2.07.1995  | 6      | 425        | (534)7052964 | (538)6732660 | 20-35 YAŞ   |
| 227 | Halil İbrahim BİMBİRDİREK | 12831119936 | E      | h_ibrahim@miuul.com  | 19.07.1971 | 6      | 756        | (544)4642995 | (537)9514174 | 46-55 YAŞ   |
| 233 | Ecrin MÜRSEL              | 1693687461  | K      | e_mvrsel@miuul.com   | 17.01.1956 | 6      | 425        | (535)3784675 | (533)9489743 | 65 YAŞ ÜSTÜ |
| 358 | Cihan SAYGINER            | 14412309644 | E      | c_sayginer@miuul.com | 26.03.1943 | 6      | 30         | (533)8984184 | (537)3434486 | 65 YAŞ ÜSTÜ |
|     |

***

**15. Müşterilerimizin telefon numaralarının operatör bilgisini getirmek istiyoruz.(TELN1 ve TELNR2 alanlarının yanına operatör numarasını (532)(505) getirmek istiyoruz.) Bu sorgu için gereken SQL sorgusunu yazınız.**

Çözüm -

````sql
 SELECT TOP 10 *,
 SUBSTRING(TELNR1,2,3) AS OPERATOR1,
 SUBSTRING(TELNR2,2,3) AS OPERATOR2
 FROM CUSTOMERS
````

#### Basamaklar:
- String verilerde istenilen karakter kadar verinin geri döndürülmesini sağlamak için SUBSTRING fonksiyonu kullanılır

- The LEFT() fonksiyonu bir dizeden (soldan başlayarak) bir dizi karakter çıkarır.


#### Cevap:
| ID | CUSTOMERNAME          | TCNUMBER    | GENDER | EMAIL                  | BIRTHDATE  | CITYID | DISTRICTID | TELNR1       | TELNR2       | AGEGROUP    | OPERATOR1 | OPERATOR2 |
| -- | --------------------- | ----------- | ------ | ---------------------- | ---------- | ------ | ---------- | ------------ | ------------ | ----------- | --------- | --------- |
| 1  | Sevda AKÇAN           | 42074151323 | K      | s_akcan@miuul.com      | 12.05.1964 | 22     | 202        | (542)5255514 | (532)3438190 | 55-65 YAŞ   | 542       | 532       |
| 2  | Sebahat ŞERALI        | 74789296130 | K      | s_serali@miuul.com     | 11.06.1943 | 78     | 473        | (534)7157144 | (532)2212126 | 65 YAŞ ÜSTÜ | 534       | 532       |
| 3  | Irmak HAMİDİ          | 86856513494 | K      | i_hamidi@miuul.com     | 13.11.1973 | 21     | 675        | (533)2144819 | (555)1183975 | 46-55 YAŞ   | 533       | 555       |
| 4  | Tuğçe AKKOÇ           | 50190579600 | K      | t_akkoc@miuul.com      | 8.06.1958  | 30     | 158        | (543)4243115 | (533)6299636 | 55-65 YAŞ   | 543       | 533       |
| 5  | Necdet ERÇAM          | 26046030220 | E      | n_ercam@miuul.com      | 22.05.1986 | 60     | 718        | (532)6896237 | (534)2924742 | 36-45 YAŞ   | 532       | 534       |
| 6  | Ahmet İNCİKAPI        | 6722155596  | E      | a_incikapi@miuul.com   | 28.05.1991 | 53     | 225        | (532)2414618 | (538)8459085 | 20-35 YAŞ   | 532       | 538       |
| 7  | Arif TEMELOĞLU        | 43691911318 | E      | a_temeloglu@miuul.com  | 11.12.1967 | 40     | 638        | (554)5504524 | (534)6379277 | 55-65 YAŞ   | 554       | 534       |
| 8  | Elif ÖZÇELİKBAŞ       | 84870496920 | K      | e_ozcelikbas@miuul.com | 6.06.1993  | 73     | 815        | (536)9014627 | (544)3937372 | 20-35 YAŞ   | 536       | 544       |
| 9  | Ali Eymen DEVE        | 80011834707 | E      | a_eymen@miuul.com      | 23.01.1985 | 39     | 463        | (533)8082176 | (538)4811026 | 36-45 YAŞ   | 533       | 538       |
| 10 | Muhammed Ali ABDULLAH | 64660973116 | E      | m_ali@miuul.com        | 7.05.1987  | 25     | 851        | (536)4359524 | (532)3864478 | 36-45 YAŞ   | 536       | 532       |
|    |


***

**16.Müşterilerimizin telefon numaralarının operatör bilgisini getirmek istiyoruz. Örneğin telefon numaraları "50"ya da "55"ile başlayan X, "54" ile başlayan Y, "53" ile başlayan Z operatörü olsun. Burada hangi operatörden ne kadar müşterimiz olduğunu bilgisini getirecek sorguyu yazınız.**

Çözüm -

```sql
SELECT SUM(TELNR1_X + TELNR2_X) AS OPERATOR_X,
SUM(TELNR1_Y + TELNR2_Y) AS OPERATOR_Y,
SUM(TELNR1_Z + TELNR2_Z) AS OPERATOR_Z FROM
(SELECT *,
 CASE
	WHEN TELNR1 LIKE '(50%' OR TELNR1 LIKE '(55%' THEN 1
	ELSE 0
END AS TELNR1_X,
 CASE
	WHEN TELNR1 LIKE '(54%' THEN 1
	ELSE 0
END AS TELNR1_Y,
 CASE
	WHEN TELNR1 LIKE '(53%' THEN 1
	ELSE 0
END AS TELNR1_Z,
 CASE
	WHEN TELNR2 LIKE '(50%' OR TELNR2 LIKE '(55%' THEN 1
	ELSE 0
END AS TELNR2_X,
 CASE
	WHEN TELNR2 LIKE '(54%' THEN 1
	ELSE 0
END AS TELNR2_Y,
CASE
	WHEN TELNR2 LIKE '(53%' THEN 1
	ELSE 0
END AS TELNR2_Z
FROM CUSTOMERS) TT
```

#### Cevap:
| OPERATOR_X | OPERATOR_Y | OPERATOR_Z |
| ---------- | ---------- | ---------- |
| 461        | 478        | 963        |
|            |

***

**17.Her ilde en çok müşteriye sahip olduğumuz ilçeleri müşteri sayısına göre çoktan za doğru sıralı şekilde getiren sorguyu yazınız.**

Çözüm -

````sql
SELECT TOP 20 CT.CITIES,D.DISTRICT, COUNT(C.ID) AS CUSTOMERCOUNT FROM CUSTOMERS C
INNER JOIN CITIES CT ON  CT.ID = C.CITYID 
INNER JOIN DISTRICTS D ON D.ID = C.DISTRICTID 
GROUP BY CT.CITIES,D.DISTRICT
ORDER BY 1,3 DESC
````
 

#### Cevap:
| CITIES         | DISTRICT              | CUSTOMERCOUNT |
| -------------- | --------------------- | ------------- |
| ADANA          | SEYHAN                | 8             |
| ADANA          | ALADAĞ                | 6             |
| ADANA          | YÜREĞİR               | 2             |
| ADIYAMAN       | ADIYAMAN MERKEZ       | 5             |
| ADIYAMAN       | BESNİ                 | 2             |
| ADIYAMAN       | SAMSAT                | 2             |
| ADIYAMAN       | GÖLBAŞI/ADIYAMAN      | 1             |
| ADIYAMAN       | KAHTA                 | 1             |
| AFYONKARAHİSAR | AFYONKARAHİSAR MERKEZ | 5             |
| AFYONKARAHİSAR | BOLVADİN              | 4             |
| AFYONKARAHİSAR | DİNAR                 | 4             |
| AFYONKARAHİSAR | DAZKIRI               | 2             |
| AFYONKARAHİSAR | EMİRDAĞ               | 1             |
| AFYONKARAHİSAR | İHSANİYE              | 1             |
| AFYONKARAHİSAR | SİNANPAŞA             | 1             |
| AFYONKARAHİSAR | SULTANDAĞI            | 1             |
| AĞRI           | TUTAK                 | 4             |
| AĞRI           | ELEŞKİRT              | 3             |
| AĞRI           | AĞRI MERKEZ           | 2             |
| AĞRI           | DİYADİN               | 2             |
|                |


***

**18. Müşterilerin doğum günlerini türkçe haftanın günleri olarak getiren sorguyu yazınız.**

Çözüm -

```sql
SET LANGUAGE Turkish
SELECT TOP 10 CUSTOMERNAME,
DATENAME(DW,BIRTHDATE) AS BIRTHDAY
FROM CUSTOMERS
```

#### Basamaklar:
- DATENAME() başa yazılan parametrenin adını döner


#### Cevap:
| CUSTOMERNAME          | BIRTHDAY  |
| --------------------- | --------- |
| Sevda AKÇAN           | Salı      |
| Sebahat ŞERALI        | Cuma      |
| Irmak HAMİDİ          | Salı      |
| Tuğçe AKKOÇ           | Pazar     |
| Necdet ERÇAM          | Perşembe  |
| Ahmet İNCİKAPI        | Salı      |
| Arif TEMELOĞLU        | Pazartesi |
| Elif ÖZÇELİKBAŞ       | Pazar     |
| Ali Eymen DEVE        | Çarşamba  |
| Muhammed Ali ABDULLAH | Perşembe  |
|                       |


***


**19. Müşterilerin doğum günlerinin bu yıl hangi güne denk geldiğini gösteren sorguyu yazınız.**

Cevap -

```sql

SELECT TOP 10 *,
	CASE
		WHEN KMKK.KACGUNGECTI%7 = 0 THEN DATENAME(weekday, GETDATE())
		WHEN KMKK.KACGUNGECTI%7 = 1 THEN DATENAME(weekday, DATEADD(day, -6, GETDATE()))
		WHEN KMKK.KACGUNGECTI%7 = 2 THEN DATENAME(weekday, DATEADD(day, -5, GETDATE()))
		WHEN KMKK.KACGUNGECTI%7 = 3 THEN DATENAME(weekday, DATEADD(day, -4, GETDATE()))
		WHEN KMKK.KACGUNGECTI%7 = 4 THEN DATENAME(weekday, DATEADD(day, -3, GETDATE()))
		WHEN KMKK.KACGUNGECTI%7 = 5 THEN DATENAME(weekday, DATEADD(day, -2, GETDATE()))
		WHEN KMKK.KACGUNGECTI%7 = 6 THEN DATENAME(weekday, DATEADD(day, -1, GETDATE()))
	END AS HANGIGUN
FROM
(SELECT KMK.CUSTOMERNAME, DATEDIFF(DAY,KMK.BIRTHDATE,KMK.TODAYSDATE) AS KACGUNGECTI
FROM 
(SELECT *, GETDATE() AS TODAYSDATE FROM CUSTOMERS) KMK)KMKK
```

#### Basamaklar:
- DATEADD() Belirtilen bir zaman aralığını tarihe eklemek veya tarihten çıkarmak için DateAdd işlevini kullanabilirsiniz.

#### Cevap:
| CUSTOMERNAME          | KACGUNGECTI | HANGIGUN  |
| --------------------- | ----------- | --------- |
| Sevda AKÇAN           | 21709       | Cumartesi |
| Sebahat ŞERALI        | 29350       | Çarşamba  |
| Irmak HAMİDİ          | 18237       | Cumartesi |
| Tuğçe AKKOÇ           | 23874       | Pazartesi |
| Necdet ERÇAM          | 13664       | Perşembe  |
| Ahmet İNCİKAPI        | 11832       | Cumartesi |
| Arif TEMELOĞLU        | 20401       | Pazar     |
| Elif ÖZÇELİKBAŞ       | 11092       | Pazartesi |
| Ali Eymen DEVE        | 14148       | Cuma      |
| Muhammed Ali ABDULLAH | 13314       | Perşembe  |
|                       |

***

**20.Doğum günü bugün olan müşterileri listeleyiniz.**

Çözüm-1

```sql
SELECT * FROM CUSTOMERS
WHERE DATEPART(DAY,BIRTHDATE)=DATEPART(DAY,GETDATE()) AND DATEPART(MONTH,BIRTHDATE)=DATEPART(MONTH,GETDATE()) 
```

Çözüm-2

```sql
SELECT CUSTOMERNAME, BIRTHDATE ,DATEPART(DAYOFYEAR, BIRTHDATE) AS 'BIRTH DAY'
FROM CUSTOMERS
WHERE DATEPART(DAYOFYEAR, GETDATE()) = DATEPART(DAYOFYEAR, BIRTHDATE);
```
#### Basamaklar:
- DATEPART: Verilen tarih-saat parametresini parçalarına ayırıp istenilen parçayı almaya yarar

#### Cevap:
| ID  | CUSTOMERNAME      | TCNUMBER    | GENDER | EMAIL                | BIRTHDATE  | CITYID | DISTRICTID | TELNR1       | TELNR2       | AGEGROUP    |
| --- | ----------------- | ----------- | ------ | -------------------- | ---------- | ------ | ---------- | ------------ | ------------ | ----------- |
| 15  | Yasin AĞAGÜL      | 32764684197 | E      | y_agagvl@miuul.com   | 19.10.1979 | 34     | 897        | (532)6102663 | (537)3381012 | 36-45 YAŞ   |
| 84  | Muhammed Ali ORUC | 1192159330  | E      | m_ali@miuul.com      | 19.10.1996 | 1      | 
