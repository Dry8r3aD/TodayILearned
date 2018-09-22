# Using HTTP Request with timeouts

## About Requests
In Python, a HTTP Request(GET, POST, etc) can be easily created by using [Requests](http://docs.python-requests.org/en/master/). It's a simple HTTP library for Python and provides HTTP session related classes and methods.

For example, when we want to create a HTTP GET Request, we can simply write a code as follow.

```Python
➜  Python git:(master) ✗ python3
Python 3.6.5 (default, Apr 25 2018, 14:23:58)
[GCC 4.2.1 Compatible Apple LLVM 9.1.0 (clang-902.0.39.1)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> import requests
>>> response = requests.get('http://example.com')
>>> print(response)
<Response [200]>
>>> print(response.status_code)
200
```

## Session Timeouts
Let's say that a GET request is created and sent to the destination. If everything works fine, we will get a response from the destination, which will be usually a web server. BUT what if a web server is down, and GET request is sent? By default, Requests module will resend the request over and over.

To prevent a situation like this, Requests module provides a field to get a input from the developer to specifies the request timeout.

For example, the following code will create a GET request to http://111.111.111.111, which is not a reachable server at the current moment. As you can notice, this code never ends, and as far as there are no interrupts, it will run forever.

Exception: when we use a domain, and a domain is not lookable, requests module will not send the request, since it can not identify the destination address.

Comment: I don't know why, but when I use Python CLI, it automatically disconnects without the timeout value... Weird :/

```Python
➜  Python git:(master) ✗ python3
Python 3.6.5 (default, Apr 25 2018, 14:23:58)
[GCC 4.2.1 Compatible Apple LLVM 9.1.0 (clang-902.0.39.1)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> import requests
res = requests.get('http://111.111.111.111')
```

To prevent situations like this, we need to pass the timeout value as an argument when creating a HTTP request.

```Python
➜  Python git:(master) ✗ python3
Python 3.6.5 (default, Apr 25 2018, 14:23:58)
[GCC 4.2.1 Compatible Apple LLVM 9.1.0 (clang-902.0.39.1)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> import requests
res = requests.get('http://111.111.111.111', timeout=10)
```

In every HTTP request methods, we can specify the timeout value in seconds as above. In above example, the requests module will wait until 10 seconds are passed.
