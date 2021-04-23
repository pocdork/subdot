<p align="center">
	<br>
	<img src="images/ico.png">
	<br>
	Discover internal subdomains using dash (-), dot (.) expressions.
</p>
<br>
<h2>Requirements</h2>
<p>
	<h4>HTTPX:</h4> Thanks to <a href="https://github.com/projectdiscovery">ProjectDiscovery</a> for such a great tool. You can download <b>httpx</b> from <a href="https://github.com/projectdiscovery/httpx">here</a>.
</p>
<br>
<h2>PostAdd</h2>
<p>
	
```
./subdot <<< "sub-exp domains.txt exp.txt out.txt"
./subdot <<< "sub.exp domains.txt exp.txt out.txt"
```
```
sub-test.example.com
sub-ext.example.com
...
sub.test.example.com
sub.ext.example.com
```
</p>
<h2>PreAdd</h2>
<p>
	
```
./subdot <<< "exp-sub domains.txt exp.txt out.txt"
./subdot <<< "exp.sub domains.txt exp.txt out.txt"
```
```
test-sub.example.com
ext-sub.example.com
...
test.sub.example.com
ext.sub.example.com	
```
</p>
<h2>Usage</h2>
<p>
	Use <code>all</code> argument for perform all operation.
	
```
./subdot <<< "[sub-exp/sub.exp/exp-sub/exp.sub/all] domains.txt exp.txt out.txt"
```
	       
<p>The result then will be passed to <b>httpx</b> and you'll get final result like this:</p>
	       
```
https://sub-test.example.com [200]
https://sub-ext.example.com [503]
https://example-ext.com [404]
...
https://sub.test.example.com [301]
https://sub.ext.example.com [401]
https://exampletest.com [200]
```
</p>
<h2>ToDo</h2>

* Perform multi level subdomain discovery

<h2>Follow Me</h2>
<p>
	
<a href="https://twitter.com/pocdork/"><img src="images/twitter.svg" width="50" height="50"></a>
</p>

