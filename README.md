# Example Cumulocity IoT UI customization
This repository contains an example of how to extend the custom branding options in Cumulocity IoT. Custom branding can be applied to all enterprise tenants in the UI. However, since the UI does not allow you to change all CSS variables, there are options for adding CSS variables, which are shown below.

Table of Contents

1. [Introduction](#example-cumulocity-iot-ui-customization)
2. [Getting Started](#getting-started)
3. [Download Your Branding](#download-your-branding)
4. [Add Extra CSS URLs Option to the Options.json File](#add-extracssurl-option-the-the-optionsjson-file)
5. [Create a Branding.css File](#create-a-brandingcss-file)
6. [Add Cumulocity.json File and Zip the Directory](#add-cumulocityjson-file-and-zip-the-direcotry)
7. [Upload the Ui-Assets.zip via UI or c8ycli](#upload-the-ui-assetszip-via-ui-or-c8ycli)



## Getting started
Follow the steps outlined in the Cumulocity guide to create a custom branding for your enterprise tenant.
 [Here's a link to the cumulocity guide](https://cumulocity.com/guides/users-guide/enterprise-tenant/#branding). 

## Download your branding.
Once the branding has been applied to your tenant, you can find an application called "Public Options" under Administration -> Ecosystem Applications. Click on the application and download the linked zip file.

## Add extraCSSUrl Option the the options.json file
To add more CSS variables to the options.json file, simply include the following lines in the file:
```
"extraCssUrls": [
        "/apps/public/public-options/branding.css"
    ]
```

## Create a branding.css file
Create a branding.css file in the same directory and add the CSS variables you'd like to modify.

## Add cumulocity.json file and zip the direcotry
Include the cumulocity.json file from the repository, and then zip all of the files by executing the following command:
```
$zip ui-assets branding.css options.json cumulocity.json
```

## Upload the ui-assets.zip via UI or c8ycli
To replace the existing Public Options application in your tenant, upload the zip file through the user interface. To do this, click on "Add Application" in the header bar and select the zip file. Alternatively, you can also upload the zip file using c8ycli with the following command:
```
c8ycli deploy
```

______________________


For more information you can Ask a Question in the [TECHcommunity Forums](http://tech.forums.softwareag.com/techjforum/forums/list.page?product=webmethods-io-b2b).

You can find additional information in the [Software AG TECHcommunity](http://techcommunity.softwareag.com/home/-/product/name/webmethods-io-b2b).

______________________

These tools are provided as-is and without warranty or support. They do not constitute part of the Software AG product suite. Users are free to use, fork and modify them, subject to the license agreement. While Software AG welcomes contributions, we cannot guarantee to include every contribution in the master project.

Contact us at [TECHcommunity](mailto:technologycommunity@softwareag.com?subject=Github/SoftwareAG) if you have any questions.