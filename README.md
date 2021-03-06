# @ionic-native/Google Maps plugin demo (on progress)

This is a demo application of [@ionic-native/Google Maps plugin](https://ionicframework.com/docs/native/google-maps/).

Unfortunately, the current wrapper plugin has lots of mistake.

In order to find out, Masashi(@wf9a5m75) needs to test all methods.
But unfortunately, he's unfamiliar with the ionic framework and the [Cordova Google Maps Plugin](https://github.com/mapsplugin/cordova-plugin-googlemaps) has lots of methods to implement.

## What do Masashi need help with?

I've has been trying to port the code from [JavaScript version demo](https://github.com/mapsplugin/v2.0-demo) into the ionic wrapper version demo [(ionic-googlemaps-demo)](https://github.com/wf9a5m75/ionic-googlemaps-demo).

Please help me to create each pages in ionic style.

## How to contribute?

It is a really easy job. Just convert what is in JavaScript to TypeScript.

**STEP-1: Fork this project on github**

Click on this button, then fork this project.

<img src="http://readme-pics.s3.amazonaws.com/fork_button.jpg" width="400">

**STEP-2: Clone the forked your repo into your local machine**

```
$> git clone https://github.com/(your account name)/ionic-googlemaps-demo

$> cd ionic-google-maps
```

**STEP-3: Create a branch with your github account name**

In order to conflict with other people, please create a branch.
For example, Masashi's github account name is @wf9a5m75.

```
$> git checkout -b wf9a5m75  // create a new branch

$> git push --set-upstream origin wf9a5m75
```

**STEP-4: Install**

Don't forget to enable the Google Maps Android API v2/Google Maps SDK for iOS
at the Google APIs console.

The package name is `ionic.google.maps`

```
$> npm install -g ionic@latest

$> ionic cordova platform add android (or ios)

$> cordova plugin add https://github.com/mapsplugin/cordova-plugin-googlemaps#multiple_maps --variable API_KEY_FOR_ANDROID="..." --variable API_KEY_FOR_IOS="..."
$> npm install @ionic-native/core (^4.2.1)  // must be 4.2.1 or over
$> npm install @ionic-native/googlemaps (^4.2.1)

```

**STEP-5: Run**

It should work.

```
$> ionic cordova run android -l
```

**STEP-6: Generate new page**

For example, create a page for `Map.animateCameraZoomIn()`.

```
$> cd (path to)ionic-googlemaps-demo

$> ionic generate page AnimateCameraZoomIn  // Don't generate if the page is already exists.
[OK] Generated a page named AnimateCameraZoomIn!

$> cd src/pages/

$> mv animate-camera-zoom-in map/
```

This will create package in pages folder(there is issue in ionic to allow to specify any location for generated folder).
All you have to do is move this folder into any folder. Restart your ionic cli and all changes will be presented.

**STEP-7: your work**

**STEP-8: Commit the files to your repo first**

```
$> git add pages/map/animate-camera-zoom-in/*

$> git commit -m "Add: map.animateCameraZoomIn()

$> git push
```

**STEP-9: Please send a pull request**
<img src="https://guides.github.com/activities/hello-world/create-pr.png" width="400">

Then Masashi will review and merge it.

----

## Before starting your work, please reserve the page.

When you want to create some pages, please let Masashi know which page do you want to create, at the slack channel (#general channel).

I will write your github account name on this README.md file.
----

## Current working progress

[x] means the page was created.

- [ ] Map
  - [x] getMap (@wf9a5m75)
  - [x] setDiv (@wf9a5m75)
  - [x] setMapTypeId (@wf9a5m75)
  - [x] animateCamera (@wf9a5m75)
  - [x] animateCameraZoomIn (@wf9a5m75)
  - [x] animateCameraZoomOut (@wf9a5m75)
  - [x] moveCamera (@wf9a5m75)
  - [x] moveCameraZoomIn (@wf9a5m75)
  - [x] moveCameraZoomOut (@wf9a5m75)
  - [x] getCameraPosition (@wf9a5m75)
  - [x] getCameraTarget (@wf9a5m75)
  - [x] getCameraZoom (@wf9a5m75)
  - [x] getCameraBearing (@wf9a5m75)
  - [x] getCameraTilt (@wf9a5m75)
  - [x] setCameraTarget (@wf9a5m75)
  - [x] setCameraZoom (@wf9a5m75)
  - [x] setCameraTilt (@wf9a5m75)
  - [x] setCameraBearing (@wf9a5m75)
  - [x] panBy (@quanganh206)
  - [x] getVisibleRegion (@wf9a5m75)
  - [x] getMyLocation (@quanganh206)
  - [x] setClickable (@quanganh206)
  - [x] remove (@wf9a5m75)
  - [x] clear (@wf9a5m75)
  - [x] fromLatLngToPoint (@wf9a5m75)
  - [x] fromPointToLatLng (@wf9a5m75)
  - [x] setMyLocationEnabled (@wf9a5m75)
  - [x] getFocusedBuilding (@wf9a5m75)
  - [x] setIndoorEnabled (@wf9a5m75)
  - [ ] setTrafficEnabled (@wf9a5m75)
  - [ ] setCompassEnabled (@wf9a5m75)
  - [ ] setAllGesturesEnabled (@wf9a5m75)
  - [ ] setVisible (@wf9a5m75)
  - [ ] setPadding (@wf9a5m75)
  - [ ] setOptions (@wf9a5m75)
  - [ ] toDataURL (@wf9a5m75)
  - [ ] MAP_CLICK (@wf9a5m75)
  - [ ] MAP_LONG_CLICK (@wf9a5m75)
  - [ ] MY_LOCATION_BUTTON_CLICK (@wf9a5m75)
  - [ ] CAMERA_EVENTS (@wf9a5m75)
  - [ ] MAP_DRAG_EVENTS (@wf9a5m75)
  - [ ] MAP_READY (@wf9a5m75)

- [ ] Marker
  - [x] map.addMarker
  - [x] getPosition (@pavel-kurnosov)
  - [x] showInfoWindow (@pavel-kurnosov)
  - [x] hideInfoWindow (@pavel-kurnosov)
  - [x] setAnimation (@pavel-kurnosov)
  - [x] isVisible (@pavel-kurnosov)
  - [x] setTitle (@pavel-kurnosov)
  - [x] setSnippet (@pavel-kurnosov)
  - [x] remove (@pavel-kurnosov)
  - [x] setIconAnchor (@pavel-kurnosov)
  - [x] setInfoWindowAnchor (@pavel-kurnosov)
  - [ ] isInfoWindowShown (@pavel-kurnosov)
  - [x] setOpacity (@pavel-kurnosov)
  - [x] setZIndex (@pavel-kurnosov)
  - [x] setVisible (@pavel-kurnosov)
  - [x] setDraggable (@pavel-kurnosov)
  - [x] setDisableAutoPan (@pavel-kurnosov)
  - [ ] setPosition (@pavel-kurnosov)
  - [ ] setRotation (@pavel-kurnosov)
  - [ ] setFlat (@pavel-kurnosov)
  - [ ] setIcon

- [ ] Circle
  - [ ] map.addCircle
  - [ ] setCenter
  - [ ] setRadius
  - [ ] setFillColor
  - [ ] setStrokeWidth
  - [ ] setStrokeColor
  - [ ] setClickable
  - [ ] setZIndex
  - [ ] remove
  - [ ] CIRCLE_CLICK

- [-] Polyline
  - [x] map.addPolyline (@quanganh206)
  - [ ] setPoints
  - [ ] getPoints
  - [ ] setGeodesic
  - [ ] setVisible
  - [ ] setClickable
  - [ ] setStrokeColor
  - [ ] setStrokeWidth
  - [ ] setZIndex
  - [ ] remove (@quanganh206)
  - [ ] POLYLINE_CLICK

- [ ] Polygone
  - [ ] map.addPolygon
  - [ ] setPoints
  - [ ] getPoints
  - [ ] setPoints
  - [ ] getHoles
  - [ ] setFillColor
  - [ ] setStrokeColor
  - [ ] setClickable
  - [ ] setVisible
  - [ ] setZIndex
  - [ ] remove
  - [ ] POLYGON_CLICK

- [ ] GroundOverlay
- [ ] map.addGroundOverlay
  - [ ] setBounds
  - [ ] setBearing
  - [ ] setImage
  - [ ] setOpacity
  - [ ] setClickable
  - [ ] setZIndex
  - [ ] remove
  - [ ] GROUND_OVERLAY_CLICK

- [ ] HtmlInfoWindow (@dasois)
  - [ ] new HtmlInfoWindow
  - [ ] setContent
  - [ ] setBackgroundColor
  - [ ] open
  - [ ] close

- [ ] TileOverlay
  - [ ] map.addTileLayer
  - [ ] setFadeIn
  - [ ] setZIndex
  - [ ] setOpacity
  - [ ] setVisible
  - [ ] remove

- [X] Geocoding (@ThorvaldAagaard)
  - [X] geocoding
  - [X] reverse_geocoding


- [ ] Environment
  - [ ] setBackgroundColor
  - [ ] getLicenseInfo

- [ ] encoding
  - [ ] encodePath
  - [ ] decodePath
