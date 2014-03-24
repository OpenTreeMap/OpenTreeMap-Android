OpenTreeMap for Android
=======================

Development Instructions
------------------------

### Eclipse/ADT Setup

* Install libraries that eclipse needs to run:
  ```bash
  apt-get install ia32-libs
  ```

* download the ADT bundle of eclipse

* unzip it to become ~/adt

* set your workspace to whatever you like, does not have to be where the code or the adt lives.

* Using the SDK Manager, install necessary software:
  * From Extras, install `Google Play services`
  * For all the SDK versions that you will use, (currently API 8, API 16, API <latest>), grab:
    * `SDK Platform`
    * `Google APIs` (ARM if there's a choice)
    * `System Image` (if you are using an emulator)

### Device Setup

You'll need to setup your device for debugging, because emulators aren't really viable.
Follow these instructions:
http://developer.android.com/tools/device.html

### App Setup

* clone the OpenTreeMap_Android repo to wherever you store code

* clone the whatever version of the app you plan to develop in lieu of ExampleApp inside this repo

* The google-play-services library should have been downloaded, include it in your workspace:
  * Click `File > Import`, `Android > Existing Code`
  * Navigate to `<adt_folder>/sdk/extras/google/google_play_services/libproject/google-play-services_lib`

* Make sure that the reference to google-play-services_lib in project.properties is correct.
  * (In Eclipse : Properties/Android/Reference)

* Setup google maps API key. See [PDF](https://github.com/OpenTreeMap/OpenTreeMap-Android/blob/9b67bd669825ac0d87f7799d5ad79695f08c95a7/howto.pdf) for suggestions.

### Weird Bugs

If you get version problems with ADT and the SDK, checkout [this thread](http://code.google.com/p/android/issues/detail?id=67325).

If your debug.keystore is not generated, you probably won't be able to run the [keytool command](https://developers.google.com/maps/documentation/android/start#obtain_a_google_maps_api_key). You can create one by right-clicking the project, Android Tools, Export *signed* application and even if it fails it should make debug.keystore.

USDA Grant
---------------
Portions of OpenTreeMap are based upon work supported by the National Institute of Food and Agriculture, U.S. Department of Agriculture, under Agreement No. 2010-33610-20937, 2011-33610-30511, 2011-33610-30862 and 2012-33610-19997 of the Small Business Innovation Research Grants Program. Any opinions, findings, and conclusions, or recommendations expressed on the OpenTreeMap website are those of Azavea and do not necessarily reflect the view of the U.S. Department of Agriculture.
