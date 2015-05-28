# Its very easy to install the program. #
<br />
<br />

Requirements:<br />
1. PHP 5 supported hosting<br />
2. Basic knowledge to know how to setup an application in facebook
3. Basic knowledge to know how to setup twitter application. Visit http://thinkdiff.net/category/twitter/http://thinkdiff.net/category/twitter/ <br />
4. Basic knowledge to know how to setup linkedin application. Visit http://thinkdiff.net/linkedin/integrate-linkedin-api-in-your-site/ <br />
<br />
Steps:
1. Visit http://www.facebook.com/developers and click setup new application. <br />
2. Provide application name, description.<br />
3. Provide the Connect URL. For my case I provide http://thinkdiff.net/demo/fblinkedtwit/ (because here i hosted the applications code) <br />
4. Click Save Changes and you'll get api and secret key.<br />
5. Now place those api and secret keys in the config.php<br />
```
$config['fb_api']               =   'xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx';
$config['fb_secret']            =   'yyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyy';
```
<br /><br />
6. Create a new application in twitter. Visit this page to learn how to create twitter application. http://thinkdiff.net/category/twitter/<br />
7. In twitter application setup set application website to http://yourdomain/yourproj/index.php. In my case it is http://thinkdiff.net/demo/fblinkedtwit/index.php<br />
8. In twitter application setup set callback url like http://yourdomain/yourproj/twitterauth.php. In my case it is http://thinkdiff.net/demo/fblinkedtwit/twitterauth.php<br />
9. After creating application update the config file<br />
```
$config['twitter_consumer']     =   'xxxxxx your app consumer key';
$config['twitter_secret']       =   'your app secret key';
```

10. Create a new application in linkedin. Visit http://thinkdiff.net/linkedin/integrate-linkedin-api-in-your-site/ to learn how to create linkedin application.<br />
11. In linkedin application setup set integration url http://yourdomain/yourproj/index.php. In my case it is http://thinkdiff.net/demo/fblinkedtwit/index.php<br />
12. In linkedin application setup set oAuth redirect url to http://yourdomain/yourproj/linkedinauth.php. In my case it is http://thinkdiff.net/demo/fblinkedtwit/linkedinauth.php<br />
13. After creating application update the config file<br />
```
$config['linkedin_access']      =   'xxx your linkedin application access key';
$config['linkedin_secret']      =   'yyy your linkedin application secret key';
```
<br />
14. Also update this configuation<br />
```
$config['base_url']             =   ''; // it would be url without file like <br />http://thinkdiff.net/demo/fblinkedtwit'
$config['callback_url']         =   ''; // like http://thinkdiff.net/demo/fblinkedtwit/index.php
```
<br /><br />
15. Upload all codes of this project in your hosting.<br />
16. Now visit your application. In my case the url is http://thinkdiff.net/demo/fblinkedtwit<br /><br />

Also remember: to update facebook status you must have to give status updated permission by clicking Give Status Update Permission<br /><br />

Run: <br />
1. Connect by facebook<br />
2. Give Twitter Access<br />
3. Give Linkedin Access<br /><br />

You may only give any one's permission like, only twitter access or linkedin access as your wish.<br /><br />

Now write something and click Update Status. Now check your sites like twitter,facebook or linkedin to see the update<br /><br />


Code:<br />
1. linkedin\_twitter folder contains twitter and linkedin library <br />
2. facebook folder contains facebook library<br />
<br />
3. config.php contains all the configuration settings <br />
4. class.fblinkedtwit.php is a class that contains some functions which are used to update status in facebook, twitter and linkedin. It also contains some functions those retrieve data from linkedin and twitter.<br />
5. statusupdate.php is used by ajax to update status. <br />
6. javascript.js contains all the essential javascript functions. <br />
7. index.php is the main file to entrance <br />
8. twitter.php and twitterauth.php are used for twitter authentication purpose. <br />
9. linkedin.php and linkedinauth.php are used for linkedin authentication purpose.