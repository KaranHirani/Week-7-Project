# Project 7 - WordPress Pentesting

Time spent: **4** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) WordPress <= 4.2 - Unauthenticated Stored Cross-Site Scripting (XSS)
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version:  4.2.1
  - [ ] GIF Walkthrough: <img src="https://github.com/KaranHirani/Week-7-Project/blob/master/assignment7_1.gif?raw=true" alt="Girl in a jacket">
  - [ ] Steps to recreate: In a page with a post that has comments, insert the following text: <script>while(1){alert(document.cookie);}</script>.  The page will either refresh by itself or next time you refresh it, it will give you the pop up
  - [ ] Affected source code:
    - [Link 1](https://compsecurityconcepts.wordpress.com/tag/cross-site-scripting/)
2. (Required)WordPress <= 4.2.2 - Authenticated Stored Cross-Site Scripting (XSS)
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.3
  - [ ] GIF Walkthrough: <img src="https://github.com/KaranHirani/Week-7-Project/blob/master/assignment7_2.gif?raw=true" alt="Girl in a jacket">
  - [ ] Steps to recreate: Create a new post. Select the insert plain text option and insert the following code:  " <a href="</a><a title=" onmouseover=alert('test')  ">link</a> ""
Once you publish the page, it will show popups when you're on the page and try clicking the link for the post.
  - [ ] Affected source code:
    - [Link 1](https://github.com/WordPress/WordPress/blob/master/wp-includes/shortcodes.php)
3. (Required) WordPress <= 4.2.2 - Widgets Title Cross-Site Scripting (XSS)
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.4
  - [ ] GIF Walkthrough:  <img src="https://github.com/KaranHirani/Week-7-Project/blob/master/assignment7_3.gif?
  - [ ] Steps to recreate: Go to any page and click customize.  Select the widgets option and press add widget.  Go to the text widget and name your widget whatever and then enter the following code: <img src="https://google.com" onerror="alert('Widget Exploit!");">
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/trunk/src/wp-admin/customize.php)


## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Had issues setting up wordpress

## License

    Copyright [2017] [Karan Hirani]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
