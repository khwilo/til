# Database Configuration  

The database configuration is located at `/config/database.php`.  

MySQL will be used as the database engine but you can change it to a database management system of your choice.  

Things you may want to update:  
1. database  
`'database' => env('DB_DATABASE', 'dbname')`  
2. username  
`'username' => env('DB_USERNAME', 'uname')`  
3. password  
`'password' => env('DB_PASSWORD', 'abcd1234')`  


