# APPLICATION CONFIGURATION

The application configuration is usually found in `/config/app.php`.  

1. Set the debugging mode - This is used to determine how much information should be displayed when an error occurs.  
2. Set the time zone - setting used by PHP date-time functions.
3. Application key - value used for encryption purposes.  

## Debugging mode  

Locate the following code:  
`'debug' => env('APP_DEBUG',false)`  
Update it to:
`'debug' => env('APP_DEBUG', true)`  

Setting debugging mode to *true* enables Laravel to display detailed information when an error occurs. Useful for troubleshooting purposes.  

## Time zone
Locate the following code:  
`'timezone' => 'UTC'`  

The above code sets the timezone to UTC. You can place the value of your prefered timezone.  

## Application key  

Locate the following code:  
`'key' => env('APP_KEY')`  

Set the key to a random, 32 character string.
