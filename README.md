# wprocket-test
This is a task that helps clear a client's cache at a specific time. The following lines are the response I will send to a Level 1 teammate.

This script will help you to clear the cache at a specific time.

# How to use
* First download this file.
* Then upload this file to your WordPress installation's root ( where wp-config.php and wp-load.php are located).

<strong>Note:</strong> If you place it in a different location, you need to edit the path in require( 'wp-load.php' ); above to match its location.

* Next, you need to create a cron job, from your web hosting control panel. You can set the cron job to the time you want the cache cleared.
For this you need to create the cron Job example: </br>
<code> wget -q -O - http://yourdomain.com/wprocket-clean-domain.php?doing_wp_cron >/dev/null 2>&1 </code> 

<strong>Note:</strong> Please remember to replace yourdomain.com with your actual domain:
Each server has different ways of adding a Cron job, so if you are not sure how to do it you can ask your hosting provider to help you.

For extra documentation about creating cron jobs, you can check this resource: <a href="https://docs.wp-rocket.me/article/1279-cron-and-wp-rocket#setting-up-cron-job-single-site">CRON and WP Rocket</a>

# troubleshoot based on the solution provided above
1. First, I would check the cron job created before is correct and that the client has uploaded the file with the correct code in this case:"wprocket-clean-domain.php".
2. After verifying that both are correct, through the URL: http://yourdomain.com/wprocket-clean-domain.php I would execute the script to verify that it is not a server-side error.
3. In case the error persists, I would also check the wp-content folder permissions specifically the cache folder.

<strong>Note:</strong> To troubleshoot this problem I assumed that:
* I have tested my code on my environment and it works fine and 
* the customer has provided me access to their site/server.
