# Changes in 0.4.0 Alpha from 0.3.0 Alpha
* Added a `Thumbnails` section under `Globals` where you can modify how thumnails are displayed.
* Added a `Interface` section under `Globals` where you can activate sliding of objects as they enter the viewport. This section will have a lot more in future releases.

# Changes in 0.3.0 Alpha from 0.2.5 Alpha
* Completely revamped the image preloading to a lazy load hybrid which should greatly increase the page load speeds.
* Added functionality to autohide the header when it's set to fixed.

# Updating
## Updating from 0.3.0 Alpha to 0.4.0 Alpha
1. Replace the templates folder on your ftp with the one in this package (`craft/templates`).
2. Replace the js folder on your ftp with the one in this package.
3. Go to your admin and log in. Then go to `Settings > Plugins` and `Install` The Architect.
4. Go to `The Architect` and then the `Available Files` tab.
5. Click on `update.json` then click the `Construct` button at the very bottom of the page.
6. Go to `Settings > Plugins` and `Uninstall` The Architect.
7. Have another beer, you can now modify more aspects of Modul.

## Updating from 0.2.5 Alpha to 0.3.0 Alpha
Updating from 0.2.5 Alpha to 0.3.0 Alpha. Updates from prior versions require fresh install. This work-in-progress process will be simplified in future releases.
1. Replace the templates folder on your ftp with the one in this package (`craft/templates`).
2. Go to your admin and log in. Then go to `Settings > Plugins` and `Install` The Architect.
3. Go to `The Architect` and paste this code:
```
{
    "groups": [
        "Header"
    ],
    "fields": [
        {
            "group": "Header",
            "name": "Header Autohide",
            "handle": "headerAutohide",
            "instructions": "Hide the header automatically when the user scrolls down (it reappears when the user scrolls up or hits the bottom of the page). Only works for fixed navigation.",
            "required": false,
            "type": "Lightswitch",
            "typesettings": {
                "default": ""
            }
        }
    ]
}
```
4. Then click `Construct`.
5. Now go to `Settings > Globals > Header` and go to the `Field Layout` tab.
6. Below the `Content` box you'll see boxes with dashed borders. Drag `HEADER AUTOHIDE` from the box that says `HEADER` to the `Content` box, and drop just below `HEADER FIXED` and save the change.
7. Go to `Settings > Plugins` and `Uninstall` The Architect.
8. Have a beer, you can now autohide the header when it's set to fixed, if you'd like.