Equipment
=========

Information about the device and its environment.

use [OWL](https://www.w3.org/OWL/) for descriptions

##Devicetypes

--> Couple display/behavior to properties of the device, not the device type
define selectors for main properties 
- device display selector like 'mobile640', 'tablet1024', 'leds', 'none' ... add a 'default' selector
- device operation selector 'pointer', 'keyboard', 'remotecontrol', 'voice', ...
- device audio selector 'beep', 'none', 'hifi'

Define features of the device
- Query
````js
    if (window.matchMedia("only screen and (max-width: 760px) and (orientation: portrait)").matches) ...
````
    - https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries
    - https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Testing_media_queries
- Change Notifications:
````js
const mediaQueryList = window.matchMedia("(orientation: portrait)");
mediaQueryList.addEventListener('change', (evt) => { (evt.matches) ? x  : y });
````    
    
multiple properties
- 2 displays
- 'keyboard', 'mouse' & 'pointer'
- 'beep' & 'hifi'

multiple devices
- TV/Desktop & Tablet used together
 
- Phone like devices: will be held portrait (portrait), screensizes 4” to 10”, fingertip
- Tablett like devices: will be held landscape (lanscape), screensizes 6” to 13”, fingertip
- PC/Notebook like devices: landscape on table, screensizes 11” to 30+”, keyboard, mouse
    - TV like devices: some meters away, screensizes from 15”, remote control
    - 2nd screen (phone or tablet) with splited app as remote control
- Headless (Server class) without UI
    - processing only
    - network only
    - perhaps no other IO devices
- External Displays! disconnectable → multiple UI settings 
- Wearables
    - very small display (SmartWatch)
    - without display, just sensors
    - e.g. vibrator only
- Distinguish also the actual input device
    - Adjust Size/Display Size on tip for controls e.g. on fingertip devices enlarge at the first tip to show all options like sort asc/desc
    - mouse
    - fingertip
    - speech
    - (additional) keyboard
    
Express device
- Features
- Behaviors

##Network
- active/inacive
- networktype
    - https://developer.mozilla.org/en-US/docs/Web/API/NetworkInformation/type
- networkspeed
    - avg
    - max
    
##Energy
- power grid
- battery
    - is low
    - is charging
    - https://developer.mozilla.org/de/docs/Web/API/BatteryManager 
- change events

##Perfomance
- https://developer.mozilla.org/de/docs/Web/API/Performance

##GEO Location
- https://developer.mozilla.org/en-US/docs/Web/API/Geolocation/watchPosition

##Notification
