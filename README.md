This is a maven repository hosted on github, where all my open source android libraries would be hosted.

Use [gradle](https://gradle.org/) to pull them as a dependency into your android project.

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
|[EasyDeviceInfo](https://github.com/nisrulz/mavenrepo/tree/master/releases/com/github/nisrulz/easydeviceinfo)|`com.github.nisrulz:easydeviceinfo:1.1.2`|
|[EvTrack](https://github.com/nisrulz/mavenrepo/tree/master/releases/com/github/nisrulz/evtrack)|`com.github.nisrulz:evtrack:1.0.0`|
|[OptimusHTTP](https://github.com/nisrulz/mavenrepo/tree/master/releases/com/github/nisrulz/optimushttp)|`com.github.nisrulz:easydeviceinfo:1.0.3`|
|[ZenTone](https://github.com/nisrulz/mavenrepo/tree/master/releases/com/github/nisrulz/zentone)|`com.github.nisrulz:zentone:1.0.0`|
|[Sensey](https://github.com/nisrulz/mavenrepo/tree/master/releases/com/github/nisrulz/sensey)|`com.github.nisrulz:sensey:1.0.0`|


# License

 <a rel="license" href="http://www.apache.org/licenses/LICENSE-2.0.html" target="_blank">Apache License 2.0</a>
