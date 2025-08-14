# MySQL_Journey EASY
1.
Show first name, last name, and gender of patients whose gender is 'M'

SELECT
  first_name,
  last_name,
  gender
FROM patients
WHERE gender = 'M';

2.
Show first name and last name of patients who does not have allergies. (null)

select first_name, last_name from patients 
where ALLERGIES IS NULL;

3.
Show first name of patients that start with the letter 'C'

select first_name from patients 
where first_name like 'C%';

4.
Show first name and last name of patients that weight within the range of 100 to 120 (inclusive)

select first_name, last_name from patients 
where weight between 100 and 120;

5.
Update the patients table for the allergies column. If the patient's allergies is null then replace it with 'NKA'

update patients
set allergies = 'NKA'
where allergies is null;

6.
Show first name and last name concatinated into one column to show their full name.

select concat(first_name,' ', last_name) as full_name
from patients

7.
Show first name, last name, and the full province name of each patient.
Example: 'Ontario' instead of 'ON'

8.
Take a look at the invoice_line table that stores information about the purchased tracks. Export all data from the table, filtering the result so that you only get tracks that cost more than $0.99. The values you need are stored in the unit_price column.

SELECT *
FROM invoice_line
WHERE unit_price > .99;

Get these fields from the client table: first_name (the client’s first name), last_name (the client’s last name), and city (the client’s location). Get only client records for customers that live in Brazil. Tip: country of residence is stored in the country field.

select first_name,Last_name,city
from client
where country = 'Brazil';

A. Check when and where the biggest purchases were made: from the invoice table, get the billing_address field and the invoice_date.
B. The date is stored in the 'YYYY-MM-DD HH:MM:SS' format but you need just the date without the time ('YYYY-MM-DD').
C. Filter out the records where the value of total is greater than or equal to 8.

select billing_address, cast(invoice_date as date) as invoice_date
from invoice
where total >= 8;


9.

 
