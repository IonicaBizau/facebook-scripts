# Facebook Scripts [![Support this project][donate-now]][paypal-donations]

A set of scripts to make your Facebook experience smoother.

## Friends that liked a photo

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

## How to contribute
Have an idea? Found a bug? See [how to contribute][contributing].

## License

[MIT][license] © [Ionică Bizău][website]

[paypal-donations]: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=RVXDDLKKLQRJW
[donate-now]: http://i.imgur.com/6cMbHOC.png

[license]: http://showalicense.com/?fullname=Ionic%C4%83%20Biz%C4%83u%20%3Cbizauionica%40gmail.com%3E%20(http%3A%2F%2Fionicabizau.net)&year=2014#license-mit
[website]: http://ionicabizau.net
[contributing]: /CONTRIBUTING.md
[docs]: /DOCUMENTATION.md