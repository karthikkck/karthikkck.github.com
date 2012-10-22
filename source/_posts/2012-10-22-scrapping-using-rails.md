---
layout: post
title: "Scrapping using rails"
date: 2012-10-22 17:01
comments: true
categories:
---

Performing scrapping using rails is something new to me at this time. I had an experience with php where I had used simple_html_dom_parser library to get things going along with imacros.

With rails as stackoverlow and every blog, forum around says, I started with nokogiri. In the process I realized that I cannot click on any of the links using "onclick" event. As "onclick" is a javascript event and nokogiri does not support this.

Now my search starts for a gem which can support javascript scrapping. Finally I figured out that there is no as such a scrapping gem like nokogiri which supports js, but we can use front-end testing gems for this. Some gem which opens a browser window at the background does the events like clicks, login, etc. on a real instance of browser running at the background.

Finally I found the best one ( from what I read and experienced ) watir, headless. The following are the gems:

    gem 'watir-webdriver'
    gem 'headless'

## A summary of what these gems can do:

1. They can fill in the forms - fill input textbox, select options, etc.
2. They can login to a system with sessions and cookies like a real browser ( of course it is running on a real browser )
3. They can read the html of a page and we can store the html in a variable for further processing ( here is an issue )

Yes, we get the html but I found that watir is not that efficient in parsing the html. So I decided to use nokogiri gem for this.

Tips & code samples:

use "sleep 0.5" efficiently throughout your code. This is necessary because it takes some time to get the html of the page when you visit a website on a browser.

#### Wait until some html gets loaded:

    until browser.link(:class => 'login-button').exists? do
      sleep sleepTime
    end

If you are getting an alert window as soon as you visit a page, use this code:

    begin
      browser.goto('http://www.google.co.in')
    rescue Selenium::WebDriver::Error::UnhandledAlertError => e
      # just to ignore the alert popup in the page
    end


