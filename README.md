Newman
===

StackMob's HTTP client. More to come here soon.

How to use
===

Basic usage:
	
	```scala
	import com.stackmob.newman.DSL
	import com.stackmob.newman.ApacheHttpClient
	import java.net.URL
	implicit val client = new ApacheHttpClient
	//execute a GET request
	val url = new URL("http://google.com")
	val response = GET(url).execute.unsafePerformIO
	println("Response returned from %s with code %d, body %s".format(url.toString,
		response.code,
		response.bodyString)
	)
	```