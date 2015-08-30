
![enter image description here](https://github.com/nisrulz/zentone/raw/master/app/src/main/res/mipmap-xhdpi/ic_launcher.png)

#ZenTone

Generating pure tone of an specific frequency was never that easy.
ZenTone does all the heavy lifting for you.

Checkout the app using the same in [Playstore](https://play.google.com/store/apps/details?id=in.excogitation.library_zentone) and the code on [Github](https://github.com/nisrulz/zentone).

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
compile 'com.github.nisrulz:zentone:1.0.0'
```

#Usage
+ To play a tone of certain frequency and duration
```java
ZenTone.getInstance().generate(freq, duration);
```
*where*

|argument|type|value in
|---|---|---|
|freq|`int`|Hz
|duration|`int`|seconds


+ To stop the tone
```java
ZenTone.getInstance().stop();
```

# License

 <a rel="license" href="http://www.apache.org/licenses/LICENSE-2.0.html" target="_blank">Apache License 2.0</a>
