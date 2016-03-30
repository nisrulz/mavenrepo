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
|[EasyDeviceInfo](https://github.com/nisrulz/mavenrepo/tree/master/releases/com/github/nisrulz/easydeviceinfo)|`com.github.nisrulz:easydeviceinfo:1.1.5`|


License
=======

    Copyright 2016 Nishant Srivastava

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.