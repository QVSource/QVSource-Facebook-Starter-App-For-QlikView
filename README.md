QVSource Facebook Fan Page Starter App For QlikView
===================================================
IMPORTANT - You will need QVSource 1.4.7.1 or later to run this application. Please contact us for advanced access to this, otherwise it should be released in early August 2013.

This is a starter QlikView application showing how to get started using the [QVSource Facebook Pages and Groups Connector](http://wiki.qvsource.com/Facebook-Pages-Connector-for-QlikView.ashx) for QlikView.

Full documentation for this template application can be found [here](http://wiki.qvsource.com/QlikView-Connector-for-Facebook-Pages-Demo-Application.ashx).

It also makes use of the [Sentiment and Text Analytics Connector](http://wiki.qvsource.com/Sentiment-Analysis-And-Text-Analytics-Connector-For-QlikView.ashx) to score comments and posts.

If you are a QlikView + QVSource user you can simply click the ["Download ZIP"](https://github.com/QVSource/QVSource-Facebook-Starter-App-For-QlikView/archive/master.zip) button on GitHub to grab this application.

The content below is copied from the change log in the first tab of the load script.

Change Log
----------

1.9.1 - 30/07/13
----------------
* Added test to check vLocalTimeZone is recognised.
* Fiexed error on Comments tab: if(NoOfRows('Params') > 1) then ==> if(NoOfRows('Params') > 0) then
* Now uses new LikeCountForItem table to get feed item likes.
* Now configured to require QVSource 1.4.7.1 or later.
* Should no longer error if no feed items are found on the initial reload. This application is however is only designed to run properly when at least one feeditem and one comment is found.
* Moved to GitHub.
* Config file renamed to config.txt.
