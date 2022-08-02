>Approximately 5 minutes to read this guide and configure spam filters


[**uBlock Origin**](https://ublockorigin.com) is a great content blocker extension for the most widely used browsers (even on mobile/tablets where supported).

We'll use it to block specific elements of the Investing.com forum that contain all the spam.

Once you've installed the uBlock extension for your browser from https://ublockorigin.com/, you'll see the Icon in the add-on area of your browser (it's a red shield with ub written on it).
 
You can either import the blocklist in this repo, and/or manually add filters to uBlock.

## Method 1 - Auto-filter using this curated blocklist

1. Open the uBlock dashboard and navigate to the "Filter Lists" tab
2. At the bottom, you'll see an option to import custom lists. Check that box
3. Add this url to that box: 
https://raw.githubusercontent.com/xenlock/investing.com-ublock-filter/main/blocklist.txt
4. Click on the "Apply Changes" button at the top
5. The list should be kept updated automatically


## Method 2 - Manually filtering


>This method is useful if you want to block certain users or any posts with certain text in them


1. Open Investing.com (refresh the page if you're already on it)
2. Open the uBlock dashboard (click on the red ub icon and then click on the gear icon)
3. Navigate to the "My Filters" tab
4. Paste the following filters:
 

    ```
    www.investing.com##div.discussion_discussion-wrapper__2TUX4:has-text(/face.*book/i)

    www.investing.com##div.discussion_discussion-wrapper__2TUX4:has-text(/🆃🅴🅻🅴🅶🆁🅼/i)
    
    www.investing.com##div.discussion_discussion-wrapper__2TUX4:has-text(/UserName/i)
    ```
    
    >⚠️ You can replace the UserName with any user you want to block and you'll never see their posts!


5. The text between // is a regular expression, so you can be very precise when blocking spam. the /i at the end is to make the expression case insensitive
6. Just one text filter of `/face.*book/i` blocks almost 95% of the spam in the forum!
7. You can block entire posts (and their replies) containing any keyword that you want to block. Just add them one line at a time with that keyword like so: `/YourKeyword/i`
8. Click on the "Apply Changes" button at the top and you're good to go

&nbsp;

Thanks for all the helpful posts y'all!
