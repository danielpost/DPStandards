# DPStandards

Daniel Post WordPress Coding Standards - Largely based on standard WordPress coding standards with a few additions and exceptions.

### What is this?

In my opinion, every developer should follow a coding standard (if you're wondering why, Scott Dorman explained it nicely [10 years ago](https://scottdorman.github.io/2007/06/29/Why-Coding-Standards-Are-Important/)). Since I work almost exclusively with WordPress, following the official [WordPress Coding Standards](https://make.wordpress.org/core/handbook/best-practices/coding-standards/php/) makes the most sense for me. However, there's a few things in their coding standard that I'm not a fan of, which is why I've made a few changes:

 - **Spaces around function calls, if statements etc**

 When it comes to spaces, I much prefer [PSR-2's](http://www.php-fig.org/psr/psr-2/) approach.

 - **Don't force Yoda conditions**

 I know it's best practice, but personally I find them unnecessary and harder to read.

 - **Allow usage of a constant as text domain**

 Personally I like to define a constant to use as a text domain instead of repeating it every time (`define('PREFIX_THEME_SLUG', get_template());`, `__('Some text', PREFIX_THEME_SLUG)`). There's some discussion about whether or not you should do this (further reading [here](https://markjaquith.wordpress.com/2011/10/06/translating-wordpress-plugins-and-themes-dont-get-clever/), [here](http://ottopress.com/2012/internationalization-youre-probably-doing-it-wrong/) and [here](https://ulrich.pogson.ch/string-text-domain-must)), so make sure you're aware of the risks. So far I haven't encountered any issues personally.

 - **Spaces instead of tabs**

 Personal preference, that's all.

### How to use
Install PHPCS, install WPCS, declare custom ruleset.xml. The [WPCS repository](https://github.com/WordPress-Coding-Standards/WordPress-Coding-Standards#installation) has a nice explanation of how to install everything. I also use the SublimeLinter and SublimeLinter-phpcs extensions to automatically check my code in Sublime Text.

### Contributing
This is still a work in progress, so if you have any suggestions or improvements please feel free to submit a PR.
