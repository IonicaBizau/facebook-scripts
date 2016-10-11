
# Facebook Scripts

 [![Patreon](https://img.shields.io/badge/Support%20me%20on-Patreon-%23e6461a.svg)][patreon] [![PayPal](https://img.shields.io/badge/%24-paypal-f39c12.svg)][paypal-donations] [![AMA](https://img.shields.io/badge/ask%20me-anything-1abc9c.svg)](https://github.com/IonicaBizau/ama) [![Version](https://img.shields.io/npm/v/facebook-scripts.svg)](https://www.npmjs.com/package/facebook-scripts) [![Downloads](https://img.shields.io/npm/dt/facebook-scripts.svg)](https://www.npmjs.com/package/facebook-scripts) [![Get help on Codementor](https://cdn.codementor.io/badges/get_help_github.svg)](https://www.codementor.io/johnnyb?utm_source=github&utm_medium=button&utm_term=johnnyb&utm_campaign=github)

> A set of scripts to make your Facebook experience smoother.

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


## :yum: How to contribute
Have an idea? Found a bug? See [how to contribute][contributing].


## :moneybag: Donations

Another way to support the development of my open-source modules is
to [set up a recurring donation, via Patreon][patreon]. :rocket:

[PayPal donations][paypal-donations] are appreciated too! Each dollar helps.

Thanks! :heart:


## :scroll: License

[MIT][license] © [Ionică Bizău][website]

[patreon]: https://www.patreon.com/ionicabizau
[paypal-donations]: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=RVXDDLKKLQRJW
[donate-now]: http://i.imgur.com/6cMbHOC.png

[license]: http://showalicense.com/?fullname=Ionic%C4%83%20Biz%C4%83u%20%3Cbizauionica%40gmail.com%3E%20(http%3A%2F%2Fionicabizau.net)&year=2014#license-mit
[website]: http://ionicabizau.net
[contributing]: /CONTRIBUTING.md
[docs]: /DOCUMENTATION.md
