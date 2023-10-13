# css-accessibility-check
Version: 0.1 – 13th of October 2023

Add the css-file to your websites for live accessibility check by adding the following line to your websites <head> section:

<link rel="stylesheet" href="https://raw.githubusercontent.com/absichtbar/css-accessibility-check/main/css-accessibility-check.css">

# What css-accessibility-check will do: 
This css will show you some accessibility errors directly in your page. And it will show them to your users as well, if you use it in production. 

So take care you first use it locally to reduce accessibility issues before you can go ahead and use it in production. Ideally it would not find anything than. 

# So why should you use css-accessibility-check?
This CSS would help you to ensure you find certain accessibility issues on your sites you might miss to avoid. 

# Wich accessibility issues does css-accessibility-check show?
Well, I need to start somewhere, so I decided to start with the most common accessibility failures! 
https://webaim.org/projects/million/ lists the top 6 issues that 96.3% of the  websites tested in 2023 show:
1. low contrast text: 83.6% 
2. Missing alternative text for images: 58.2%
3. Empty links: 50.1%
4. Missing form input labels: 45.9% 
5. Empty buttons: 27.5%
6. Missing document language: 18.6% 

css-accessibility-check can detect the following of this failures:

## 2. Missing alternative text for images
css-accessibility-check looks for:
• img that do not have an alt tag at all and marks them using a red overlay and 3px red border

It does not check if an alt tag is available but empty, because this may be set to mark the image decorative. 

# Wich accessibility issues will it show later?
## 3. Empty links
css-accessibility-check looks for 
• empty <a></a> tags that do not have a title, aria-label or aria-labelled-by attribute and marks them with a 3px red border

## 4. Missing form input labels
css-accessibility-check looks for 
• forms that have <input> that is not type="button" or type="hidden" but dos not have <label> 

## 5. Empty buttons

## 6. Missing document language

And hopefully more soon! 

# Wich accessibility issues will not be added?
## 1. low contrast text
this needs JavaScript to be detected. 