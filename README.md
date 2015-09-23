# Xcode: Simulated Metrics Size

## Objectives

1. Identify various iOS device size classes.
2. Set an explicit Simulated Metric Size while size classes are enabled.

## Size Classes

Up through the iPhone 4S, the form factor of the device family had remained a consistent 4:3 ratio. Even the iPad held to a formulaic size and resolution up until the iPad Retina and the iPad Mini. Now with the addition of the [iPhone 5, 6, and 6 Plus form factors](http://www.paintcodeapp.com/news/ultimate-guide-to-iphone-resolutions), and the myriad iPad sizes, the two standard form factors have evolved into over a dozen various sizes each with their own layout dynamics.

This, however, doesn't even take into consideration the split-screen functionality on iPads (i.e. master view applications) and device rotation (portrait vs. landscape). A truly robust application should be programmed to dynamically accommodate all of these layout scenarios.

Enter size classes.

Size classes allow the application to dynamically assess how it should lay itself out on a screen without needing explicit knowledge of the current device type. To encourage developers to program their layouts to be independent of any particular device, the default canvas size for a view controller in a storyboard file is an unusual 600 x 600 point square — a size which does not nor ever shall correspond to the dimensions of any existing or future iOS-capable mobile device.

**Note:** *A "point" is a measure of physical size roughly equivalent to one pixel on the original iPhone, which had 164.8 pixels (i.e. "points") per linear inch.*

While this has value in reminding seasoned developers to think outside the context of any single device, it takes an understanding of autolayout constraints to execute successfully — a topic which will not be covered until later. While you are learning how to use Interface Builder to create storyboarded applications, you should begin with static layouts designed for a single device shape that you are familiar with. Once you have gained experience with the basics of Interface Builder and storyboards, it will then be time to return to the generic 600 x 600 point canvas.

Because having size classes enabled affects the availability of segue types, it's necessary to have them turned on. However, to present a familiar canvas in the storyboard, a simulated metric size can be selected to render a canvas of a specific size. While some of labs will provide you with a view controller already set to a simulated metric size, the section below will walk you through how to change this selection on your own.

## Setting the Simulated Metric Size

To set a simulated size within the storyboard itself, follow the steps outlined below:

1 — Navigate to the storyboard file in your open application by using the Project Navigator in the Navigator Area.  

2 — Select the View Controller in the storyboard whose simulated size you wish to change.  

3 — Select the File Inspector pane in the Utilities Area.  

4 — Verify that the Use Size Classes option in the Interface Builder Document section is selected.

![](https://curriculum-content.s3.amazonaws.com/ios-segues-and-nav-controllers-unit/xcode_verify_size_classes.png)

5 — Select the Attributes Inspector pane (the fourth symbol) in the Utilities Area.  

6 — Open the drop down menu for Size in the Simulated Metrics section.

![](https://curriculum-content.s3.amazonaws.com/ios-segues-and-nav-controllers-unit/xcode_size_menu.png)

7 — Select the display size you wish to simulate (the iPhone 6/6S are 4.7 inches in screen size).  

8 — The View Controller's representation in the storyboard will change size according to your selection.

![](https://curriculum-content.s3.amazonaws.com/ios-segues-and-nav-controllers-unit/xcode_size_iphone6.png
)