# Bug Demo Project for Maven Enforcer Plugin 3.0.0 M2

This project demonstrates a problem I have with the Enforcer Plugin after upgrading from version 3.0.0 M1 to version 3.0.0 M2.

## How to run the demo

1. `cd parent; mvn clean install`
2. `cd ../child; mvn clean install -U -Dno-tests -Denforce-release-ready`

The Enforcer Plugin complains on missing version information for plugins
although the plugin management section of the parent defines the
version information. 

Version 3.0.0 M1 works as expected. You can see the difference if 
you run the demo like this:

1. `cd parent; mvn clean install`
2. `cd ../child; mvn clean install -U -Dno-tests -Denforce-release-ready -Denforcer-plugin.version=3.0.0-M1`
