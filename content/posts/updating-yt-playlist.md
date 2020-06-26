---
title: "\"A YouTube playlist but everytime someone adds a tune to a Facebook group it updates too\""
date: 2020-06-12T17:07:24+01:00
summary: "If you're anything like me then you might find you spend a bit too much time on Facebook on various music groups.
          A mate of mine who runs one of these music groups was meticulously adding every track posted in the group to a YouTube playlist. 
          I sought out to make this process less painful and fully automated. Here is a short guide outlining how you can set up the same thing for your Facebook group, as long as Zuckerburg decides not to change the rules..."
---

If you're anything like me then you might find you spend a bit too much time on Facebook on various music groups.
A mate of mine who runs one of these music groups was meticulously adding every track posted in the group to a YouTube playlist. 
I sought out to make this process less painful and fully automated. Here is a short guide outlining how you can set up the same thing for your Facebook group, as long as Zuckerburg doesn't change the rules...

To get this set up you will need three things:
1. An [integromat.com](https://www.integromat.com/) account.
1. A Facebook account that is the admin of the Facebook group you want to scrape the videos from.
1. A YouTube account for the playlist to live on.

## Integromat Scenario

This first thing that we'll be getting set up is something called an Integromat Scenario, this will be the bulk of the work with the only others things to do being connecting it to the right places in Facebook and YouTube.

1. To create the scenario in integromat you will click the 'Create a new scenario' button on the dashboard, skip the service integration that pops up.
1. Download this [blueprint file.](/blueprint.json) (Right click -> save link as)
1. Once you've opened that up you will click the '...' button labelled more and click 'Import Blueprint', select the blueprint file you downloaded in the previous step.
1. You should now see modules in your scenario. Click on the Facebook groups module and add a connection to your Facebook account which should open a Facebook window, click 'OK'.
1. Now on the Facebook groups module you will be able to choose the Facebook group you want to scrape. Make sure you also set the limit to '999'. You will be prompted to choose where you start scraping posts from, if you want Youtube links previously posted choose 'All'.
1. For integromat to have access to your group you will need to add the Integromat App. As an admin of the Facebook group you will need to 'Edit group settings' and click 'Add Apps'. At the time of writing you will need to wait a while for this to load... Once loaded search for 'Integromat' and add this app.
1. Click on the YouTube module and add a Google connection to the Youtube channel your playlist lives on.
1. Before the YouTube connection can work you will need to follow the instructions in this [link](https://support.integromat.com/hc/en-us/articles/360025257393-Connecting-YouTube-to-Integromat-via-Google-OAuth-Client). Once you've sorted that you will need to paste in the client ID and secret you created into the advanced settings of the YouTube module. You may need to click 'Proceed unsafe' when prompted that the app is not verified.
1. Now choose your playlist in the youtube module and for Video ID click 'Link'.
1. If the text parser module is not working, try deleting what is currently in the text field and click 'Link'. You will also want to do this for the filter between the modules, "youtube link".
1. You can change the schedule for this scenario by clicking the clock on the facebook module. I would recommend running this on the Every day setting.