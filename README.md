Titanium Cintric iOS SDK Wrapper
===========================================
Free drag and drop background location analytics for your app! Sign-up at Cintric.com to get your FREE SDK-Keys. 

QUICKSTART
------------

1. In appcelerator studio, choose help > install mobile module. Enter “https://cintric.com/sdk/titanium” for the URL and press ok (you can choose to install local or global if you prefer).

2. Add the following location flags to your tiapp.xml file under `<ios><plist><dict>`  
        `       <key>NSLocationAlwaysUsageDescription</key>
                <string>
                    //NOTE this will be displayed to the user! always background location
                </string>
                <key>NSLocationWhenInUseUsageDescription</key>
                <string>
                    //NOTE this will be displayed to the user! while in use location
                </string>
                <key>UIBackgroundModes</key>
			    <array>
			        <string>location</string>
			    </array> `
3. Add the following code anywhere your app initializes (Alloy.js):  
    `var Cintric = require('com.cintric.ios.titanium');`  
    ` Cintric.init('<##YOUR PUBLIC KEY##>','<##YOUR SECRET KEY##>');`  
4. When you are ready to trigger the location permission prompt and start the tracking you can call:  
    `Cintric.startBackgroundTracking();`  
    It will use the text you set in the location flag above. (You can call this immediately after the init code above if you wish).

Contact
------------

Email any questions to contact@cintric.com!
