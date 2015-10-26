#Sensey

Simplified sensor based gesture detection android library.

#Integration
- Include the below into your app's ***build.gradle*** right at the very bottom.
```gradle
repositories {
    maven{
        url 'http://maven.excogitation.in/'
    }
}
```
- Next add the dependency
```gradle
compile 'com.github.nisrulz:sensey:1.0.0'
```

#Usage
+ To register listening for a gesture
```java
Sensey.getInstance().initWithGesture(context, Sensey.TYPE_OF_GESTURE);
```

+ To setup listener for gesture events
```java
Sensey.getInstance().setGestureListener(Sensey.TYPE_OF_GESTURE, new TYPE_OF_GESTUREListener() {
  @Override
//Corresponding Functions here
});
```

+ To unregister listening for a gesture
```java
Sensey.getInstance().unregisterGestureDetector(Sensey.TYPE_OF_GESTURE);
```

where

|Type of Gesture|TYPE_OF_GESTUREListener()|
|---|---|
|SHAKE|`ShakeListener`|
|FLIP|`FlipListener`|
|ORIENTATION|`OrientationListener`|
|PROXIMITY|`ProximityListener`|

# License

 <a rel="license" href="http://www.apache.org/licenses/LICENSE-2.0.html" target="_blank">Apache License 2.0</a>
