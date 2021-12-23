# Log4J Maven Shade Hidden Vulnerable

This jar file was produced using the maven shade plugin 
https://maven.apache.org/plugins/maven-shade-plugin/index.html

This plugin is tyipcally used to resolve issues with multiple conflicting versions of dependencies on the Java classpath. 

I have seen it used often specificallyi to shade logging frameworks within some libraries.  

In this case, the configuration copies all classes from org.apache to a new hidden.org.apache folder structure. 

    <relocations>
        <relocation>
            <pattern>org.apache</pattern>
            <shadedPattern>hidden.org.apache</shadedPattern>
            <includes>
                <include>org.apache.*</include>
            </includes>
        </relocation>
    </relocations>

This file is vulnerable to CVE-2021-44228
 