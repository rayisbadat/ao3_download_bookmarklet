# ao3_download_bookmarklet
A stub of javascript you can save as a bookmarklet and download ao3 storeis as epub with 1 click

* Create a new bookmark (Putting it in the Bookmark toolbar makes most sense)
* give it any `Name` you want.
* For the URL copy/paste in this JS snippet ::
  ```
  javascript: (() => {
    var download = document.getElementsByClassName('download');
    var dlBase = 'https://download.archiveofourown.org';
    var uriPath = download[0]['children'][1]['children'][1]['firstChild']['attributes'][0]['nodeValue'];
    location.href = dlBase + uriPath;
  })();
  ```
* You cant auto close the tab, since that functionality only exists if the script created the tab.
