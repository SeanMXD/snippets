/*
From https://stackoverflow.com/a/8248281

Note 1: This does not execute the DROP statements, it just gives you a list of them. You will need to cut and paste the output into your SQL engine to execute them.

Note 2: If you have VIEWs, you'll have to correct each DROP TABLE `VIEW_NAME` statement to DROP VIEW `VIEW_NAME` manually.
*/

SELECT concat('DROP TABLE IF EXISTS `', table_name, '`;')
FROM information_schema.tables
WHERE table_schema = 'MyDatabaseName';
