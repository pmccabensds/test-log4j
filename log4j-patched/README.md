# Log4J Patched

This file was patched following guidlines to remove the JNDILookup.class file from the Log4J jar file.

The following command was used
zip -q -d log4j-core-*.jar org/apache/logging/log4j/core/lookup/JndiLookup.class

This file is not vulnerable to CVE-2021-44228

