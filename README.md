Facebook Scripts
================

Useful Facebook scripts

# Friends that liked a photo

 1. Open the photo.
 2. Open the popup with the people that liked the photo.
 3. If needed, click `More` button to load all the users.
 4. Then open the browser developer tools where you will run the following script:

```js
ul = document.getElementsByTagName("ul")
ul = ul[ul.length - 1]
a = ul.querySelectorAll("li a[data-hovercard]") 
f = [];
for (var i = 0; i < a.length; ++i) {
  if (!a[i].innerText) continue; f.push(a[i].innerText);
}
```

After running the script above, `f` will be an array with the names of the users that liked the opened photo.
