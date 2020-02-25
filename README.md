# javaJarToMacOsApp

I have a java jar application to run on macOs. Application is updated maybe once or twice in a year so I need to pack it as installer not very often, that why the decision was made to move from InstallBuilder(2000$ licence) to something open source. I found IzPack. For my solution IzPack have few disadvantages, which are:
- it creates new jar from a jar.
- some files needs to be installed to /Library/LaunchAgents and this is possible only when installer jar is started using `sudo java -jar YourJar.jar`.
But it seems like IzPack is the best open source solution to create installer for MacOs/Windows/Linux. 

So, I have a installer jar now. That is why I decided to use jdk8 javapackager to create dmg image with .app installer. But when you start the installer app it asks for admin running privileges.

Useful links:
IzPack tool: http://izpack.org/

IzPack wiki: https://izpack.atlassian.net/wiki/spaces/IZPACK/pages/491528/IzPack%2B5

javapackager: https://docs.oracle.com/javase/8/docs/technotes/tools/unix/javapackager.html