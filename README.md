PhoneKal
========

# Overview
This is a simple attempt to develop a PhoneGap plugin for the Kal library to present a calendar-driven date picker.

# Installation:
* Set up your PhoneGap project
* Convert it to ARC through the wizard (the default PhoneGap project template is not ARC-based)
* Add Kal (instructions from https://github.com/klazuka/Kal.git) - don't forget to set the "-all_load" linker flag
* Include the EventKit and EventKitUI frameworks
* Copy PhoneKal.m and PhoneKal.h into the Plugins group of your project
* Copy PhoneKal.js in your www folder and include it in the pages you need
* Declare the plugin in PhoneGap.plist using "PhoneKal" as the plugin name and class name 
* To use, invoke
    window.plugins.PhoneKal.presentPicker(options,function(result) {...});
where options is a dictionary that can have the following keys:
    - initialDate - the date initially selected in the picker
    - title - the title appearing in the navigation bar
and the function in second argument is the callback to be executed after selection of the date (passed as a string in format 'yyyy-m-d')

