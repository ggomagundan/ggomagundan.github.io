---
layout: post
title: Md-Date-Time-Picker-Rails
desc: Migration md-date-time-picker to rails Gem
proj-url: https://github.com/ggomagundan/md-date-time-picker-rails
proj-num: 01
---




[![Gem
Version](https://badge.fury.io/rb/md-date-time-picker-rails.svg)](https://badge.fury.io/rb/md-date-time-picker-rails)

md-date-time-picker-rails gem is the integration of md-date-time-picker javascript
library(using 2.2 Version) for your Rails 4, 5 application.

md-date-time-picker is Material Design - Date and Time Picker
source: https://github.com/PuranjayJain/md-date-time-picker

Ruby gems url: https://rubygems.org/gems/md-date-time-picker-rails


## Installation

Add this line to your application's Gemfile:

```ruby
gem 'md-date-time-picker-rails'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install md-date-time-picker-rails

Now you need to edit your `app/assets/javascripts/application.js` file
and add the following line:

``` javascript
//= require moment.min
//= require moment.locales# if using another locale 
//= require draggabilly.pkgd.min # If using TimeDialog
//= require mdDateTimePicker
```

And you need to edit your `app/assets/stylesheets/application.css` file
and add the following line:

```css
*= require mdDateTimePicker
```

If Use `app/assets/stylesheets/application.scss` file
```scss
@import "mdDateTimePicker";
```

## Theme

mdDateTimePicker provided prebuilt
[themes](http://puranjayjain.github.io/md-date-time-picker/)

This Gem progressively support all Themes

If you apply theme, you need to edit your `app/assets/stylesheets/application.scss` or `app/assets/stylesheets/application.scss` file
and change the following line:


```css
# app/assets/stylesheets/application.css
*= require themes/dark/amber/mdDateTimePicker
```

```scss
# app/assets/stylesheets/application.scss
@import "themes/dark/amber/mdDateTimePicker";
```

Currently,  Support Theme List

- `themes/dark/amber`, `themes/dark/blue`, `themes/dark/blue-grey`, `themes/dark/cyan`, `themes/dark/deep-orange`, `themes/dark/deep-purple`, `themes/dark/green`, `themes/dark/grey`,`themes/dark/indigo`, `themes/dark/light-blue`, `themes/dark/light-green`, `themes/dark/lime`, `themes/dark/orange`, `themes/dark/pink`, `themes/dark/purple`, `themes/dark/red`, `themes/dark/teal`, `themes/dark/yellow`
- `themes/light/amber`, `themes/light/blue`, `themes/light/blue-grey`, `themes/light/cyan`, `themes/light/deep-orange`, `themes/light/deep-purple`, `themes/light/green`, `themes/light/grey`,`themes/light/indigo`, `themes/light/light-blue`, `themes/light/light-green`, `themes/light/lime`, `themes/light/orange`, `themes/light/pink`, `themes/light/purple`, `themes/light/red`, `themes/light/teal`, `themes/light/yellow`






## Usage

Here is the example working code to test with your Rails application.

Add this sample code to your `app/assets/javascripts/application.js`
file

``` javascript
$(document).ready(function(){

 toggleButton = document.getElementById("OBJECT_ID");
 dialog = new mdDateTimePicker["default"]({
   type: 'date',
   type: 'time',                      # If you wanna TIME
   future: moment().add(1, 'years'),  # Optional
   trigger: toggleButton              # Optional
 });
 toggleButton.addEventListener("click", function() {
    return dialog.toggle();
  });
  toggleButton.addEventListener("onOk", function(e) {
    return this.value = dialog.time().format('L');
  });

});
```

If use `app/assets/javascript/application.coffee`

``` coffee

  toggleButton = document.getElementById("OBJECT_ID")
  dialog = new mdDateTimePicker.default(
    type: 'date',
    future: moment().add(1, 'years'),
    trigger: toggleButton
  )

  toggleButton.addEventListener "click", ->
    dialog.toggle()
  toggleButton.addEventListener "onOk", (e) ->
    this.value = dialog.time.format('L')

```



## Full documentation 

The Documentation is at
https://puranjayjain.github.io/md-date-time-picker

## Change Log

Current Version 2.1.2

This link listing [Change Log](https://github.com/ggomagundan/md-date-time-picker-rails/blob/master/CHANGE_LOG.md)


## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Added some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request


## License

The gem is available as open source under the terms of the [MIT
License](http://opensource.org/licenses/MIT).



