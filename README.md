# SQL-data-cleaning
## SQL-data-cleaning
### SQL-data-cleaning
# Markdown Editor (Swiss Coding Academy)
        
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam orci quam, rutrum sed nunc ac, feugiat blandit tortor. Nulla a ipsum vitae massa porta ullamcorper eget ut libero. Nam venenatis rhoncus dolor at lobortis. Proin dignissim, sem et lobortis tincidunt, eros urna finibus lorem, interdum suscipit dui purus eget nisl. Cras felis erat, auctor eu pellentesque quis, lobortis a ligula. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Vivamus molestie elit sed accumsan cursus. Quisque id ullamcorper tortor. Praesent non hendrerit turpis. Duis ultrices aliquet odio, vel placerat tortor bibendum nec. Vivamus efficitur sapien metus, eget egestas mi porta in.

<img src="https://lms.swisscoding.edu.vn/pluginfile.php/1/core_admin/logo/0x200/1711103404/sca_logo.png" width="200" style="display: block; margin: 50px auto;">

a1 | b2
---|---
1|2

# Get the 10 first rows from the table using SQL console
|full_name|age|martial_status|email|phone|full_address|job_title|membership_date|
|---------|---|--------------|-----|-----|------------|---------|---------------|
|addie lush|40|married|alush0@shutterfly.com|254-389-8708|3226 Eastlawn Pass,Temple,Texas|Assistant Professor|7/31/2013|
|      ROCK CRADICK|46|married|rcradick1@newsvine.com|910-566-2007|4 Harbort Avenue,Fayetteville,North Carolina|Programmer III|5/27/2018|
|Sydel Sharvell|46|divorced|ssharvell2@amazon.co.jp|702-187-8715|4 School Place,Las Vegas,Nevada|Budget/Accounting Analyst I|10/6/2017|
|Constantin de la cruz|35||co3@bloglines.com|402-688-7162|6 Monument Crossing,Omaha,Nebraska|Desktop Support Technician|10/20/2015|
|  Gaylor Redhole|38|married|gredhole4@japanpost.jp|917-394-6001|88 Cherokee Pass,New York City,New York|Legal Assistant|5/29/2019|
|Wanda del mar       |44|single|wkunzel5@slideshare.net|937-467-6942|10864 Buhler Plaza,Hamilton,Ohio|Human Resources Assistant IV|3/24/2015|
|Joann Kenealy|41|married|jkenealy6@bloomberg.com|513-726-9885|733 Hagan Parkway,Cincinnati,Ohio|Accountant IV|4/17/2013|
|   Joete Cudiff|51|divorced|jcudiff7@ycombinator.com|616-617-0965|975 Dwight Plaza,Grand Rapids,Michigan|Research Nurse|11/16/2014|
|mendie alexandrescu|46|single|malexandrescu8@state.gov|504-918-4753|34 Delladonna Terrace,New Orleans,Louisiana|Systems Administrator III|3/12/1921|
| fey kloss|52|married|fkloss9@godaddy.com|808-177-0318|8976 Jackson Park,Honolulu,Hawaii|Chemical Engineer|11/5/2014|

# Make a copy of your table
```
CREATE TABLE club_member_info_cleaned (
	full_name VARCHAR(50),
	age INTEGER,
	martial_status VARCHAR(50),
	email VARCHAR(50),
	phone VARCHAR(50),
	full_address VARCHAR(50),
	job_title VARCHAR(50),
	membership_date VARCHAR(50)
);
```
# Copy all values from original table
```
INSERT INTO club_member_info_cleaned
SELECT * FROM club_member_info ;
```
# Leading and trailing whitespaces
## TRIM TEXT
```
UPDATE club_member_info_cleaned 
SET full_name =TRIM(full_name);
```
## UPPER TEXT
```
UPDATE club_member_info_cleaned 
SET full_name =TRIM(full_name);
```
### FILTER Age out of realistic range and fix by setting value = 0
```
SELECT  age 
FROM club_member_info_cleaned cmic 
WHERE age >=120
```
```
UPDATE club_member_info_cleaned 
SET age = 0
WHERE age >=150
```
