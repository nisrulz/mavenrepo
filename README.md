#Github-Based Maven Repository

Maven repository hosted on github to facilitate hosting open source android libraries.

Use [gradle](https://gradle.org/) to pull them as a dependency into your android project.

How to use
----------
- Include the below into your app's ***build.gradle*** right at the very bottom.
```gradle
repositories {
    maven{
        url 'http://maven.excogitation.in/'
    }
}
```
- Next add the corresponding dependency
```gradle
compile 'gradle-reference-id'
```

where ```gradle-reference-id``` is

|Name of Dependency|gradle-reference-id|
|---|---|
|[EasyDeviceInfo](https://github.com/nisrulz/mavenrepo/tree/master/releases/com/github/nisrulz/easydeviceinfo)|`com.github.nisrulz:easydeviceinfo:1.1.4`|


# License

 <a rel="license" href="http://www.apache.org/licenses/LICENSE-2.0.html" target="_blank">Apache License 2.0</a>
