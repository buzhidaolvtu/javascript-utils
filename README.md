# javascript-utils

* retry(task, count, timeout)

	示例：  
	```
    retry(function() {
            var deferred = this;
            console.log(new Date().format('hh-mm-ss.S'), "execute task");
            $.get('http://www.baidu.com')  //请替换成允许跨域的URL
                .then(function() {
                    deferred.reject();
                    // deferred.resolve();
                })
        }, 5, 1000)
        .done(function() {
            console.log(new Date().format('hh-mm-ss.S'), "success");
        })
        .fail(function() {
            console.log(new Date().format('hh-mm-ss.S'), "fail");
        })
 	```       

* urlTemplate2(url)

	示例：  
	```
	urlTemplate2("http://localhost:8080/{var1}/{var2}/{var}",'a','b','c')
	=>
	http://localhost:8080/a/b/c
	```

* CopyToClipboard(containerid)
