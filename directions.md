jenni=# CREATE DATABASE apartmentlab;
jenni=# CREATE TABLE owners(id SERIAL PRIMARY KEY NOT NULL, name VARCHAR(50), number of units INTEGER, owner id NOT NULL);

*schema has to be public


1. \dt
2. SELECT User FROM mysql.user  
ERROR: relation "mysql.user" does not exist

3. SELECT * FROM owners;
4. SELECT name FROM owners;
5. SELECT age FROM owners ORDER BY age ASC;
6. SELECT name FROM owners WHERE name='Bonnie Blalock';
7. SELECT * FROM owners WHERE age > 30;
8. SELECT name FROM owners WHERE name LIKE 'B%';
9. INSERT INTO owners (name, age) VALUES ('John', 33);
10. INSERT INTO owners (name, age) VALUES ('Jane', 43);
11. UPDATE owners SET age='30' WHERE name='Jane';
12. UPDATE owners SET name='Janet' WHERE name='Jane';
13. INSERT INTO properties (name, units, owner_id) VALUES ('Archstone', 20, 4);
14. DELETE FROM owners WHERE name = 'Janet';
15. SELECT * FROM properties WHERE name NOT IN ('Archstone') AND property_id NOT IN (3, 5) ORDER BY name ASC;
16. SELECT count (*) FROM properties;
17. SELECT * FROM owners ORDER BY age DESC LIMIT 1;
18. SELECT * FROM owners LIMIT 3;
19. ALTER TABLE properties ADD CONSTRAINT owners_fk FOREIGN KEY (owner_id) REFERENCE owners (owner_id) ON DELETE NO ACTION;
20. SELECT * FROM owners JOIN properties ON owner.id = properties.owner_id;
ERROR: missing FROM - clause entry for table "owner"

