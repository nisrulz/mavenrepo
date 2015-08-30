#Easy DeviceInfo

Enabling device information to be at android developers hand like a piece of cake!
Checkout the app using the same in [Playstore](https://play.google.com/store/apps/details?id=in.excogitation.deviceinfo)
#Integration
- Include the below into your app's ***build.gradle*** right at the very bottom.
```gradle
repositories {
    maven{
        url 'https://github.com/nisrulz/mavenrepo/raw/master/releases'
    }
}
```
- Next add the dependency
```gradle
compile 'com.github.nisrulz:easydeviceinfo:1.1.2'
```

#Usage
+ Create an instance of ***EasyDeviceInfo*** class
```java
EasyDeviceInfo easyDeviceInfo=new EasyDeviceInfo(context);
```
+ Next call the required function on the ***easyDeviceInfo*** instance such as
```java
String value=easyDeviceInfo.functionName();
```

|Value|functionName|returns
|---|---|---|
|Time|`getFormatedTime()`|String
|Language|`getLanguage()`|String
|Android ID|`getAndroidID()`|String
|IMEI|`getIMEI()`|String
|IMSI|`getIMSI()`|String
|GSFID|`getGSFID()`|String
|Pseudo ID|`getPsuedoUniqueID()`|String
|Device Serial Number|`getSerial()`|String
|SIM Serial Number|`getSIMSerial()`|String
|Manufacturer|`getManufacturer()`|String
|Model|`getModel()`|String
|OS Codename|`getOSCodename()`|String
|OS Version|`getOSVersion()`|String
|Country|`getCountry()`|String
|WiFi MAC Address|`getWifiMAC()`|String
|Bluetooth MAC Address|`getBluetoothMAC()`|String
|Display Resolution|`getResolution()`|String
|Phone Number|`getPhoneNo()`|String
|ISP/Carrier|`getCarrier()`|String
|Radio Hardware Version|`getRadioVer()`|String
|Product|`getProduct()`|String
|Device|`getDevice()`|String
|Board|`getBoard()`|String
|Hardware|`getHardware()`|String
|Bootloader|`getBootloader()`|String
|IP Address|`getIPAddress()`|String
|Type of Network|`getNetworkType()`|String
|User Agent|`getUA()`|String
|Fingerprint|`getFingerprint()`|String
|Screen Density|`getDensity(context)`|String
|Installer Store|`getStore(context)`|String
|Is internet available|`isNetworkAvailable()`|boolean
|Is running on emulator|`isRunningOnEmulator()`|boolean


---

+ To get Latitude-Longitude (Geo)
```java
//Get Lat-Long
double[] l = easyDeviceInfo.getLatLong(this);
String lat = String.valueOf(l[0]);
String lon = String.valueOf(l[1]);
```

+ To get Email IDs
```java
//Get Google Email ID
StringBuilder emailIDs = new StringBuilder();
	for (String eid : easyDeviceInfo.getAccounts(this)) {
			emailIDs.append(eid).append("\n");
		};

String emailId=emailIDs.toString();
```

+ To get Advertiser's ID
```java
//Get Android Advertiser ID
		easyDeviceInfo.getAndroidAdId(MainActivity.this, new EasyDeviceInfo.AdIdentifierCallback() {
			@Override
			public void onSuccess(String adIdentifier, boolean adDonotTrack) {
				// Do something with the advertiser's ID
			}
		});

```


# License

 <a rel="license" href="http://www.apache.org/licenses/LICENSE-2.0.html" target="_blank">Apache License 2.0</a>
