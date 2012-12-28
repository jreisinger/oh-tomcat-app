Tomcat script for running applications as seaprate instance.

<ul>
    <li>
        Copy <b>oh-tomcat-app</b> to <b>/etc/init.d</b>
    </li>
    <li>
        Create symlink
        <b>ln -s /etc/init.d/oh-tomcat-app /etc/init.d/&lt;your_app&gt;</b>
    </li>
    <li>
        Create CATALINA_BASE in <b>/opt/&lt;your_app&gt;</b>
    </li>
    <li>
        Place config (JAVA_HOME etc.) in
        <b>/etc/default/&lt;your_app&gt;</b>
        This file is read on startup
    </li>
</ul>

Then you can just start you application by calling 
<b>/etc/init.d/&lt;your_app&gt; start</b>

Instead of copying the script, you can create .deb package by executing 
<b>./build <i>n</i></b> where <i>n</i> is build number (ex. 1).
