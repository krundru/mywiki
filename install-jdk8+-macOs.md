# Install OpenJDK8+ on macOS
  Install oepn jdk 8,9,10,11,12,13,14 by downloading tar file.

1. Follow instructions on this [AdoptOpenJDK](https://adoptopenjdk.net/installation.html?variant=openjdk11&jvmVariant=hotspot#x64_mac-jdk) page to download & extract required JDK

2. Move extracted JDK directory to `/Library/Java/JavaVirtualMachines/`
   ``` 
   sudo mv $PWD/jdk-11.0.5+10 /Library/Java/JavaVirtualMachines/
   ```
3. Check if installation is successful using `/usr/libexec/java_home`
   ```
   C02YT9HGLVCF:javaworld kundru$ /usr/libexec/java_home -V
   Matching Java Virtual Machines (1):
   11.0.5, x86_64:	"OpenJDK 11.0.5"	/Library/Java/JavaVirtualMachines/jdk-11.0.5+10/Contents/Home
   ```
   **Note:**: `/usr/libexec/java_home` is pre installed utility to switch java versions. 
4. Verify java version 
   ```
    C02YT9HGLVCF:javaworld kundru$ java --version
    openjdk 11.0.5 2019-10-15
    OpenJDK Runtime Environment AdoptOpenJDK (build 11.0.5+10)
    OpenJDK 64-Bit Server VM AdoptOpenJDK (build 11.0.5+10, mixed mode)
   ```
