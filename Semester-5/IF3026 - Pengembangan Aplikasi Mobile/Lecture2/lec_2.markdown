---
title: "Structure Android Studio"
date: 2023-09-16 13:15:23
tags: []
categories: []
---

## Release Notes
---
* ProguardFiles

## Dependencies
---
* Used to insert any module that related to stuff

## Section res
---
* res module is used to store stuff like button (from android studio template
    for example)
* The layout is where the template of the main apps where

## Layout in XML
---
* Opening Tag
```kotlin
<LinearLayout
  android:layout_width="match_parent"
  android:layout_height="match_parent"
  android:orientation
```

### View Attribute in XML

## Activity Lifecycle
---
* Activity lifecycle methods are methods that are called by the Andriod system
    at various lifecycle of an activity
There are many activity lifecycle methods

## Intent
Used to do some actions in apps (inside or outside apps like accessing galery)

## View & ViewGroup
* ConstraintLayout, acts as a default layout for new Android Studio Project.
* Build complex apps views without a nested layout
* As a ViewGroup, ConstraintLayout Offers flexibility for layout design.
* Provides constrants to determine pos. and alignment of UI elements
* Acts as a connectino to another view; parent layout or invisble guideline.

### RecyclerView
* Has a light memory and good performance
* Contains ViewHolder by default.
* Easy animations for adding, updating or removing items
* Support layoutManager to change layout
* Suport 

Consist of 
- DataSource - ArrayList or list contain data class
- Adapter - Connects data to the RecyclerView
- Layout Item - XML file for one row of item
- ViewHolder - has view information for displaying one item
- LayoutManager - handle the organization of UI components in a view

## Fragment
---
* Class yang bergantung dengan Activity 
* Each Fragment instance has its own lifecycle
* Fragment fully dependent on the activity lifecycle in which it is embedded
    (e.g. when on activity state created, frament callbacks can call many
    Fragment)

## Conclusion
---
* Activity repersents a single screen in an Android App, the building blokc of
    an app user interface
* Intent is a messaging objects you can use to request an action from another
    app components, used to navigate between activities or to invoke different
    actions
* Fragment is a reusable components that represents part of an activity UI,
    allows you to build ma more modular and flexible user interface.
