# Example Cumulocity IoT UI customization

To deploy:

1. Create a branding in your cumulocity tenant
2. Download your branding in the created application "public-option". The file should have the name ui-assets.zip.
3. Unzip ui-assets.zip and replace the options.json file.
4. Add "extraCssUrls": [
        "/apps/public/public-options/branding.css"
    ] to the options.json file.
5. Extend you custom bradning in the branding.css file.
6. Zip via $zip ui-assets branding.css options.json cumulocity.json
7. Upload new application via c8ycli deploy or upload the zip via UI.
