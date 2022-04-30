# Log4j

![pattern](../images/Java/log4j.PNG)

code below should be added so that every time you create a new instance of the logger these settings will remain

```JAVA
consoleAppender.activateOption();
Logger.getRootLogger().addAppender(consoleAppender);
```