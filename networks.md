# --- General options --- #

# Name of website
title: Nguyen-Hoai Nam's site

# Short description of your site
description: All about technical and leisure life

# --- Local development options ---
# If your website is hosted locally rather than on GitHub, then you need to uncomment the next two parameters to set the url and baseurl
# *** If you're not sure what this mean, then leave this section as it is. Only modify the url and baseurl if you know what you're doing!***

# url is the the website domain URL without a trailing slash
#url: "https://example.com"

# baseurl should be an empty string
#baseurl: ""

# --- Navigation bar options --- #



# If you want to have an image logo in the top-left corner instead of the title text,
# then specify the following parameter
# title-img: /path/to/image

# --- Background colour/image options --- #

# Personalize the colors in your website. Colour values can be any valid CSS colour


# Select your active Social Network Links.
# Uncomment the links you want to show in the footer and add your information to each link.
# You can reorder the items to define the link order.
# If you want to add a new link that isn't here, you'll need to also edit the file _data/SocialNetworks.yml

#  snapchat: deanat78
#  instagram: deanat78
#  youtube: user/deanat78
#  spotify: yourname
#  telephone: +14159998888
#  steam: deanat78
#  twitch: yourname
#  yelp: yourname


# How to display the link to the website in the footer
# Remove this if you don't want a link in the footer
#url-pretty: "MyWebsite.com"  # eg. "deanattali.com/beautiful-jekyll"

# --- Web Statistics Section --- #


# Matomo (aka Piwik) Web statistics
# Uncomment the following section to enable Matomo. The opt-out parameter controls
# whether or not you want to allow users to opt out of tracking.

#matomo:
#  site_id: "9"
#  uri: "demo.wiki.pro"
#  opt-out: true

# --- Comments --- #

# Fill in your Disqus shortname (NOT the userid) if you want to support Disqus comments
# disqus: ""



# Character used to separate site title and description in HTML document title
# and RSS feed title



# prose.io config
prose:
  rooturl: '_posts'
  media: 'img'
  ignore:
    - 404.html
    - LICENSE
    - feed.xml
    - _config.yml
    - /_layouts
    - /_includes
    - /css
    - /img
    - /js
  metadata:
    _posts:
      - name: "layout"
        field:
          element: "hidden"
          value: "post"
      - name: "title"
        field:
          element: "text"
          label: "Post title"
          placeholder: "Title"
          alterable: true
      - name: "subtitle"
        field:
          element: "textarea"
          label: "Subtitle"
          placeholder: "A description of your post."
          alterable: true
      - name: "date"
        field:
          element: "text"
          label: "Date"
          help: "Enter date of post."
          placeholder: "yyyy-mm-dd"
          alterable: true
      - name: "image"
        field:
          element: "text"
          label: "Image"
          help: "Add a thumbnail image to your post."
          placeholder: "Thumbnail"
          alterable: true
      - name: "published"
        field:
          element: "checkbox"
          label: "Publish"
          help: "Check to publish post, uncheck to hide."



# Beautiful Jekyll / Dean Attali
# 2fc73a3a967e97599c9763d05e564189
