Challenge Question: Create a patient summary that shows patient_id, full name in uppercase, service in lowercase, age category (if age >= 65 then 'Senior', if age >= 18 then 'Adult', else 'Minor'), and name length. Only show patients whose name length is greater than 10 characters.

Query:
SELECT
    ->     patient_id,
    ->     UPPER(name) AS name,
    ->     LOWER(service) AS service,
    ->     CASE
    ->         WHEN age >= 65 THEN 'Senior'
    ->         WHEN age >= 18 THEN 'Adult'
    ->         ELSE 'Minor'
    ->     END AS age_category,
    ->     LENGTH(name) AS name_length
    -> FROM
    ->     patients
    -> WHERE
    ->     LENGTH(name) > 10;
+--------------+-------------------------+------------------+--------------+-------------+
| patient_id   | name                    | service          | age_category | name_length |
+--------------+-------------------------+------------------+--------------+-------------+
| PAT-09484753 | RICHARD RODRIGUEZ       | surgery          | Adult        |          17 |
| PAT-f0644084 | SHANNON WALKER          | surgery          | Minor        |          14 |
| PAT-ac6162e4 | JULIA TORRES            | general_medicine | Adult        |          12 |
| PAT-3dda2bb5 | CRYSTAL JOHNSON         | emergency        | Adult        |          15 |
| PAT-08591375 | GARRETT LIN             | icu              | Adult        |          11 |
| PAT-283cda07 | WILLIAM HERRERA         | emergency        | Adult        |          15 |
| PAT-5b61868c | ASHLEY WALLER           | icu              | Minor        |          13 |
| PAT-f9c8afa6 | VICTOR BAKER            | general_medicine | Adult        |          12 |
| PAT-5290be70 | JEFFREY CHANDLER        | emergency        | Adult        |          16 |
| PAT-003ce690 | LARRY DIXON             | icu              | Adult        |          11 |
| PAT-18f78014 | KENNETH SCOTT           | general_medicine | Senior       |          13 |
| PAT-69dc0dc1 | APRIL FROST             | general_medicine | Adult        |          11 |
| PAT-95afe21e | MICHELLE HARMON         | emergency        | Minor        |          15 |
| PAT-cc50ad71 | HELEN JONES             | surgery          | Adult        |          11 |
| PAT-0beb4754 | ERIN EDWARDS            | general_medicine | Senior       |          12 |
| PAT-3223420e | MICHELLE EVANS          | emergency        | Minor        |          14 |
| PAT-f0682772 | JASON POWELL            | general_medicine | Senior       |          12 |
| PAT-af65396f | CAMERON FISHER          | emergency        | Adult        |          14 |
| PAT-5e3f8747 | ELIZABETH KELLEY        | icu              | Adult        |          16 |
| PAT-ba5529f4 | DUSTIN JORDAN           | general_medicine | Adult        |          13 |
| PAT-208fd478 | MARY MARSHALL           | general_medicine | Minor        |          13 |
| PAT-127ca40e | DANIEL KENNEDY          | general_medicine | Senior       |          14 |
| PAT-f70aeea1 | REBECCA JACKSON         | icu              | Adult        |          15 |
| PAT-9bc45d47 | JOSE SCHULTZ            | emergency        | Minor        |          12 |
| PAT-13c9b20f | ROBERT POTTER           | surgery          | Minor        |          13 |
| PAT-cd63d937 | COURTNEY GONZALEZ       | emergency        | Adult        |          17 |
| PAT-1bc22a80 | DAVID ALVAREZ           | surgery          | Minor        |          13 |
| PAT-5044053e | ANGEL PERRY             | icu              | Senior       |          11 |
| PAT-f3846605 | CHEYENNE HORTON         | icu              | Adult        |          15 |
| PAT-736d270f | DAVID DOUGLAS JR.       | surgery          | Senior       |          17 |
| PAT-af250ef4 | PATRICIA RODRIGUEZ      | icu              | Minor        |          18 |
| PAT-eacf84b5 | CHRISTOPHER RUBIO       | surgery          | Senior       |          17 |
| PAT-8029775b | AMBER WRIGHT            | surgery          | Adult        |          12 |
| PAT-9ba7a6ee | JOYCE SOLIS             | emergency        | Senior       |          11 |
| PAT-029113eb | VICTORIA LARSON         | surgery          | Senior       |          15 |
| PAT-44c855d4 | STEPHANIE SALAZAR       | emergency        | Adult        |          17 |
| PAT-8b1e87b0 | KATHY RIVAS             | general_medicine | Senior       |          11 |
| PAT-fade1b7b | STEPHANIE MANNING       | general_medicine | Senior       |          17 |
| PAT-d4f82ecb | DAVID WRIGHT            | surgery          | Adult        |          12 |
| PAT-5b51b470 | PAMELA BOYD             | emergency        | Minor        |          11 |
| PAT-cb6b3892 | DENISE JONES            | general_medicine | Adult        |          12 |
| PAT-87783e44 | DEVON FLORES            | emergency        | Adult        |          12 |
| PAT-33d8d801 | BRENDA HALL             | icu              | Minor        |          11 |
| PAT-48f61d27 | MICHELLE BROWN          | surgery          | Adult        |          14 |
| PAT-24a653c8 | JOSHUA PERRY            | icu              | Senior       |          12 |
| PAT-0d00ca2c | JASON STEIN             | general_medicine | Adult        |          11 |
| PAT-70057243 | MELISSA GATES           | general_medicine | Adult        |          13 |
| PAT-84559395 | JAMIE SMITH             | surgery          | Senior       |          11 |
| PAT-581a47d8 | PAUL CASTANEDA          | emergency        | Minor        |          14 |
| PAT-851d3ef5 | JENNIFER ADKINS         | emergency        | Adult        |          15 |
| PAT-a2c2be76 | LINDSEY WALKER          | general_medicine | Adult        |          14 |
| PAT-ae81e45f | JEFFREY JOHNSON         | emergency        | Adult        |          15 |
| PAT-51e4d298 | MICHAEL POWELL          | emergency        | Senior       |          14 |
| PAT-deada259 | JOHN ANDERSON           | icu              | Adult        |          13 |
| PAT-73381b12 | ALYSSA LONG             | emergency        | Adult        |          11 |
| PAT-a4a957cb | JOEL WILLIAMS           | general_medicine | Minor        |          13 |
| PAT-a2ac2b3b | DANIEL MURPHY           | icu              | Adult        |          13 |
| PAT-64a781e0 | JAMIE WALTON            | surgery          | Adult        |          12 |
| PAT-54bd8932 | DARLENE MILLER          | general_medicine | Minor        |          14 |
| PAT-1e630d47 | JOSHUA COOKE            | icu              | Adult        |          12 |
| PAT-d1c95e77 | MATTHEW HARRINGTON      | general_medicine | Senior       |          18 |
| PAT-69802c02 | NICOLE HERRING          | icu              | Adult        |          14 |
| PAT-8b68dd5f | ALEX HERNANDEZ          | emergency        | Minor        |          14 |
| PAT-93f48cc9 | MICHAEL ELLIOTT         | general_medicine | Adult        |          15 |
| PAT-0477a000 | MICHAEL WANG            | emergency        | Minor        |          12 |
| PAT-efd9dfb4 | LAWRENCE ADKINS         | icu              | Adult        |          15 |
| PAT-1dd2fee7 | ROBERT OCONNELL         | general_medicine | Adult        |          15 |
| PAT-f316dd98 | ALEXANDER COLLINS       | icu              | Minor        |          17 |
| PAT-d6e424a7 | TINA SANDERS            | icu              | Adult        |          12 |
| PAT-9da5da0c | ANGELA VAUGHN           | emergency        | Adult        |          13 |
| PAT-d6009d2d | ASHLEY BARTON           | icu              | Adult        |          13 |
| PAT-93eef480 | LINDSAY MARTINEZ        | emergency        | Adult        |          16 |
