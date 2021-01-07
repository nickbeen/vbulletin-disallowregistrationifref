# Anti-spambot: disallow registration if referer page = register.php

This is an extra percussion to limit the spam on your forum. This product is likely to function on vBulletin 3.6.x to vBulletin 3.8.x.

**What does this product do to limit potential spam?**  
After doing research on my forum, I noticed 80% of all spambots visiting my register.php page, used the same register.php page as the refering page. This is automatic spambot behavior, because it's likely your members click the register link on your forum index and not on the same register page.

Request header | Request response
----- | -----
Request | www.myvbulletinforum.com/forum/register.php
Accept | text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Encoding | gzip, deflate
Accept-Language | en-us;q=0.7,en;q=0.3
Cookie | bblastvisit=1370691249; bblastactivity=0
DNT | 1
Host | www.myvbulletinforum.com
Referer | www.myvbulletinforum.com/forum/register.php
User-Agent | Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1; SV1; FunWebProducts; .NET CLR 1.1.4322; PeoplePal 6.2)

It's likely in doing so, because a lot of websites block targeted entries if there is no refering page used (general bad idea, though). With this product, they will get served a blank page when trying to enter your register.php page with your register.php page as a referer.

It adds an extra layer of security, next to your other security measures on your bot. On my forum, 80% of those requests get a blank page served and not even had to rely on my other anti-spam measures on the actual register page. Also note that the register page is close to 30kB to load, this product will save you a lot of bandwidth if your register page is also visited 80% of the times by spambots with a referer to your register.php page.

````
Conditions:
- The spambot/user request the page: www.myvbulletin.com/forum/register.php
- The refering page of the requested page is also: www.myvbulletinforum.com/forum/register.php

Result:
- The spambot/user gets a blank page of 0kB served
````

**Is this all I need?**  
This product can work great against preprogrammed spambots, who are programmed to search on the internet to forums with an existing page on the pagerequest of www.myvbulletinforum.com/forum/register.php and variations. This product won't help against human spammers.

No settings required, all you have to do is install the product.

**History**  
1.0 - Initial release  
1.1 - Bug fix  
1.2 - Bug fix
