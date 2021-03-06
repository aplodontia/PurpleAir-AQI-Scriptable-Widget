# PurpleAir-AQI-Scriptable-Widget

<img src="https://sixcolors.com/wp-content/uploads/2020/10/widget-44.jpg" width="400" />

By Jason Snell <jsnell@sixcolors.com> with enormous contributions by many others, including Matt Silverlock , Rob Silverii, Adam Lickel, Alexander Ogilvie, and Brian Donovan.

## About this project

This script is meant to be used inside [Scriptable](https://scriptable.app) to generate iOS home screen widgets. The trend line feature requires latest version of Scriptable, 1.5.1. It uses data from the [PurpleAir network](https://www2.purpleair.com) of low-cost, consumer air quality sensors to display your local air quality, including AQI rating and trend.

The EPA has a large, established network of air-quality sensors that feed into many weather apps and their assorted widgets. I built this tool because the nearest EPA sensor to me was three towns away and in heavy wildfire smoke conditions did not accurately reflect my local air quality. If you just want the official EPA sensors, you don't need this widget.

You can [read more about the origin of this project](https://sixcolors.com/post/2020/08/how-bad-is-the-air-out-there/) if you like.

## How does this widget calculate AQI?

AQI can be calculated in a lot of different ways. Standard AQI calculations were made with certain assumptions in place, including a goal of understanding industrial smog and and the use of expensive particle detectors. They were also meant to reflect long-term readings.

This widget uses the EPA-suggested calculation [detailed in this document](https://cfpub.epa.gov/si/si_public_record_report.cfm?dirEntryId=349513&Lab=CEMM&simplesearch=0&showcriteria=2&sortby=pubDate&timstype=&datebeginpublishedpresented=08/25/2018) for more immediate readings from low-cost sensors like PurpleAir in areas where wood smoke is an issue, such as those affected by smoke from wildfires. You can [read about the backstory here](https://thebolditalic.com/understanding-purpleair-vs-airnow-gov-measurements-of-wood-smoke-pollution-562923a55226).

To see this calculation on PurpleAir, choose **US EPA** from the Conversion popup on the PurpleAir map. If you tap on the widget when it's out on your home screen, you will be taken to the PurpleAir map for that station, with US EPA selected.

## What matters more, the numbers or the words/colors?

The words and colors! Earlier versions of this widget had a larger display for the numbers and a smaller display for the condition level, but the real point of AQI isn't a precise number, it's getting the level -- the words and color -- in the right zone. 

But we all like numbers, so it displays a number too. Also, the widget does display a trend if one exists, so if you're in volatile conditions, you should be able to tell at a glance if your air quality is improving or worsening. I found this very useful during a recent set of wildfires in my area.

## How to use this

To use it, make a new script inside the Scriptable and paste in the contents of purpleair-aqi.js. 

You can run the script from within the app, or add a new Small widget on your home screen, set it to Scriptable, choose the script, and enter the sensor ID from a nearby PurpleAir sensor in the Parameter field.

To find a sensor ID, go to the PurpleAir map and tap or click on a station near you. The URL in your browser should change to the new selection. A four- or five-digit number will appear just after "select=" and that's the number to enter in to the Parameter field.
