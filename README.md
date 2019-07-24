# Issue
The application contains a vulnerability that allows an
attacker to view account data of other users. This class
of vulnerability is called an insecure direct object
reference.
The vulnerability is exploited on this resource:
* http://umbrella.com/accounts/id?=465246
The **id** parameter can be iterated to a different
number like **465245** which will give an attacker access
to another users private data.
# Steps to Reproduce
1.
2.
3.
4.
5.
Log into the Umbrella Bank as your @bugcrowdninja.com username.
Navigate to the Account details page.
Notice that there is an id parameter in the query string.
Attach this id parameter into the query string of any page that
you would like to access as a different user.
Change id parameter into a different number other than your own
account on the checking account page.
You will now be looking at another Iron Bank user's account
details and see another user's gold, bitcoin, and ethereum
holdings.
<snip>
