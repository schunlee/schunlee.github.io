---
title: google_spreadsheet_tips
date: 2018-11-01 17:19:19
tags:
---

### Tips
* when export BigQuery SQL result to Google Spreadsheet (adunit hyperlink as one field in it), find all hyperlinks don't work on newly auto created Spreadsheet, cannot click and redirect, an apostrophe ahead of every hyperlink text. With function REGEXREPLACE to replace the head apostrophe, and paste the value, the hyperlink still not work.

    <a href="https://i.imgur.com/4lREnao.png)"><img src="https://i.imgur.com/4lREnao.png)"/></a>

* fortunately, with Spreadsheet API to rewrite the spreadsheet can solve above bug. So here use Google Apps Script to refresh the data.(seeing spreadsheet_tool.gs)
  * Menu -> Tools -> Script editor -> paste spreadsheet_tool.gs -> Save -> Run the Script -> Authorize via browser
  * then you will see Menu -> Custom Tools -> Refresh Current Sheet, choose to click

    <a href="https://i.imgur.com/OgUrfTe.png)"><img src="https://i.imgur.com/OgUrfTe.png)"/></a>

    <a href="https://i.imgur.com/1ZMc6Ph.png)"><img src="https://i.imgur.com/1ZMc6Ph.png)"/></a>

    <a href="https://i.imgur.com/4lREnao.png)"><img src="https://i.imgur.com/4lREnao.png)"/></a>

    <a href="https://i.imgur.com/lUdRQmR.png)"><img src="https://i.imgur.com/lUdRQmR.png)"/></a>

  <script src="https://gist.github.com/schunlee/7fbff5eddbd4464614f0d9c0fd92ad70.js"></script>
