# modown-sql-Injection
In the Modown Wordpress Theme <=9.1 version, there is an SQL injection vulnerability in the "id" parameter of the /action/collect.php file. Attackers can execute arbitrary SQL statements by constructing malicious requests, which may lead to data leakage, data tampering, or other malicious operations.


([Modown Wordpress Theme](https://www.mobantu.com/7191.html) "Click here to download the theme")

There is an SQL injection vulnerability in the "id" parameter of the /action/collect.php file.
The id parameter is directly spliced ​​into the SQL statement without filtering
<img width="1054" alt="image" src="https://github.com/user-attachments/assets/7ef4c7c8-3c6b-4cdf-98b3-aaddf63d55bf" />

Authenticated users (only subscriber permissions are needed) can initiate requests to this interface. Specially constructed id parameters can lead to SQL injection, causing database data leakage and further obtaining system control permissions.

## Proof of Concept

### install the theme
