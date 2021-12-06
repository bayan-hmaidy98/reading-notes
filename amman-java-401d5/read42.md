# Location
**getting the last location is one of the google play provided services and to be able to use it we use the API provide from them.
One of the most known API's from google is fused location provider that is installed and downloaded from google play.**
* Using the Google Play services location APIs, your app can request the user's device's last known location.
* `fused location provider`. It manages the underlying location technology and provides a simple API for declaring high-level requirements.
## Specify app permissions
* Depending on the use cases of the features, apps that use location services must request location permissions.
* To protect user privacy, apps that use location services must request location permissions.
* The important thing when it comes to location permissions is that to include multiple permissions related to location. Which permissions you request, and how you request them, depend on the location requirements for your app’s use case.
* Types of location access
  * Category: Either foreground location or background location.
  * Accuracy: Either precise location or approximate location.
  * Foreground location: sharing or receiving location information only once, or for a defined amount of time.
* The system considers your app to be using foreground location if a feature of your app accesses the device’s current location in one of the following situations:
  * An activity that belongs to your app is visible.
  * Your app is running a foreground service.
  * Background location: An app requires background location access if a feature within the app constantly shares location with other users or uses the Geofencing API
_Accuracy , and there levels of accuracy_
* Approximate: Provides an estimate of the device’s location, to within about 1 mile (1.6 km).
* Precise: Provides an estimate of the device’s location that is as accurate as possible, usually within about 160 feet (50 meters) and sometimes as accurate as within 10 feet (a few meters) or better.  
* Request location access at runtime :
When a feature in your app needs location access, wait until the user interacts with the feature before making the permission request.
## Create location services client
* In your activity's onCreate() method, create an instance of the Fused Location Provider Client
```
    private FusedLocationProviderClient fusedLocationClient;
    // ..
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        // ...
        fusedLocationClient = LocationServices.getFusedLocationProviderClient(this);
    }
```
## Get the last known location
* we can get the last known location of a user's device after  creating the ALocation Services client.
* To retrieve the device location, use the fused location provider's `getLastLocation()` method.
* The `getLastLocation()` method returns a Task that may be used to get a Location object with a geographic location's latitude and longitude coordinates.
1. In the following cases, the location object may be null:
2. In the device settings, location is disabled.
3. The device did not keep track of its location.
4. The device's Google Play services have been restarted.
## Choose the best location estimate
The `FusedLocationProviderClient` provides several methods to retrieve device location information, you can use any of them:
1. `getLastLocation()` gets a location estimate more quickly and minimizes battery usage.
2. `getCurrentLocation()` gets a fresher, more accurate location.
* If your app calls `requestLocationUpdates()`, your app can sometimes consume large amounts of power if location isn't available, or if the request isn't stopped correctly after obtaining a fresh location.