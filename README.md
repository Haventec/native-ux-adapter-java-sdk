# Native UX Adapter Java SDK
Applications that would like to offer login pages with a native UX, could use this SDK to orchestrate the OpenID Connect flow from their application backend service.

## Installation

The .jar file can be imported into your Java project via the standard way of importing modules.

If using gradle, add the following repository:
```
repositories {
    ...
    ..
    .
    jcenter()
}
``` 
and the following dependencies:

```
dependencies {
   ...
   ..
   .
   // SDK library
   implementation 'com.haventec:native-ux-adapter-java-sdk:1.0.2'

   // Dependencies required due to the SDK library
   compile group: 'ch.qos.logback', name: 'logback-classic', version: '1.2.3'
   compile group: 'org.apache.httpcomponents', name: 'httpclient', version: '4.5.11'
   compile group: 'org.slf4j', name: 'log4j-over-slf4j', version: '1.7.25'
   compile group: 'com.fasterxml.jackson.core', name: 'jackson-databind', version: '2.11.0'
}
```

Ensure to use the latest published version of the SDK[ ![Download](https://api.bintray.com/packages/haventec/maven/native-ux-adapter-java-sdk/images/download.svg?version=1.0.3) ](https://bintray.com/haventec/maven/native-ux-adapter-java-sdk/1.0.3/link)


## Usage

To use the SDK, import the following class and its dependencies:
```
import com.haventec.nativeux.adapter.java.sdk.api.HaventecOidcLp;
```

This class has the following methods:

 * **createIamPasswordUser (Deprecated):** It creates a user in Haventec IAM
 * **loginIamPasswordUser:** It logs in users with credentials and device authentication.
 
 ## Demo app
 
 1. Create a personal config.properties file based on the template: 
 ```
 cd demo/nativeUxAdapterJavaSdkDemo/src/main/resources
 cp config.properties.template config.properties
 ```
 
 2. Fill in all the IAM properties and Haventec OIDC properties of your environment
 
 3. Open the folder demo/nativeUxAdapterJavaSdkDemo as a project in your IDE of choice
 
 4. Run the main class MainApp
 
 ## Development
 To build, run the following:
 ```
 ./gradlew clean build publish
 ```
 
 ## License
 
 This code is available under the MIT license. A copy of the license can be found in the LICENSE file included with the distribution.
