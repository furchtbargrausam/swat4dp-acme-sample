# swat4dp-acme-sample
a sample project setup showing how the fictional company ACME could use swat4dp

## Prerequisite
* Java
* Maven
* Ant
* (optional) Eclipse or any other IDE that facilitates Ant, Maven and Git integration 

## Setup


### Domains
* _admin_ : Domain for administrative services 
* _trash_ : Adminstrative domain that acts as recycle bin (needs to be disabled)
* util : Utility domain hosting business-relevant services
* business _ Main application domain hosting the sample business services

### Infrastructure
The preconfigured infra setup makes the following assumptions:

* Customer: acme
  * Zones: DMZ
    * Environments: dev
	  * Domains: adm, bu, util
  * Device Sets: dev
    * Devices: dev5

### Devices



## Delploy


## FAQ

1. How to resolve “java.lang.IllegalAccessError” issues with Java 17 or newer?
  * The Ant xmltask uses a library that still needs access to internal java functions.
    This works till Java 11 but with a newer JDK you have to add the following VM arguments:
	```
	--add-exports java.xml/com.sun.org.apache.xpath.internal.objects=ALL-UNNAMED
	--add-exports java.xml/com.sun.org.apache.xpath.internal=ALL-UNNAMED
	```

## Hints and Links
[How to resolve “java.lang.IllegalAccessError” OR “unnamed module cannot access class” Error in java 17](https://medium.com/@varunrathod0045/how-to-resolve-java-lang-illegalaccesserror-553ac2c83af9)
[Migrating From JDK 8 to Later JDK Releases ](https://docs.oracle.com/en/java/javase/19/migrate/migrating-jdk-8-later-jdk-releases.html#GUID-7744EF96-5899-4FB2-B34E-86D49B2E89B6)