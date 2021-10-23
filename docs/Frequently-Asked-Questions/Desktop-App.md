## How to recalculate stats on my activities?

Click the _[3-dots]_ button in top right and corner, then _Advanced menu_ > _Recalculate stats on all activities_.

[](id:calculate-compute-history-activity-activities)

## How to transfer athlete settings from legacy web extension to desktop app?

From old extension version **v6 or less**:

1. Open the old chrome extension app in your browser (version 6 or less only).
1. Press `F12` to display the developer's tools.
1. Click on `Console` tab.
1. `Copy` & `Paste` the following code into developer `Console`:
> `chrome.storage.local.get(null, r => console.log(btoa(JSON.stringify(r.athlete.datedAthleteSettings))));`
1. Tap `enter`.
1. A backup string should be returned as a result. It should be something like: `W3sibWF4S......m51bGx9XQ==`
1. `Copy` this string in your clipboard.
1. In the desktop app, go to `Athlete Settings` and click on upload athlete settings button.
1. `Paste` the string previously copied.
1. Your settings should be back ;)

[](id:transfert-athlete-settings-extension-desktop)


## Why 1st Strava sync takes so much time?

When syncing the Strava connector you probably got the following message: 

**_"Strava wants you to slow down...🐌 Resuming sync in X seconds..."_**.

This behavior is not an issue. This is a call limitation set up by Strava on their servers. The default Strava rate limit allows **100 requests every 15 minutes** and **1000 requests per day**. [More info here](https://developers.strava.com/docs/rate-limits/)

This means that your 1st Strava sync can take many hours to finish. Upcoming syncs with few activities on a daily or weekly basis will be instantaneous.

**💡 Tip: You can speed up your 1st Strava sync through the _"How to speed up the 1st Strava sync?"_ helper on this page.**

[](id:strava-connector-slow-first-sync)

## How to speed up the 1st Strava sync?

The 1st sync can take hours to complete if you have a large history (Enter _"id:strava-connector-slow-first-sync"_ in the help search bar for more info). To bypass this, here is what you can do:

1. First [request a download of your activities **(in step 2)**](https://www.strava.com/athlete/delete_your_account).
1. Unzip the downloaded archive to a location of your choice.
1. Using the **File connector**, select and sync the folder ⇾ _**"activities"**_.
1. Then, on the **Strava connector**, click _Configure_ and **tick** the option _**Override existing activities names, types and commute statuses with those fetched from Strava.**_.
1. Sync now the **Strava connector** with _Sync all activities_ button.
Only the activities names and types previously synced by the file connector will be updated. Every others and "heavy" network calls to Strava will be avoided.

And voilà 😉! Your 1st Strava sync has been done at speed of light. You can now use the Strava connector on your regular daily or weekly basis using the _Sync new activities_ button.

[](id:strava-connector-faster-first-sync)

## How to use Elevate with multiple users on same computer?

To use Elevate on same computer with multiple users, you have to create dedicated users accounts into your operating system. Then each user has to install Elevate into their own isolated environment. 

>📝 Independently of Elevate, creating multiple users in your operating system is actually a best practice if several people use the same computer. Although convenient, one shared account between users on same computer is NOT recommended.

Here is how to create a new local user on:

- [Windows](https://support.microsoft.com/en-us/windows/create-a-local-user-or-administrator-account-in-windows-10-20de74e0-ac7f-3502-a866-32915af2a34d) | [additional help](https://duckduckgo.com/?q=site%3Amicrosoft.com+create+windows+user)
- [Mac OS](https://support.apple.com/guide/mac-help/set-up-other-users-on-your-mac-mtusr001/mac) | [additional help](https://duckduckgo.com/?q=site%3Aapple.com+create+mac+user)
- [Linux (Ubuntu distrib)](https://help.ubuntu.com/stable/ubuntu-help/user-add.html.en) | [additional help](https://duckduckgo.com/?q=site%3Aubuntu.com+create+new+user)

[](id:multiple-accounts-users-same-computer)
