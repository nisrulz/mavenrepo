#EvTrack

Event & Exception tracking simplified.
Based of [EasyDeviceInfo](https://github.com/nisrulz/mavenrepo/tree/master/releases/com/github/nisrulz/easydeviceinfo) lib and [okhttp](https://github.com/square/okhttp).

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
compile 'com.github.nisrulz:evtrack:1.0.0'
```

#Usage
+ Create an instance of the ***EvTrack*** class
```java
EvTrack evTrack== new EvTrack();
```

+ Next if in debug stage, enable logs
```java
evTrack.enableLogs();
```

+ To record an event, pass in an ArrayMap to recordEvent() function
```java
ArrayMap<String, String> event_params = new ArrayMap<String,String>();
event_params.put("key1", "value1");
event_params.put("key2", "value2");
..
event_params.put("key7", "value7");
evTrack.recordEvent(context, event_params, SERVER_URL);
```

+ To record an exception, pass in an ArrayMap to recordException() function
```java
ArrayMap<String, String> exp_param = new ArrayMap<String,String>();
exp_param.put("key1", "value1");
exp_param.put("key2", "value2");
..
exp_param.put("key7", "value7");
evTrack.recordException(context, exp_param, SERVER_URL);
```

# License

 <a rel="license" href="http://www.apache.org/licenses/LICENSE-2.0.html" target="_blank">Apache License 2.0</a>
