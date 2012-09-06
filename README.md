playbook_gps_test
=================

This is based off of rim's gps test page (http://supportforums.blackberry.com/t5/Web-and-WebWorks-Development/Using-HTML5-Geolocation-in-your-Web-or-BlackBerry-WebWorks/ta-p/630406).
However, I've added modifications to figure out if gps was working when wifi was on/off. So sorry if I've stepped on any toes regarding
copyright/legal stuff. I think it was all apache 2 so I think I'm in the clear...

Anyways, there have been numerous discussions on the phonegap/cordova mailing list about geolocation constantly timing out so I felt like creating a 
small test app to sanely know if gps was working when wifi was on or not. It appears that geolocation is a little flaky on blackberry devices
and according to some forum posts, it may take up to 5 minutes to actually get a signal back. 

So if you're a person who wants to know if GPS is working on your playbook, try running this app, push the get location button and see how long it takes
to get a signal. 

How to run:
=================
Just drop the contents of this repo into your www/ folder and use the cordova command line tools to run on device. Just remember
to keep the ext-air/ and playbook/ folders in the www/ folder since the build tool looks for those when you run ./cordova/debug playbook
or ant playbook load-device. 

Once the app is running on device, simply hit the "Get GPS Location" button. In all of the cases I've tested this, I always get results within 10 seconds
with an accuracy of around 40. However, for whatever reason - some people can take up to five minutes to get a signal so try to keep that in mind.

To note: this actually doesn't use any phonegap/cordova calls to test the gps. In fact, the phonegap/cordova api actually uses the 
built in navigator.geolocation object anyways so having the phonegap/cordova javascript is un-necessary. 



