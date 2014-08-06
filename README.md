QVSource Facebook Fan Page & Groups Starter App For QlikView
===================================================
IMPORTANT - You will need QVSource 1.5.4.6 or later to run this application as it ONLY works with the Facebook Pages & Groups Connector v2.

If you are using an older version of QVSource or the Facebook Fan Pages Connector v1, then you need to use an older version of this application, which can be found [here](https://github.com/QVSource/QVSource-Facebook-Starter-App-For-QlikView/releases)

This is a starter QlikView application showing how to get started using the [QVSource Facebook Pages and Groups Connector](http://wiki.qvsource.com/Facebook-Fan-Pages-And-Groups-Connector-For-QlikView-(v2).ashx) for QlikView.

Full documentation for this template application can be found [here](http://wiki.qvsource.com/QlikView-Connector-for-Facebook-Pages-Demo-Application.ashx).

It also makes use of the [Sentiment and Text Analytics Connector](http://wiki.qvsource.com/Sentiment-Analysis-And-Text-Analytics-Connector-For-QlikView.ashx) to score comments and posts.

If you are a QlikView + QVSource user you can simply click the ["Download ZIP"](https://github.com/QVSource/QVSource-Facebook-Starter-App-For-QlikView/archive/master.zip) button on GitHub to grab this application.

The content below is copied from the change log in the first tab of the load script.

Change Log
----------
2.0.0.0 - 05/08/14
------------------
* YOU MUST HAVE QVSource version 1.5.4.6 or later to use this application
* upgraded to ONLY WORK with the Facebook Pages and Groups Connector (v2)
* If you are looking for a version of this application to work with Facebook Pagess and Groups Connector v1, then please look here: https://github.com/QVSource/QVSource-Facebook-Starter-App-For-QlikView/releases
* BREAKING CHANGE:  Removed Sentimental (formerly Chatterbox) connectivity - this is because Sentimental have now removed their API from Mashape and as such we are no longer able to offer it either. If you have used this
then please update the config.txt file to utilise a different Sentiment Analytics API engine
* Changed 'since' parameter to 'StartDate' for the FeedItems' load URL string
* Replaced remaining port 5555 references to use the variable
* Fixed issue where script was testing for feeditem comments being 'true', but should have been testing for 'True'
* Fixed issue where the FB_Feed table had duplicate rows

1.9.2.5 - 11/05/14
------------------
* Fixed issue where real like and comment counts were not coming through if greater than 25 (by setting vLikeCountThreshold and vCommentCountThreshold to 24).

1.9.2.4 - 21/03/14
------------------
* Fixed old QVSource logos.

1.9.2.3 - 19/03/14
------------------
* Added FeedItems_comment_link and FeedItems_like_link fields to Feed Item data. This is a link which allows you to open the specific post in a browser.
* Added response_status fields to Poster and Commenter tables.

1.9.2.2 - 11/12/13
------------------
* Changed FeedItem_comments_count2 to FeedItem_comments_count in CH26, CH27 y CH32.

1.9.2.1 - 04/12/13
------------------
* Updated badge.

1.9.2.0 - 30/08/13
------------------
* BREAKING CHANGES - This new version will not be compatible with QVDs from a previous version.
* IMPORTANT - This version requires QVSource 1.4.7.5 or later.
* Added columns to feed table:
from_id as FeedItem_from_id,
status_type as FeedItem_status_type,
to_id as FeedItem_to_id,
to_name as FeedItem_to_name,
to_category as FeedItem_to_category,
story as FeedItem_story,
application_name as FeedItem_application_name,
application_namespace as FeedItem_application_namespace,
application_id as FeedItem_application_id,
has_at_least_this_many_likes as FeedItem_has_at_least_this_many_likes,
has_at_least_this_many_comments as FeedItem_has_at_least_this_many_comments,
* Added new vLikeCountThreshold and vCommentCountThreshold to config file and associated logic/loadscript. See notes in config file for more detail.
* vIgnoreCache moved to config file.
* Added warning notes on intro tab when vLoadCommentCountForFeedItems or vLoadLikeCountForFeedItems are not set to 1.
* App is now set to require QVSource 1.4.7.5.

1.9.1.2 - 02/08/13
------------------
* Added let vLoadCommentCountForFeedItems and vLoadLikeCountForFeedItems flags to config file. Currently recommended that these are turned off.

1.9.1.1 - 01/08/13
------------------
* vIsFirstTime flag is now based on the existence of FB_Feed.qvd instead of FB_Page.qvd

1.9.1 - 30/07/13
----------------
* Added test to check vLocalTimeZone is recognised.
* Fiexed error on Comments tab: if(NoOfRows('Params') > 1) then ==> if(NoOfRows('Params') > 0) then
* Now uses new LikeCountForItem table to get feed item likes.
* Now configured to require QVSource 1.4.7.1 or later.
* Should no longer error if no feed items are found on the initial reload. This application is however is only designed to run properly when at least one feeditem and one comment is found.
* Moved to GitHub.
* Config file renamed to config.txt.
