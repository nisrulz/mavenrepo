#OptimusHTTP

Transforming your ease of implementing networking in your android apps.
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
compile 'com.github.nisrulz:optimushttp:1.0.3'
```

#Usage
####Inside your Activity ( i.e MainActivity.java)
+ Create an object of OptimusHTTP class and intialize it (preferably inside your **onCreate()** function
```java
OptimusHTTP client = new OptimusHTTP();
```
----
+ Enable debugging (_**Use it only while testing**_)
```java
client.enableDebugging();
```
----
+ Set the request method to be used
```java
client.setMethod(OptimusHTTP.METHOD_POST);
```
+ Possible arguments

1. OptimusHTTP.METHOD_POST

2. OptimusHTTP.METHOD_GET

----
+ Set the request mode to be used
```java
client.setMode(OptimusHTTP.MODE_SEQ);
```
+ Possible arguments

1. OptimusHTTP.MODE_SEQ

2. OptimusHTTP.MODE_PARALLEL

----
+ Setup the params as a HashMap object
```java
HashMap<String, String> params = new HashMap<>();
params.put("key1", "value1");
params.put("key2", "value2");
```
----
+ Make a HTTP  Request
```java
HttpReq req=client.makeRequest(MainActivity.this, SERVER_URL + "test", params, new OptimusHTTP.ResponseListener() {
	@Override
	public void onSuccess(String msg) {
		System.out.println(msg);
	}

	@Override
	public void onFailure(String msg) {
		System.out.println(msg);
	}
});
```
_**req** is the HttpReq object_

_**MainActivity.this** is the context_

_**SERVER_URL** is the String object containing the server url_

_**params** is the HashMap object you created in the previous step_

_**OptimusHTTP.ResponseListener** is the Response Listener object to handle the response from the server_

----
+ Cancel a HttpReq
```java
client.cancelReq(req);
```
_**req** is the reference to the **HttpReq** object_

----
[**Need help?**](mailto:nisrulz@gmail.com?Subject=Library%20OptimusHTTP%20Integration%20Query/)


# License

 <a rel="license" href="http://www.apache.org/licenses/LICENSE-2.0.html" target="_blank">Apache License 2.0</a>
