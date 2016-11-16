---
layout: post
title: Clipboard-Toastr-Rails
desc: clipboard.js and toastr javascript Gem
proj-url: https://github.com/ggomagundan/clipboard-toastr-rails
proj-num: 01
---



[![Gem
Version](https://badge.fury.io/rb/clipboard-toastr-rails.svg)](https://badge.fury.io/rb/clipboard-toastr-rails)
[![Build
Status](https://travis-ci.org/ggomagundan/clipboard-toastr-rails.svg?branch=master)](https://travis-ci.org/ggomagundan/clipboard-toastr-rails)

clipboard-toastr-rails gem is the integration of clipboard.js and toastr javascript
library(using 2.2 Version) for your Rails 4, 5 application.

Ruby gems url: https://rubygems.org/gems/clipboard-toastr-rails


## Installation

Add this line to your application's Gemfile:

```ruby
gem 'clipboard-toastr-rails'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install clipboard-toastr-rails

Now you need to edit your `app/assets/javascripts/application.js` file
and add the following line:
``` javascript
//= require clipboard-toastr
```

And you need to edit your `app/assets/stylesheets/application.css` file
and add the following line:

```css
*= require toastr
```

If Use `app/assets/stylesheets/application.scss` file
```scss
@import "toastr";
```







## Usage

Here is the example working code to test with your Rails application.

Add this sample code to your `app/assets/javascripts/application.js`
file

``` javascript
$(document).ready(function(){

  clip = new Clipboard('.copy-target')

  toastr.options = {
    "positionClass": "toast-bottom-center",
    ....
    ....
  }

  $(".copy-target").click ->
    toastr.info "Copy Success Alert"


});
```

```html

<html>
  <head>
  ...
  </head>

  <body>
    ...
    ...

    <span class="copy-target" data-clipboard-text="COPY CONTENT">Copy Link</span>

    ...
    ...
  </body>

</html>

```




## Full documentation 

The Documentation is at
[Clipboard.js Document](https://clipboardjs.com/)
[Toastr Document](http://codeseven.github.io/toastr/)

## Change Log

Current Version 1.0.0

This link listing [Change Log](https://github.com/ggomagundan/clipboard-toastr-rails/blob/master/CHANGE_LOG.md)


## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Added some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request


## License

The gem is available as open source under the terms of the [MIT
License](http://opensource.org/licenses/MIT).




