# 2.2: MySQL queries: 

## Store Database

We have the product and manufacturer tables, each with the following fields:
- product (code, number, price, manufacturer_code)
- manufacturer (code, number)
The 'manufacturer_code' field of the product entity is related to the 'code' field of the manufacturer.
Please make the following inquiries:

<ol id="yui_3_17_2_1_1645156986537_112">
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Lists the names of all the products in the product table.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Lists the names and prices of all products in the product table.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Lists all columns in the product table.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">List the product name, price in Euros, and price in US Dollars (USD).</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">List the product name, price in Euros, and price in US Dollars (USD). </font><font style="vertical-align: inherit;">Use the following aliases for columns: product name, euros, dollars.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Lists the names and prices of all products in the product table, converting the names to uppercase.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Lists the names and prices of all products in the product table, converting the names to lowercase.</font></font></li>
                    <li id="yui_3_17_2_1_1645156986537_111"><font style="vertical-align: inherit;" id="yui_3_17_2_1_1645156986537_110"><font style="vertical-align: inherit;" id="yui_3_17_2_1_1645156986537_109">List the names of all the manufacturers in one column, and in another column, capitalize the first two characters of the manufacturer's name.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Lists the names and prices of all products in the product table, rounding the value of the price.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Lists the names and prices of all products in the product table, truncating the value of the price to show it without any decimal place.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Lists the code of the manufacturers who have products in the product table.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Lists the code of the manufacturers who have products in the product table, removing the codes that appear repeatedly.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Lists the names of the manufacturers in ascending order.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Lists the names of the manufacturers in descending order.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Lists the product names sorted first by name in ascending order and second by price in descending order.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Returns a list with the first 5 rows of the manufacturer table.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Returns a list with 2 rows from the fourth row of the manufacturer table. </font><font style="vertical-align: inherit;">The fourth row should also be included in the answer.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">List the name and price of the cheapest product. </font><font style="vertical-align: inherit;">(Use only the ORDER BY and LIMIT clauses). </font><font style="vertical-align: inherit;">NOTE: I could not use MIN (price) here, I would need GROUP BY</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">List the name and price of the most expensive product. </font><font style="vertical-align: inherit;">(Use only the ORDER BY and LIMIT clauses). </font><font style="vertical-align: inherit;">NOTE: I could not use MAX (price) here, I would need GROUP BY.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Lists the name of all products of the manufacturer whose manufacturer code is equal to 2.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Returns a list with the product name, price, and manufacturer name of all products in the database.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Returns a list with the product name, price, and manufacturer name of all products in the database. </font><font style="vertical-align: inherit;">Sort the result by manufacturer's name, in alphabetical order.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Returns a list with the product code, product name, manufacturer code, and manufacturer name of all products in the database.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Return the name of the product, its price and the name of its manufacturer, the cheapest product.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Return the name of the product, its price and the name of its manufacturer, the most expensive product.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Returns a list of all products from the manufacturer Lenovo.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Returns a list of all products from the manufacturer Crucial that are priced above € 200.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Returns a list of all products from Asus, Hewlett-Packard and Seagate. </font><font style="vertical-align: inherit;">Without using the IN operator.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Returns a list of all products from Asus, Hewlett-Packard and Seagate. </font><font style="vertical-align: inherit;">Using the IN operator.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Returns a list with the name and price of all the products of the manufacturers whose name ends with the vowel e.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Returns a list with the name and price of all products whose manufacturer's name contains the character w in their name.</font></font></li>
                    <li>Retorna un llistat amb el nom de producte, preu i nom de fabricant, de tots els productes que tinguin un preu major o igual a 180€. Ordeni el resultat en primer lloc pel preu (en ordre descendent) i en segon lloc pel nom (en ordre
                        ascendent)
                    </li>
                    <li>Retorna un llistat amb el codi i el nom de fabricant, solament d'aquells fabricants que tenen productes associats en la base de dades.</li>
                    <li>Retorna un llistat de tots els fabricants que existeixen en la base de dades, juntament amb els productes que té cadascun d'ells. El llistat haurà de mostrar també aquells fabricants que no tenen productes associats.</li>
                    <li>Retorna un llistat on només apareguin aquells fabricants que no tenen cap producte associat.</li>
                    <li>Retorna tots els productes del fabricador Lenovo. (Sense utilitzar INNER JOIN).</li>
                    <li>Retorna totes les dades dels productes que tenen el mateix preu que el producte més car del fabricador Lenovo. (Sense utilitzar INNER JOIN).</li>
                    <li>Llista el nom del producte més car del fabricador Lenovo.</li>
                    <li>Llista el nom del producte més barat del fabricant Hewlett-Packard.</li>
                    <li>Retorna tots els productes de la base de dades que tenen un preu major o igual al producte més car del fabricador Lenovo.</li>
                    <li>Llesta tots els productes del fabricador Asus que tenen un preu superior al preu mitjà de tots els seus productes.</li>
                </ol>


## University database 


Please download the schema_universidad.sql file database, view the ER diagram in an editor, and perform the following queries:

<ol id="yui_3_17_2_1_1645156986537_125">
                    <li id="yui_3_17_2_1_1645156986537_124"><font style="vertical-align: inherit;" id="yui_3_17_2_1_1645156986537_123"><font style="vertical-align: inherit;" id="yui_3_17_2_1_1645156986537_122">Returns a list with the first surname, second surname and first name of all students. </font><font style="vertical-align: inherit;">The list must be sorted alphabetically from lowest to highest by first, last and last name.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Find out the first and last names of students who have not registered their phone number in the database.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Returns the list of students who were born in 1999.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Returns the list of teachers who have not registered their phone number in the database and also their nif ends in K.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Returns the list of subjects taught in the first semester, in the third year of the degree that has the identifier 7.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Returns a list of teachers along with the name of the department to which they are linked. </font><font style="vertical-align: inherit;">The list must return four columns, first surname, second surname, first name and first name of the department. </font><font style="vertical-align: inherit;">The result will be sorted alphabetically from lowest to highest by last name and first name.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Returns a list with the name of the subjects, start year and end year of the student's school year with number 26902806M.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Returns a list with the names of all the departments that have professors who teach a subject in the Degree in Computer Engineering (Syllabus 2015).</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Returns a list of all students who have enrolled in a subject during the 2018/2019 school year.</font></font></li>
                </ol>


Solve the following 6 queries using the LEFT JOIN and RIGHT JOIN clauses.

<ol id="yui_3_17_2_1_1645156986537_130">
                    <li id="yui_3_17_2_1_1645156986537_129"><font style="vertical-align: inherit;" id="yui_3_17_2_1_1645156986537_128"><font style="vertical-align: inherit;" id="yui_3_17_2_1_1645156986537_127">Returns a list with the names of all teachers and related departments. </font><font style="vertical-align: inherit;">The list should also show those teachers who have no associated department. </font><font style="vertical-align: inherit;">The list must return four columns, name of the department, first surname, second surname and name of the teacher. </font><font style="vertical-align: inherit;">The result will be sorted alphabetically from lowest to highest by department name, last name, and first name.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Returns a list of teachers who are not associated with a department.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Returns a list of departments that do not have associate professors.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Returns a list of teachers who do not teach any subject.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Returns a list of subjects that do not have a teacher assigned.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Returns a list of all departments that have not taught subjects in any school year.</font></font></li>
                </ol>

Summary queries:

<ol id="yui_3_17_2_1_1645156986537_131">
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Returns the total number of students.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Calculate how many students were born in 1999.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Calculate how many teachers there are in each department. </font><font style="vertical-align: inherit;">The result should only show two columns, one with the name of the department and one with the number of teachers in that department. </font><font style="vertical-align: inherit;">The result should only include departments that have associate professors and should be sorted from highest to lowest by the number of professors.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Returns a list with all the departments and the number of teachers in each of them. </font><font style="vertical-align: inherit;">Please note that there may be departments that do not have associate professors. </font><font style="vertical-align: inherit;">These departments should also be listed.
                    </font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Returns a list with the names of all the existing degrees in the database and the number of subjects each has. </font><font style="vertical-align: inherit;">Note that there may be degrees that do not have associated subjects. </font><font style="vertical-align: inherit;">These degrees must also appear in the list. </font><font style="vertical-align: inherit;">The result must be ordered from highest to lowest by the number of subjects.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Returns a list with the names of all the existing degrees in the database and the number of subjects that each has, of the degrees that have more than 40 associated subjects.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Returns a list showing the name of the degrees and the sum of the total number of credits available for each type of subject. </font><font style="vertical-align: inherit;">The result must have three columns: name of the degree, type of subject and the sum of the credits of all the subjects that exist of this type.</font></font></li>
                    <li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Returns a list showing how many students have enrolled in a subject in each of the school years. </font><font style="vertical-align: inherit;">The result must show two columns, one column with the start year of the school year and another with the number of students enrolled.</font></font></li>
                    <li>Retorna un llistat amb el nombre d'assignatures que imparteix cada professor. El llistat ha de tenir en compte aquells professors que no imparteixen cap assignatura. El resultat mostrarà cinc columnes: id, nom, primer cognom, segon
                        cognom i nombre d'assignatures. El resultat estarà ordenat de major a menor pel nombre d'assignatures.</li>
                    <li>Retorna totes les dades de l'alumne més jove.</li>
                    <li>Retorna un llistat amb els professors que tenen un departament associat i que no imparteixen cap assignatura.</li>
                </ol>