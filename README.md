## FloatingActionButtonMenuDrag
 A Floating Action Button with Menu and Draggable 

[![1.0](https://jitpack.io/v/aeonSolutions/FloatingActionButtonMenuDrag.svg)](https://jitpack.io/#aeonSolutions/AeonLabs-Android-Floating-Action-Button-Menu-Drag) [![](https://jitci.com/gh/aeonSolutions/FloatingActionButtonMenuDrag/svg)](https://jitci.com/gh/aeonSolutions/AeonLabs-Android-Floating-Action-Button-Menu-Drag)
![](https://views.whatilearened.today/views/github/aeonSolutions/AeonLabs-Android-Floating-Action-Button-Menu-Drag.svg)
[![CodeFactor](https://www.codefactor.io/repository/github/aeonsolutions/AeonLabs-Android-Floating-Action-Button-Menu-Drag/badge/main)](https://www.codefactor.io/repository/github/aeonsolutions/AeonLabs-Android-Floating-Action-Button-Menu-Drag/overview/main)

An implementation of [Floating Action Button](http://www.google.com/design/spec/components/buttons.html#buttons-floating-action-button) for Android with lots of features, such as move on touch and hold the menu fab.
You can view a demostration of the library working on YouTube: [click to view](https://youtu.be/KYduCAGDWYE)

![GitHub all releases](https://img.shields.io/github/downloads/aeonSolutions/AeonLabs-Android-Floating-Action-Button-Menu-Drag/total?style=for-the-badge)
![GitHub search hit counter](https://img.shields.io/github/search/aeonSolutions/AeonLabs-Android-Floating-Action-Button-Menu-Drag/Floating%20Action%20Button?style=for-the-badge)
![GitHub](https://img.shields.io/github/license/aeonSolutions/AeonLabs-Android-Floating-Action-Button-Menu-Drag?style=for-the-badge)

### Requirements
The library requires Android **API Level 21+**.


### Features
- Option for Moveveable on touch and hold of the Menu button
- Ripple effect on Android Lollipop devices
- Option to set custom **normal**/**pressed**/**ripple** colors
- Option to set custom shadow color and offsets
- Option to disable shadow for buttons and (or) labels
- Option to set custom animations
- Option to set custom icon drawable
- Support for **normal** `56dp` and **mini** `40dp` button sizes
- Custom FloatingActionMenu icon animations
- Option to expand menu up and down
- Option to show labels to the left and to the right of the menu
- Option to show circle progress on `FloactinActionButton`
- Option to add button to the `FloatingActionMenu` programmatically
- Option to dim the `FloatinActionMenu`'s background
- *Option to remove all buttons from the `FloatingActionMenu`*
- *Option to set a label for the `FloatingActionMenu`'s button*

## Join the WhatsApp Group
If you like this kind of projects and want to stay updated with the latest research ideas and prototypes during the day and week, join the WhatsApp Group
[LDAD Lab & Prototyping](https://chat.whatsapp.com/FkNC7u83kuy2QRA5sqjBVg)

### Usage
Step 1. Add it in your root build.gradle at the end of repositories:

	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
Step 2. Add the dependency

	dependencies {
	        implementation 'com.github.aeonSolutions:FloatingActionButtonMenuDrag:1.1'
	}


Add the `aeonlabs.solutions.common.layout.fab.FloatingActionButton` to your layout XML file.
```XML
<FrameLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:fab="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <ListView
        android:id="@+id/list"
        android:layout_width="match_parent"
        android:layout_height="match_parent" />

    <aeonlabs.solutions.common.layout.fab.FloatingActionButton
        android:id="@+id/fab"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_gravity="bottom|right"
        android:layout_marginBottom="8dp"
        android:layout_marginRight="8dp"
        android:src="@drawable/ic_menu"
        fab:fab_colorNormal="@color/app_primary"
        fab:fab_colorPressed="@color/app_primary_pressed"
        fab:fab_colorRipple="@color/app_ripple"/>

</FrameLayout>
```
You can set an icon for the **FloatingActionButton** using `android:src` xml attribute. Use drawables of size `24dp` as specified by [guidlines](http://www.google.com/design/spec/components/buttons.html#buttons-floating-action-button). Icons of desired size can be generated with [Android Asset Studio](http://romannurik.github.io/AndroidAssetStudio/icons-generic.html).

### Floating action button
Here are all the **FloatingActionButton**'s xml attributes with their **default values** which means that you don't have to set all of them:
```XML
<aeonlabs.solutions.common.layout.fab.FloatingActionButton
        android:id="@+id/fab"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_gravity="bottom|right"
        android:layout_marginBottom="8dp"
        android:layout_marginRight="8dp"
        android:src="@drawable/your_icon_drawable"
        app:fab_colorNormal="#DA4336"
        app:fab_colorPressed="#E75043"
        app:fab_colorRipple="#99FFFFFF"
        app:fab_showShadow="true"
        app:fab_shadowColor="#66000000"
        app:fab_shadowRadius="4dp"
        app:fab_shadowXOffset="1dp"
        app:fab_shadowYOffset="3dp"
        app:fab_size="normal"
        app:fab_showAnimation="@anim/fab_scale_up"
        app:fab_hideAnimation="@anim/fab_scale_down"
        app:fab_label=""
        app:fab_progress_color="#FF009688"
        app:fab_progress_backgroundColor="#4D000000"
        app:fab_progress_indeterminate="false"
        app:fab_progress_max="100"
        app:fab_progress="0"
        app:fab_progress_showBackground="true"/>
```
All of these **FloatingActionButton**'s attributes has their corresponding getters and setters. So you can set them **programmatically**.

### Floating action menu
Here are all the **FloatingActionMenu**'s xml attributes with their **default values** which means that you don't have to set all of them:
```XML
<aeonlabs.solutions.common.layout.fab.FloatingActionMenu
        android:id="@+id/menu"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_alignParentBottom="true"
        android:layout_alignParentRight="true"
        android:layout_marginRight="10dp"
        android:layout_marginBottom="10dp"
        android:layout_marginLeft="10dp"
        fab:menu_fab_size="normal"
        fab:menu_showShadow="true"
        fab:menu_shadowColor="#66000000"
        fab:menu_shadowRadius="4dp"
        fab:menu_shadowXOffset="1dp"
        fab:menu_shadowYOffset="3dp"
        fab:menu_colorNormal="#DA4336"
        fab:menu_colorPressed="#E75043"
        fab:menu_colorRipple="#99FFFFFF"
        fab:menu_animationDelayPerItem="50"
        fab:menu_icon="@drawable/fab_add"
        fab:menu_buttonSpacing="0dp"
        fab:menu_labels_margin="0dp"
        fab:menu_labels_showAnimation="@anim/fab_slide_in_from_right"
        fab:menu_labels_hideAnimation="@anim/fab_slide_out_to_right"
        fab:menu_labels_paddingTop="4dp"
        fab:menu_labels_paddingRight="8dp"
        fab:menu_labels_paddingBottom="4dp"
        fab:menu_labels_paddingLeft="8dp"
        fab:menu_labels_padding="8dp"
        fab:menu_labels_textColor="#FFFFFF"
        fab:menu_labels_textSize="14sp"
        fab:menu_labels_cornerRadius="3dp"
        fab:menu_labels_colorNormal="#333333"
        fab:menu_labels_colorPressed="#444444"
        fab:menu_labels_colorRipple="#66FFFFFF"
        fab:menu_labels_showShadow="true"
        fab:menu_labels_singleLine="false"
        fab:menu_labels_ellipsize="none"
        fab:menu_labels_maxLines="-1"
        fab:menu_labels_style="@style/YourCustomLabelsStyle"
        fab:menu_labels_position="left"
        fab:menu_openDirection="up"
        fab:menu_backgroundColor="@android:color/transparent"
        fab:menu_fab_label="your_label_here"
        fab:menu_fab_show_animation="@anim/my_show_animation"
        fab:menu_fab_hide_animation="@anim/my_hide_animation">

        <aeonlabs.solutions.common.layout.fab.FloatingActionButton
            android:id="@+id/menu_item"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:src="@drawable/ic_star"
            fab:fab_size="mini"
            fab:fab_label="Menu item 1" />

    </aeonlabs.solutions.common.layout.fab.FloatingActionMenu>
```

If you're using custom style for labels - other labels attributes will be ignored.

Labels shadow preferences depends on their corresponding **FloatingActionButtons**' shadow preferences.

For more usage examples check the **sample** project.


#### Credits:
this project is a functionality upgrade from the discontinued project below:
[visit Clans on Github](https://github.com/Clans/FloatingActionButton) by Dmytro Tarianyk as base development,
from previous project [android-floating-action-button](https://github.com/futuresimple/android-floating-action-button) library by Jerzy Chalupski as a base for development.

<br />
<br />

## Author

You can get in touch with me on my LinkedIn Profile:

#### Miguel Tomas

[![LinkedIn Link](https://img.shields.io/badge/Connect-Miguel--Tomas-blue.svg?logo=linkedin&longCache=true&style=social&label=Connect)](https://www.linkedin.com/in/migueltomas/)

<a href="https://stackexchange.com/users/18907312/miguel-silva"><img src="https://stackexchange.com/users/flair/18907312.png" width="208" height="58" alt="profile for Miguel Silva on Stack Exchange, a network of free, community-driven Q&amp;A sites" title="profile for Miguel Silva on Stack Exchange, a network of free, community-driven Q&amp;A sites" /></a>

<a href="https://app.userfeel.com/t/2f6cb1e0" target="_blank"><img src="https://app.userfeel.com/tester/737648/image?.png" width="257" class="no-b-lazy"></a>

You can also follow my GitHub Profile to stay updated about my latest projects: [![GitHub Follow](https://img.shields.io/badge/Connect-Miguel--Tomas-blue.svg?logo=Github&longCache=true&style=social&label=Follow)](https://github.com/aeonSolutions)

<br>

### Be supportive of my dedication and work towards technology education and buy me a cup of coffee
The PCB Desgin Files i provide here for anyone to use are free. If you like this Smart Device or use it, please consider buying me a cup of coffee, a slice of pizza or a book to help me study, eat and think new PCB design files.

<p align+"left">
<a href="https://www.buymeacoffee.com/migueltomas">
   <img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" data-canonical-src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" height="35" />
 </a>
<br>
<img src="https://github.com/aeonSolutions/PCB-Prototyping-Catalogue/blob/main/Designs/bmc_qr.png" height="130">
</p>



<br />

### Make a donation on Paypal
Make a donation on paypal and get a TAX refund*.

[![](https://github.com/aeonSolutions/PCB-Prototyping-Catalogue/blob/main/paypal_small.png)](http://paypal.me/mtpsilva)

<br>

### Support all these open hardware projects and become a patreon  
Liked any of my PCB KiCad Designs? Help and Support my open work to all by becomming a LDAD Patreon.
In return I will give a free PCB design in KiCad to all patreon supporters. To learn more go to patreon.com. Link below.

[![](https://github.com/aeonSolutions/PCB-Prototyping-Catalogue/blob/main/patreon_small.png)](https://www.patreon.com/ldad)

<br />
<br />

______________________________________________________________________________________________________________________________
### License

Before proceeding to download any of AeonLabs software solutions for open-source development and/or PCB hardware electronics development make sure you are choosing the right license for your project. See [AeonLabs Solutions for Open Hardware & Source Development](https://github.com/aeonSolutions/PCB-Prototyping-Catalogue/wiki/AeonLabs-Solutions-for-Open-Hardware-&-Source-Development) for more information. 



______________________________________________________________________________________________________________________________
