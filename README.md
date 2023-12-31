# css-accessibility-check
Version: 0.4 – 25th of October 2023

Add the css-file to your websites for live accessibility check by adding the following line to your websites <head> section AFTER your other stylesheets:

&lt;link rel="stylesheet" href="https://raw.githubusercontent.com/absichtbar/css-accessibility-check/main/css-accessibility-check.css"&gt;

# What css-accessibility-check will do: 
This css will show you some accessibility errors directly in your page. And it will show them to your users as well, if you use it in production. 

So take care you first use it locally to reduce accessibility issues before you can go ahead and use it in production. Ideally it would not find anything than. 

# So why should you use css-accessibility-check?
This CSS would help you to ensure you find certain accessibility issues on your sites you might miss to avoid. 

# How did you choose wich accessibility issues css-accessibility-check should show?
Well, I need to start somewhere, so I decided to start with the most common accessibility failures! 
https://webaim.org/projects/million/ lists the top 6 issues that 96.3% of the  websites tested in 2023 show:
1. low contrast text: 83.6% 
2. Missing alternative text for images: 58.2%
3. Empty links: 50.1%
4. Missing form input labels: 45.9% 
5. Empty buttons: 27.5%
6. Missing document language: 18.6% 

# Wich accessibility issues does css-accessibility-check show?
css-accessibility-check can detect the following of this failures:

## 2. Missing alternative text for images
css-accessibility-check looks for:
1. img that do not have an alt tag or title tag at all and are not set to role="presentation"
2. img that do have an alt tag but it contains only one string without space 
3. img that do have an alt tag but it contains the file name (using .jpg, .svg, .png, .gif, .webp) 

and marks them using a red overlay and 3px red border

It does not check if an alt tag is available but empty, because this may be set to mark the image decorative. 

Lern more about the image issue: https://www.w3.org/WAI/tutorials/images/decorative/ 
Learn more about useful alt text: https://www.dbsv.org/bildbeschreibung-4-regeln.html (page is in german, please use translatoer if needed)

## 3. Empty links
css-accessibility-check looks for 
empty <a></a> tags that do not have a title, aria-label or aria-labelled-by attribute and marks them with a 3px red border

## 4. Missing form input labels
css-accessibility-check looks for 
forms that have <input> that is not type="button" or type="hidden" but does not have <label> or has empty <label>

It does not check if the form contains labels without for attribute (but contains inputfield inside the label) nor it does check if the for-attribute is connected to an id inside the form.

## 5. Empty buttons
css-accessibility-check looks for:
buttons that do not contain any text nor image and marks them red and removes icons or text that is rendered by generated content.

It does not work if a button contains an image or icon inserted between <button> and </button>. 

## 6. Missing document language
css-accessibility-check looks for 
empty or missing language tag for html. 

It does not check if the language tag is set correctly. 

++++++++++++++++++++++++++++++++++++++++++++++
# Wich accessibility issues will it show later?
None further planned for this file.

# Wich accessibility issues will not be added?
## 1. low contrast text
this needs JavaScript to be detected. 
