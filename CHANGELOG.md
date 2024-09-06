# Changelog

## [v1.2.8](https://github.com/hibbitts-design/docsify-open-course-starter-kit/releases/tag/v1.2.8)
### 08/31/2023

**Improved:**   
* ReadMe updated

## [v1.2.7](https://github.com/hibbitts-design/docsify-open-course-starter-kit/releases/tag/v1.2.7)
### 08/25/2023

**Improved:**   
* Updated example custom CSS for LMSs
* Cleanup default CSS
* Adjusted badge colours for dark theme
* Use light/dark theme display for topic indexes
* Clarify light + dark theme use comments
* ReadMe updated

## [v1.2.6](https://github.com/hibbitts-design/docsify-open-course-starter-kit/releases/tag/v1.2.6)
### 08/15/2023

**New:**   
*  Support for nav pill (`navpill`) Markdown CSS class

**Improved:**   
* Added 'youtube-nocookie.com' to domains made responsive through the automatic addition of the CSS Markdown class `video-container-16by9`

**Improved:**   
* ReadMe updated

## [v1.2.5](https://github.com/hibbitts-design/docsify-open-course-starter-kit/releases/tag/v1.2.5)
### 06/27/2023

**Improved:**   
* Match Docsify-This Markdown file rendering with Docsify Starter Kits CSS (incl. faded header image ToC adjustments and automatic responsive iFrames for YouTube and Google Docs embeds)

## [v1.2.4](https://github.com/hibbitts-design/docsify-open-course-starter-kit/releases/tag/v1.2.4)
### 05/08/2023

**Improved:**   
* Refined responsize header line heights

## [v1.2.3](https://github.com/hibbitts-design/docsify-open-course-starter-kit/releases/tag/v1.2.3)
### 04/09/2023

**Improved:**   
* Set font of buttons to sans-serif
* Set font of badges to sans-serif
* Remove unneeded GitHub image file path adjustments
* Refined responsize header font size and line heights

## [v1.2.2](https://github.com/hibbitts-design/docsify-open-course-starter-kit/releases/tag/v1.2.2)
### 03/13/2023

**Improved:**   
* Restore initial header spacing except for alerts and blockquotes
* Remove extra space between Sidebar icons and labels
* ReadMe updated

## [v1.2.1](https://github.com/hibbitts-design/docsify-open-course-starter-kit/releases/tag/v1.2.1)
### 02/13/2023

**New:**
* Support for images with border and rounded border (`image-border`,`image-border-rounded`)
* Support for 75%, 50% and 25% scaled images with border (`image-75-border`,`image-50-border` and `image-25-border`)

**Improved:**   
* Consolidate and simplify example custom CSS for LMSs
* Additional support and improvements for optional dark mode
* Match Docsify-This CSS with Docsify Starter Kits CSS

## [v1.2.0](https://github.com/hibbitts-design/docsify-open-course-starter-kit/releases/tag/v1.2.0)
### 01/02/2023

**New:**
* Support for 75%, 50% and 25% scaled images (`image-75`,`image-50` and `image-25`)
* Additional languages for Prismjs (Bash, Go, Java, Kotlin, PHP, Python and Swift in addition to the base set https://docsify.js.org/#/language-highlight?id=language-highlighting)

**Improved:**
* Adjust page margins when content is being embedded
* Adjust margins and padding for alerts and blockquotes
* Increase clickable areas for Topics alphabetical index
* ReadMe updated

## [v1.1.4](https://github.com/hibbitts-design/docsify-open-course-starter-kit/releases/tag/v1.1.4)
### 01/17/2023

**New:**
* Support for optionaly showing the navbar when embedded/standalone (now fully supported with v1.1.2 release)
* Support for displaying a footer ('_footer.md' file) via 'footer' setting in index.html or using the URL parameter 'footer=true'

**Improved:**
* Adjusted opacity of 'header-image-fade' class for improved accessibility

**Bugfix:**   
* Pass 'navbar' URL parameter for page-to-page navigation links

## [v1.1.3](https://github.com/hibbitts-design/docsify-open-course-starter-kit/releases/tag/v1.1.3)
### 12/15/2022

**New**
* Support for background gradient header image (`header-image-fade`, with thanks to Jamie Adam for original CSS)
* Support for full-width header image (`header-image-full-width`, optional Table of Contents not available)

**Improved:**
* ReadMe updated

## [v1.1.2](https://github.com/hibbitts-design/docsify-open-course-starter-kit/releases/tag/v1.1.2)
### 11/23/2022

**Improved:**
* Aligned ToC CSS with Docsify-This.net
* Support for scrolling of Table of Contents
* ReadMe updated
* Removed deprecated emoji plugin (as of Docsify v4.13)
* Support for page-to-page navigation when embedded/standalone
* Changed support for light/dark Themeable theme switching to optional

## [v1.1.1](https://github.com/hibbitts-design/docsify-open-course-starter-kit/releases/tag/v1.1.1)
### 09/02/2022

**Improved:**  
* Reduced page margins when displayed as embedded or standalone
* Adjusted font size and line height for Topics index items
* Added example CSS colours to be the same as Sakai LMS
* Streamlined settings for custom CSS colours
* Simplified 'ToC' setting in index.html
* Reduced left margin of page Table of Contents on smaller screens
* Updated Table of Contents plugin items
* Added Editor.css file for better Markdown previews
* Added new Themeable support for light/dark theme switching (OS-level)
* Adjusted link colours for dark theme

**Bugfix:**   
* Removed unused JS and CSS resources
* Fixed incorrect links in example course content
* Added missing Sidebar name and link colour settings
* Support the removal of the '_sidebar.md' file with standalone setting
* Fixed embedded code blocks overflow issues

## [v1.1.0](https://github.com/hibbitts-design/docsify-open-course-starter-kit/releases/tag/v1.1.0)
### 05/30/2022

**Improved:**  
* Aligned default link colour to be the same as Canvas LMS
* Added example link colours to be the same as Moodle LMS
* Adjusted left Markdown section padding
* Adjusted margins for site name in Sidebar
* Added 'standalone' setting in index.html to permanently alter the display of all pages (i.e. hidden Sidebar and Navbar)

**Bugfix:**   
* Fixed 'hidegitlink' URL parameter detection

## [v1.0.8](https://github.com/hibbitts-design/docsify-open-course-starter-kit/releases/tag/v1.0.8)
### 03/21/2022

**Improved:**  
* Adjusted link colours for improved contrast

## [v1.0.7](https://github.com/hibbitts-design/docsify-open-course-starter-kit/releases/tag/v1.0.7)
### 02/15/2022

**New:**  
* Added conditional display of page table of contents (`?toc=true`)

**Improved:**  
* Restored user zoom ability for improved accessibility
* Revised alt image text for improved accessibility
* Revised JS function `getURLParameterByName` to accept multiple terms (i.e. to support aliases) and also include functionality of previous returnByURLParameterByName function

**Bugfix:**
* Fixed incorrect H3 headers

## [v1.0.6](https://github.com/hibbitts-design/docsify-open-course-starter-kit/releases/tag/v1.0.6)
### 11/15/2021

**Improved:**  
* Adjusted header line heights for improved readability
* Added initial support for responsive font sizing (480px only)
* Improved badge alignment
* Improved text label spacing for buttons
* Removed unneeded embedded check for Pagination Plugin
* Adjusted right margin of navbar to improve alignment
* Removed background colour from accordions to better support a dark theme

**Bugfix:**   
* Added an additional new line before Edit this Page on GitHub links to ensure proper formatting break

## [v1.0.5](https://github.com/hibbitts-design/docsify-open-course-starter-kit/releases/tag/v1.0.5)
### 10/15/2021

**Improved:**  
* Relocated images to be within top-level docs folder

## [v1.0.4](https://github.com/hibbitts-design/docsify-open-course-starter-kit/releases/tag/v1.0.4)
### 10/05/2021

**Improved:**
* Added 'Use this Template on GitHub' button on Sidebar
* Changed name of Sidebar page
* Revised Sidebar project links
* Updated example image descriptions
* Adjusted tall banner images for use in multi-course setups

## [v1.0.3](https://github.com/hibbitts-design/docsify-open-course-starter-kit/releases/tag/v1.0.3)
### 08/03/2021

**Improved:**
* Added variable for text of Edit this Page on GitHub links to make modifications easier
* Changed JS function name from `getParameterByName` to `getURLParameterByName` for improved clarity
* Added the new JS function `returnByURLParameterByName` to return one of two values based on URL parameter (e.g. choose external link behaviour based on embedded status)

## [v1.0.2](https://github.com/hibbitts-design/docsify-open-course-starter-kit/releases/tag/v1.0.2)
### 06/16/2021

**Improved:**
* Adjusted custom list bullet presentation

## [v1.0.1](https://github.com/hibbitts-design/docsify-open-course-starter-kit/releases/tag/v1.0.1)
### 05/30/2021

**Improved:**
* Changed variable name `yourRepoURL` to `gitLinkRepoURL` for improved clarity

## [v1.0.0](https://github.com/hibbitts-design/docsify-open-course-starter-kit/releases/tag/v1.0.0)
### 05/18/2021

**Improved:**
* ReadMe and screenshot updates
* Changed conditional loading of Pagination script to asynchronous
* Adjusted breakpoint for two column display
* Decreased padding between items in navbar

**Bugfix:**  
* Fixed URL to project ReadMe file

## [v1.0.0-preview.2](https://github.com/hibbitts-design/docsify-open-course-starter-kit/releases/tag/v1.0.0-preview.2)
### 05/10/2021

**Improved:**
* Moved example Canvas LMS visual style adjustments from index.html to custom.css file
* Adjusted CSS of Headers for improved line wrapping
* Adjusted root base line height to increase lines in Sidebar
* Renamed 'responsive-wrap' class to 'responsive-container' for improved consistency
* Changed default external target link to '_top'
* Updated example styling for matching Docsify pages within Canvas LMS
* Increased padding below custom navbar to support more menu items
* Adjusted header sizes and margins
* List and button style updates
* Updated GitHub repo URL config and documentation
* Relocated embedly script to index.html file

**Bugfix:**  
* Fixed label colour for linked badges
* Consistent hover behaviour for linked badges and buttons

## [v1.0.0-preview.1](https://github.com/hibbitts-design/docsify-open-course-starter-kit/releases/tag/v1.0.0-preview.1)
### 05/04/2021

**New:**  
* Welcome to the preview release of Docsify Open Course Starter Kit!
