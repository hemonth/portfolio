+++
date = "2017-08-05T12:00:00"
draft = false
tags = ["jShell", "java 9", "JDK 9 REPL", "REPL"]
title = "jShell Introduction"
summary = """
Read-Evaluate-Print-Loop has been there in Lisp, Python, Ruby, Groovy, Clojure, and other languages for a while. Unix shell is a REPL which can read shell commands, evaluate them, print the output, and goes back in the loop to do the same thing.
"""

# caption = "Image credit: [**Academic**](https://github.com/gcushen/hugo-academic/)"
+++

One of the new coolest feature of java 9 is jShell. jShell / Project Kulla is the first official Java REPL (Read-Eval-Print-Loop), a command line tool that lets you run Java statements on their own without having to wrap them in classes or methods. We know scala and groovy already have this feature. Among the upcoming features of Java 9, it's definitely going to be more interesting ones. To fire up and start playing with jshell we need to download jdk & jre 9 from <http://jdk.java.net/9/> . Once you are done with installation you need to setup JAVA_HOME as

```
JAVA_HOME = C:\Program Files\Java\jdk-9
```

once you are done setting the path variables open the command prompt and verify the java version

```
java -version
java version "9"
Java(TM) SE Runtime Environment (build 9+181)
Java HotSpot(TM) 64-Bit Server VM (build 9+181, mixed mode)
```

Once you see this, you can start using jShell by typing jShell on command prompt.

Now lets see some of the cool features of jShell:

# Expressions:

Simply just type any valid java expression it will return you the value.

```
jshell> 1+2
$1 ==> 3

jshell>
```

# Default Imports:

By default you will get a set of common imports

```
jshell> /imports
|    import java.io.*
|    import java.math.*
|    import java.net.*
|    import java.nio.file.*
|    import java.util.*
|    import java.util.concurrent.*
|    import java.util.function.*
|    import java.util.prefs.*
|    import java.util.regex.*
|    import java.util.stream.*
```

```
jshell> Math.sqrt(16)
$2 ==> 4.0
jshell>
```

# Variables:

Declare variables and name them. Once you do that they become visible in scope.

```
jshell> int x=5
x ==> 5
jshell> int y=30
y ==> 30
jshell> int z=x+y
z ==> 35
```

# Methods:

Define methods and even replace them.

```
jshell> public void helloWorld(){ System.out.println("Hello World!!"); }
|  created method helloWorld()

jshell> public void helloWorld(){ System.out.println("Override method successful!!"); }
|  modified method helloWorld()

jshell> helloWorld()
Override method successful!!
```

# Commands:

`/help` lists all the commands jShell provides. Some of the most useful once are:

## Listing Variables

```
  jshell> /vars
  |    int $1 = 3
  |    double $2 = 4.0
  |    int x = 5
  |    int y = 30
  |    int z = 35
  jshell>
```

## Listing Methods

```
  jshell> /methods
  |    void helloWorld()
  jshell>
```

## Listing Sources

```
  jshell> /list
  1 : 1+2
  2 : Math.sqrt(16)
  10 : int x=5;
  11 : int y=30;
  12 : int z=x+y;
  14 : public void helloWorld(){ System.out.println("Override method successful!!"); }
  15 : helloWorld()
  jshell>
```

## Editing Sources In External Editor

```
  jshell> /edit helloWorld
  |  modified method helloWorld()
  jshell>
```

`/edit` will bring up an jShell edit pad and allow user to edit.
[![jShell Edit Pad](https://www.packtpub.com/graphics/9781787282841/graphics/image_01_006.jpg)]()

## Testing Java Niuanses

Comparing autoboxed integers references which values are from range -128 to 127 (inclusive) returns true (they are cached)? You can verify that with shell in a matter of seconds:

```
  jshell> Integer i=129
  i ==> 129
  jshell> Integer j=129
  j ==> 129
  jshell> i == j
  $28 ==> false
  jshell> Integer i=127
  i ==> 127
  jshell> Integer j=127
  j ==> 127
  jshell> i == j
  $31 ==> true
  jshell>
```

## REPL Networking

With jShell we're not confined to our machine and have networking access, this opens up some interesting opportunities. For instance, think about using it as a terminal to communicate with your server, connecting remotely and controlling some parameters from the outside. Another option would be querying your database, and the possibilities here are really endless.

```
jshell> URL url = new URL("https://twitter.com/hemonthmandava")
url ==> https://twitter.com/hemonthmandava

jshell> URLConnection connection = url.openConnection()
connection ==> sun.net.www.protocol.https.DelegateHttpsURLConnec ... twitter.com/hemonthmandava

jshell> connection.getHeaderFields()
$34 ==> {date=[Sat, 05 Aug 2017 23:52:30 GMT], null=[HTTP/1.1 200 OK], server=[tsa_b], x-ua-compatible=[IE=edge,chrome=1], expires=[Tue, 31 Mar 1981 05:00:00 GMT], x-response-time=[231], transfer-encoding=[chunked], x-frame-options=[SAMEORIGIN], x-transaction=[004281e90002c12f], strict-transport-security=[max-age=631138519], pragma=[no-cache], set-cookie=[ct0=d2178dc1826ab3f42a02c86296e05f21; Expires=Sun, 06 Aug 2017 05:52:30 UTC; Path=/; Domain=.twitter.com; Secure, guest_id=v1%3A150197715027179788; Expires=Mon, 05 Aug 2019 23:52:30 UTC; Path=/; Domain=.twitter.com, personalization_id="v1_0YKziyiLVsomYk1ppqSf6w=="; Expires=Mon, 05 Aug 2019 23:52:30 UTC; Path=/; ... at, 05 Aug 2017 23:52:30 GMT], x-xss-protection=[1; mode=block], x-content-type-options=[nosniff], x-connection-hash=[99684d9ded1cc7abf5f1facfda4cee96], x-twitter-response-tags=[BouncerCompliant], content-type=[text/html;charset=utf-8], cache-control=[no-cache, no-store, must-revalidate, pre-check=0, post-check=0], status=[200 OK]}
jshell>
```

# Conclusion:

JShell is a very useful tool for prototyping and testing Java code snippets. There is also a JShell Java api which allows you to evaluate JShell from java. Once the java 9 is out I bet there will be JShell integrations in most popualar IDEs - this will make using it even more handy.
