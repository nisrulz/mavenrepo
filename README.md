#Github-Based Maven Repository

This is a maven repository hosted on github, where all my open source android libraries would be hosted.

You can use this to pull these android libraries as a dependency via [gradle](https://gradle.org/) build system.
How to use
----------
- Include the below into your app's ***build.gradle*** right at the very bottom.
```gradle
repositories {
    maven{
        url 'https://github.com/nisrulz/mavenrepo/raw/master/releases'
    }
}
```
- Next add the corresponding dependency 
```gradle
compile 'com.github.nisrulz:easydeviceinfo:1.1.2'
```
|Name of Dependency|gradle|
|---|---|
|EasyDeviceInfo|`com.github.nisrulz:easydeviceinfo:1.1.2`|
|EvTrack|`com.github.nisrulz:evtrack:1.0.0`|
|OptimusHTTP|`com.github.nisrulz:easydeviceinfo:1.0.3`|


# License

 <a rel="license" href="http://www.apache.org/licenses/LICENSE-2.0.html" target="_blank">Apache License 2.0</a>