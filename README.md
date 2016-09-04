# MagicMirror-LocalTransport-Module

<p>
<img src="https://img.shields.io/badge/Status-BETA-red.svg" alt="Status-BETA">
<a href="http://choosealicense.com/licenses/mit"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License"></a>
</p>

This module display the next local transport connection between an origin and destination.

![preview](https://github.com/GHLasse/MagicMirror-LocalTransport-Module/blob/master/.github/preview-Berlin.png)

## Installation

Go to your MagicMirror folder.

`cd MagicMirror`

Clone the repository.

`git clone https://github.com/CFenner/MagicMirror-LocalTransport-Module.git modules/localtransport`

## Configuration

Add module configuration to config.js.

```js
{
  module: 'localtransport',
  position: 'ANY_POSITION',
  config: {
    api_key: 'YOUR_API KEY',
    origin: 'YOUR_ORIGIN',
    destination: 'YOUR_DESTINATION'
  }
},
```

|Option|Description|
|---|---|
|`apiKey`|The API key, which can be obtained [here](https://developers.google.com/maps/documentation/directions/).<br><br>This value is **REQUIRED**|
|`origin`|The start location.<br><br>**Example:** `Mannheim HBF`<br>This value is **REQUIRED**|
|`destination`|The target location.<br><br>**Example:** `Frankfurt HBF`<br>This value is **REQUIRED**|
|`maximumEntries`|How many routes should be displayed?<br><br>**Default value:** `3`|
|`updateInterval`|How often does the content needs to be fetched? (Minutes) Note that the module refreshes every 15seconds to always display an accurate estimate when you need to leave.<br><br>**Default value:** `5`|
|`animationSpeed`|Speed of the update animation. (Seconds)<br><br>**Default value:** `1`|
|`displayStationLength`|Number of characters of the departure station for each transport mode to display. <br>0 means display all, <br>-1 means don't show the departure station<br><br>**Default value:** `0`|
|`displayWalk`|Boolean if steps for walking should be shown<br><br>**Default value:** `true`|
|`maxWalkTime`|Maximum time you are willing to walk between stations in minutes<br><br>**Default value:** `15`|
|`fade`|Boolean if a fade should be applied - same as for calendar module<br><br>**Default value:** `true`|
|`fadePoint`|Percentage, where the fade should start. This should be a value between 0 and 1 - same as for calendar module<br><br>**Default value:** `0.3`|
|`language`|Language to display information in - german 'de' or english 'en'<br><br>**Default value** `is same as defined in the main config file`|
|`units`|Units to use - metric or imperial<br><br>**Default value** `is same as defined in the main config file`|
|`timeFormat`|24 or 12 hour clock for displaying the arrival time<br><br>**Default value** `is same as defined in the main config file`|

## Preview of various settings


![London - left long block](https://github.com/GHLasse/MagicMirror-LocalTransport-Module/blob/master/.github/preview-London.png)
![Berlin - right short](https://github.com/GHLasse/MagicMirror-LocalTransport-Module/blob/master/.github/preview-Berlin.png)
![New York - left](https://github.com/GHLasse/MagicMirror-LocalTransport-Module/blob/master/.github/preview-NewYork.png)

## Special Thanks

Thanks to [SamLewis0602](https://github.com/SamLewis0602) for his module [MMM-Traffic by SamLewis0602](https://github.com/SamLewis0602/MMM-Traffic) on which this one is based on.
