Facebook Scripts
================

Useful Facebook scripts

# Friends that liked a photo

 1. Open the photo.
 2. Open the popup with the people that liked the photo.
 3. If needed, click `More` button to load all the users.
 4. Then open the browser developer tools where you will run the following script, after including jQuery on page (just paste and run [this code](http://code.jquery.com/jquery-1.11.1.min.js)):

```js
$all = $("div:contains('People Who Like This') ul > li")
f = [];
for (var i = 0; i < $all.length; ++i) {
  f.push($("a[data-gt]", $all[i]).text())
}
```

After running the script above, `f` will be an array with the names of the users that liked the opened photo.
