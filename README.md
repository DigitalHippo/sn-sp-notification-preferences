# sn-sp-notification-preferences
ServiceNow Service Portal Notification Preferences

As you may (or may not) know, one main item missing from the current Service Portal is a way for end users to manage their Notification & Subscription preferences. Currently the only options around this limitation are to either create a custom widget or to create an iframe which utilizes the Notification Preferences UI page.

Now the latter will only work if you have the system property "glide.notification.preference.ui.enabled" set to false as of Jakarta, Notification Preferences are shown in the System Settings. Setting this property to false will allow you to use the iframe method but it will also change the way all users of the platform manage their preferences i.e they will use the UI page rather than the System Settings.

This has created a major roadblock when we have started the process of moving existing CMS users to the Service Portal as simply changing the System Property was not an option we wanted to entertain. After searching the community for anyone else who has effectively solved this issue I was unable to find any actual solution thus I have created a custom widget which mimics all of the features available for Notification & Subscription Preference management.

The OOB Knowledge Subscription & Notification Preferences widget was used as the base and then new functions were created to use the Notification Preferences API (/api/now/v1/notification/preference). This is the API which is used by the System Settings for notification management. The widget , ng-templates, and a portal page "notification_preferences" are included in the attached XML for your use. Im sure there are improvements which can be made to the widget but hopefully this will help anyone who finds themselves with the same need as I did.

Screenshots

Notifications By Category:

find_real_file.png

 

New Personal Notification:

find_real_file.png

 

Category Notifications:

find_real_file.png

 

Notification Channel Edit:

find_real_file.png

Notification Channels:

find_real_file.png

 

New Channel:

find_real_file.png
