Delete largon/data/mysql-8
cd to laragon/bin/mysql8.0.0.x/bin folder via cmder (important for step 3)
run 'mysqld --initialize --console' (remember the password)
run 'start mysqld'
run 'mysql -u root -p'
put in the password from 3.
You are now in mysql shell and can remove the password again: "ALTER USER 'root'@'localhost' IDENTIFIED BY '';"
run 'exit' and ctrl + c the spawned tab from step 4.
