# Gmail Print Multiple Messages Workaround
Here's a method to print multiple emails at one time. It's not a direct method, but a decent workaround.


1. Select the multiple emails you wish to print. 
2. At the top, the three dots "Forward As Attachment" to yourself.
3. Click to print the forwarded email, which will open in a new window, but then close the print dialog box.
4. Open Google DevTools, and on the "Console" tab, at the bottom, enter the following Javascript and click enter:

document.body.innerHTML = document.body.innerHTML.replace(new RegExp('---------- Forwarded message ----------', 'g'), '&lt;div style="clear:both;page-break-before:always;"&gt;&lt;/div&gt;---------- Forwarded message ----------');

5. Now you can print. This simple script will add page breaks above each message allowing you to print the individual pages. Some emails may be multi page, so you can custom select the pages you need and omit the extras if they exist. 

__NOTE: This method is limited to 10 emails, above that gets truncated by the system.__

Hope This helps someone :)
