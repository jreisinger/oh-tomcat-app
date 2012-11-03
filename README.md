Tomcat script for running applications as seaprate instance.

Copy "oh-tomcat-app" to "/etc/init.d", create symlink "ln -s /etc/init.d/oh-tomcat-app /etc/init.d/&lt;your_app&gt;"
Create CATALINA_BASE in "/var/app/&lt;your_app&gt;". You can place config (JAVA_HOME etc.) in "/etc/default/&lt;your_app&gt;".
This file is read on startup.

Then you can just start you application by calling "/etc/init.d/&lt;your_app&gt; start"

Instead of copying the script, you can create .deb package by executing "./build n", where n is build number (ex. 1).
