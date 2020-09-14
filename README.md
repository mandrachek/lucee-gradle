# lucee-gradle

This uses [gradle](https://gradle.org/) and the [gretty-gradle-plugin](https://gretty-gradle-plugin.github.io/gretty-doc/index.html).

If you run `./gradlew appStart` (or invoke the task from your IDE) this will start embedded tomcat9. However because gretty uses some 
tricks to create [virtual WEB-INF/lib](https://gretty-gradle-plugin.github.io/gretty-doc/Web-app-virtual-webinflibs.html) entries, 
lucee can't see where the jar is, and puts the lucee-server folder under the catalina.home (e.g., the tomcat.8080 folder).

However, if you run `./gradle appRunWar` instead, it will build a war file (or assemble what would be in the exploded version of the war) 
and run that instead. 



