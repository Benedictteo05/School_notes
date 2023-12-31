### SQL Injection  (SQLi)
- Occurs when an attacker is able to manipulate SQL statements through data inputs of an application.
- Attackers can possibly modify SQL statement in a vulnerable application via forms or parameters.
- Impacts:
	1. Data loss or corruption, lack of accountability, or denial of access.
	2. May lead to gaining access to vulnerable system.

### In-band SQL injection (Simple SQLi)
- Most common SQL injection 
- The same channel was used to launch the attack and obtain the result
- Error-based & Union-based

### Error-based SQLi
- An error-based SQL injection technique relies on error message thrown by the database server to obtain information about the structure of the database.

### Union-based SQLi
- Leverage the UNION SQL operator to combine the results of two or more SELECT statements into a single result, which is then returned as part of the HTTP response.

### Inferential SQL injection (Blind SQLi)
- Attackers sends data payloads to the server and observes the response and behavior of the server to learn more about its structure. (data is not transferred from the website database to the attacker)
- Attackers are not able to see the results of an attack as no data is transferred via the web application (Blind SQLi)
- Boolean-based blind SQLi and Time-based blind SQLi

### Boolean-based blind SQLi
- Relies on sending an SQL query to the database, which forces the application to return a TRUE or FALSE result.

### Time-based blind SQLi
- Forces the database to wait for a specified amount of time (in seconds) before responding. The response time will indicate to the attacker whether the result of the query is TRUE or FALSE.

### Example 1
```
-- Designed to always return TRUE
SELECT * from Account WHERE
admin = '' or 1=1 -- ' AND password = '';
======================================================
Effecively becomes:
admin = '' or 1 = 1;
Which always returns TRUE
```
- Comment symbol (--) to turn everything placed after the last placeholder into a comment.

### Example 2
```
-- Inside username field in Login
' UNION SELECT Username, password FROM Account --
======================================================
Effecively becomes:
SELECT * from Account WHERE admin = '' UNION SELECT Username, password FROM Account -- ';

OR 
SELECT * FROM Account WHERE Admin = ''; DROP TABLE Account --';
```

### SQLi Prevention
- Primary Defenses
	1. Use Parameterized Queries (Prepared Statements)
		- Allows to differentiate between code and data.
		- Ensure the attacker is not able to manipulate the query.
			- Even if 'or 1=1--' is passed as parameter.
	2. Use Parameterized Stored Procedure
		- To prevent users from directly interacting with SQL code.
		- SQL code is defined and stored in the database.
	3. Encoding all User Supplied Input
		- Improper encoding or escaping can allow attackers to change the commands that are sent to another component, inserting malicious commands instead.
		- Use the `httpUtility.HtmlEncode(dangerous_string)` to avoid characters that could lead to an unintended SQL command.
- Additional Defenses:
	- Use white list input validation
	- Use a low privileged account to run the database