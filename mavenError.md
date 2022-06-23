# Mac, Maven error: No complier is provided in this environment.Perhaps you are running on a JRE rather than a JDK?

When i am using command ```mvn clean verify``` the error "No complier is provided in this environment.Perhaps you are running on a JRE rather than a JDK?" happens. 

1. Because the error message is no compiler privided,so first check maven status using command `mvn --version` : i got the information like this: 
> Apache Maven 3.8.1 (05c21c65bdfed0f71a2f2ada8b84da59348c4c5d)  
Maven home: /Users/lynnyang/work/apache-maven-3.8.1  
Java version: 1.8.0_331, vendor: Oracle Corporation, runtime: /Library/Internet Plug-Ins/JavaAppletPlugin.plugin/Contents/Home  
Default locale: en_GB, platform encoding: UTF-8  
OS name: "mac os x", version: "12.4", arch: "x86_64", family: "mac"  

From this I can see this is not the target java.
2. check java status using command `/usr/libexec/java_home -V` and got inforation below:
> Matching Java Virtual Machines (2):  
    1.8.331.09 (x86_64) "Oracle Corporation" - "Java" /Library/Internet Plug-Ins/JavaAppletPlugin.plugin/Contents/Home  
    1.8.0_271 (x86_64) "Oracle Corporation" - "Java SE 8" /Library/Java/JavaVirtualMachines/jdk1.8.0_271.jdk/Contents/Home  
/Library/Internet Plug-Ins/JavaAppletPlugin.plugin/Contents/Home

The second one is what I want here. so set the ```JAVA_HOME``` to the right PATH using:
```
export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_271.jdk/Contents/Home
```
Check the mvn status again by ```mvn clean verify```
