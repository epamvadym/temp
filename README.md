## Running the tests
First, you need to download and install [Java SE Development Kit 8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) 
and set up the Environment Variables JAVA_HOME and PATH [link](https://docs.oracle.com/cd/E19182-01/821-0917/inst_jdk_javahome_t/index.html).

Then, to build up project you need the SDK v26, the best way is to install development environment [Android Studio](https://developer.android.com/studio/index.html), 
from where you can download the SDK and checkout the project from GitHub. 

When the installing is finished, checkout the project from GitHub

![checkout](https://user-images.githubusercontent.com/36236584/36541130-94014cfa-17e5-11e8-9320-35b3f5eb5138.png)
![clone](https://user-images.githubusercontent.com/36236584/36541198-cd778634-17e5-11e8-9a31-b681b0778ab1.png)

After that the studio download the environment it needs and build the project.


When the project is built, there two ways how to run tests:
#### From Android Studio:
Open the app/java folder, right ckick the test directory and run it

![run studio](https://user-images.githubusercontent.com/36236584/36541485-bc6cabd4-17e6-11e8-854c-82779c3642a1.png)

#### From command line
If you do not want Android Studio, you can download the basic Android command line tools and 
use the included [sdkmanager](https://developer.android.com/studio/command-line/sdkmanager.html) to download other SDK packages.
This way you need to add the local.properties file with the path to sdk `sdk.dir=D\:\\..\\sdk` file at the root of the project. 

Open the command line at the root of the project and run `./gradlew test` (or `gradlew test` for Windows) command

![run tests](https://user-images.githubusercontent.com/36236584/36541649-4986e340-17e7-11e8-85ef-beb68bf102ec.png)

You can see the which test are passed and failed

![running tests](https://user-images.githubusercontent.com/36236584/36543391-5255db70-17ec-11e8-921c-2a057957848e.png)

The test reports are built at `..\hs-android-customer\app\build\reports\tests` directory where you can see the HTML result

![result](https://user-images.githubusercontent.com/36236584/36543605-e0127784-17ec-11e8-9c62-feb4a03e9ff2.png)

The `./gradlew test` command runs tests for all build variants, it's enough to use the 
`./gradlew testUniversalDebugUnitTest` command for testing only the universal build variant, so it will run faster.
