# WP Rocket Assessment
This is a task that helps clear a client's cache at a specific time. The following lines are the response I would send to a <strong>Level 1</strong> teammate.


# How to use
* First download <a href="https://github.com/rosamillan/wprocket-assessment/blob/main/wprocket-clean-domain.php">this file.</a>
* Then upload this file to the WordPress installation's root ( where wp-config.php and wp-load.php are located).

<strong>Note:</strong> If you place it in a different location, you need to edit the path in require( 'wp-load.php' ); above to match its location.

* Next, Client needs to create a cron job, from their web hosting control panel. They can set the cron job to the time they want the cache cleared.
For this they need to create the cron Job, example: </br>
<code> wget -q -O - http://yourdomain.com/wprocket-clean-domain.php >/dev/null 2>&1 </code> 

<strong>Note:</strong> Please, remember to replace "yourdomain.com" with your actual domain. Each server has different ways of adding a Cron job, so if the client is not sure how to do it, he should ask his hosting provider for help.

If the client is using cPanel, share this short video for reference: <a href="https://recordit.co/A4Jj1Kg7x9">video</a>

# troubleshoot based on the solution provided above
1. First, I would check the cron job created before is correct and that the client has uploaded the file with the correct code in this case: <a href="https://github.com/rosamillan/wprocket-assessment/blob/main/wprocket-clean-domain.php">"wprocket-clean-domain.php".</a>
2. After verifying that both are correct, through the URL: http://yourdomain.com/wprocket-clean-domain.php I would execute the script to verify that it is not a server-side error.
3. I would also activate the PHP and WordPress error logs and verify if there is an error. 
4. In case the error persists, I would also check the wp-content and cache folders permissions.

<strong>Note:</strong> To troubleshoot this problem I assumed that:
* I have tested my code on my environment and it works fine and 
* the customer has provided me access to their site/server.
