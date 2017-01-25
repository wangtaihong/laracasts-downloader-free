# Laracasts Downloader Free (Without Login)


## Requirements
- PHP >= 5.4
- php-cURL
- php-xml
- Composer

## Installation
- Clone this repo to a folder in your machine
- `composer install`
- `php start.php`and you are done!

Also works in the browser, but is better from the cli because of the instant feedback


## Downloading specific series or lessons
- You can use series and lessons names
- You can use series and lessons slugs (preferred because there are some custom slugs too)
- You can download multiples series/lessons

### Commands to download series
    php start.php -s "What's New in Laravel 5.4" -s "whats-new-in-laravel-5-4"

Then Open the file in series folder'download.html', Download them with your browser
Recommended Use Firefox with DownThemAll

![Screen1](https://ww3.sinaimg.cn/large/006tNc79gy1fc2x2h8gvvj30tj0f20vl.jpg)
![Screen2](https://ww2.sinaimg.cn/large/006tNc79gy1fc2x7oooszj30uv0id43j.jpg)

### Command to download lessons
    php start.php -l "Lesson name example" -l "lesson-slug-example"
    php start.php --lesson-name "Lessons name example" --lesson-name "lesson-slug-example"

## Troubleshooting
If you have a `cURL error 60: SSL certificate problem: self signed certificate in certificate chain` do this:

- Download [http://curl.haxx.se/ca/cacert.pem](http://curl.haxx.se/ca/cacert.pem)
- Add `curl.cainfo = "PATH_TO/cacert.pem"` to your php.ini

And you are done! If using apache you may need to restart it.

## License

This library is under the MIT License, see the complete license [here](LICENSE)
