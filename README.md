# Week7WebSecurityWP
Using word press 4.2 for these vulnerabilites.
# Project 7 - WordPress Pentesting

Time spent: **6** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) Unauthenticated XXS Cross-Site Scripting
  - [ ] Summary:XXS Comment vulnerabilites that affects the site on the move of the mouse after code has been submitted. 
    - Vulnerability types:XXS
    - Tested in version:WordPress 4.2
    - Fixed in version:4.2.1
  - [ ] GIF Walkthrough: ![alt text](https://github.com/EchoX18/Week7WebSecurityWP/blob/master/XSS2.gif)
  ![alt text](https://github.com/EchoX18/Week7WebSecurityWP/blob/master/XSS3.gif)
     - [Link 1](https://wpvulndb.com/vulnerabilities/7945)
 
                         
  - [ ] Steps to recreate:
  1.Attacker must fix access the site then add a long code(comment) 
  2.Once the comment has been submitted the site will display the vulnerability including the message (DOOMED PLANET)
  - [ ] Affected source code:Listing of changes. This inlcuding changing the script.
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Required) Authenticated Stored Cross-Site Scripting
  - [ ] Summary: Inserting a Youtube embed code that allows for cross site scripting to occur when posted or when authenticated user previews the post.
    - Vulnerability types: XXS
    - Tested in version: 4.2
    - Fixed in version: 4.2.1
  - [ ] GIF Walkthrough:  ![alt text](https://github.com/EchoX18/Week7WebSecurityWP/blob/master/XXS%20Number%202.gif)
  - [ ] Steps to recreate: 
  1.Log into Word Press as an Admin or as a authorized user.
  2.Retrieve the youtube embedded code that you can customize to your liking.
  3.Insert code into a posting page.
  4.Click on preview 
  5.Script should appear with digits one or zero.
  - [ ] Affected source code: 
    - [Link 1](https://wpvulndb.com/vulnerabilities/8768)
1. (Required) Authenticated Stored Cross-Site Scripting Via Image File Name 
  - [ ] Summary: This vulnerability is done by placing a executing scripting into the name of an image, once submitted and page is preview the script will execute showing the (document.cookie). This can potentially lead to greater risks if the script is manipulated to reveal other items of interest.
    - Vulnerability types:XXS Cross Site Scripting
    - Tested in version:4.6 
    - Fixed in version:4.6.1
  - [ ] GIF Walkthrough:
  ![alt text](https://github.com/EchoX18/Week7WebSecurityWP/blob/master/XXS%20Image%202.gif)
  ![alt text](https://github.com/EchoX18/Week7WebSecurityWP/blob/master/XXS%20Image%202-2.gif)
  
  - [ ] Steps to recreate:
  1. A script must be made in order to rename the image. In this case I used a img src script.
  2. Secondly, you must have an image or save an image from a website or stored device.
  3. Next, you must rename the image to the script that has been made(this is what will be executed when uploaded)
  4. You upload to the word press and preview the page.
  5. Bravo! The Script has been executed.
  - [ ] Affected source code:
    - [Link 1](https://wpvulndb.com/vulnerabilities/8615)
1. (Optional) Large File Error XXS
  - [ ] Summary: This XXS is made by creating a fake file that is at least 20 MB. Once file is made, user must rename the file to a XXS script in png. using img src. Once done the user will upload the file and the script will be executed through as a error. 
    - Vulnerability types: XXS Cross Site Scripting
    - Tested in version:4.7.2
    - Fixed in version: 4.7.5
  - [ ] GIF Walkthrough: 
  ![alt text](https://github.com/EchoX18/Week7WebSecurityWP/blob/master/XXS%20MAX.gif)
  ![alt text](https://github.com/EchoX18/Week7WebSecurityWP/blob/master/XXS%20MAX%202.gif)
  - [ ] Steps to recreate:
  1. The user must create a fake file of at least 20 MB and rename it with the script (doomedplanet<img src=x onerror=alert(1)>.png)
  2. The user must upload to Wordpress as a media file.
  3.Once the user uploads an error will occur showing max file size.
  4.Bravo! You have done it!
  - [ ] Affected source code:
    - [Link 1](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-9061) 


## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

One main challenge that I got from switching from version to version is that Wordpress started to force me to update to their new version of the program. I still havent gotten a fix for this. This stopped me from moving foward. I used Kali Linux for the last two as you can't rename it as I did in windows.

## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
