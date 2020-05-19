# Event-Finder
A small app using the GitHub Rest API to find events from specific user's repos.

JavaScript was chosen to avoid complications with user computers not having curl installed.

!! This documentation is for Windows !!

Before running, please install Node.js (and any dependencies), then use the now installed npm to run
"npm install http-server -g"
from your command line. This will allow you to use 
"http-server ."
to host the html file to localhost:8080. Other hosting methods should work fine as well.

Once hosting is complete, go to localhost:8080 from your web browser, and you will be met with a prompt to enter the username of the target repository's owner. This will be the username of the account that owns the repository for which you are trying to view the events of. Enter the username and press "OK" or press enter to continue.
This should bring up a new prompt asking for the name of the target repository as well as populate the main web page with up to thirty** repository names. Each of these names will be a link to the repository page on GitHub.com, clickable once the next steps are complete. If nothing appears on the main web page, one of 2 things has occured:

1. The username has no repositories associated with it.
2. The username was entered wrong.

Refresh the page to try again

Enter the name of the desired repository and you will be met with a new prompt asking if you'd like to filter event types. If you would not like to, press "OK" and the program will display up to thirty events from that repository with information on the type, date, and actor below the repository names. If you would like to filter, enter the event type you would like to filter for and press "OK." This will display all events with matching event types. Be sure to use the proper case and wording of the event type, available here: https://developer.github.com/v3/activity/event_types/

If nothing appears below the repository names, one of x things has occurred:

1.The repository does not exist.
2.The repository was entered wrong.
3.If an event filter was used, events of that type do not exist.
4.If an event filter was used, the event type was entered incorrectly

Refresh the page to try again

From this point, the repository links can be clicked and up to thirty events matching your filters should be displayed below the repository names. If you'd like to search a different repository, just refresh the page and the program will restart. Thanks for using!!


**While more than thirty repositories or events may exist, the program will still only display thirty due to default parameters in the github api. More can be shown through pagination or by requests, but these were not implemented in this iteration of the program for the sake of time and necessity.
