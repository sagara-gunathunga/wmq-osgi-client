

Repackaging WMQ 7.1 client Jars to solve OSGi split-package problems
====================================================================

1. Copy following list of Jar files to "wmq-client/lib" directory from your WMQ installation.

-com.ibm.mq.headers.jar
-com.ibm.mq.jar
-com.ibm.mq.jmqi.jar
-com.ibm.mq.pcf.jar

2. Use following Maven command for repackaging.

"mvn clean package"

3. Repackaged OSGI bundle can be found here "wmq-client/target/wmq-client-1.0.0.jar"

4. Copy this OSGI bundle in to "wso2esb-4.8.1/repository/components/dropins" directory. 



NOTE 01 - Make sure you don't copy this bundle to "wso2esb-4.8.1/repository/components/lib" directory.

Note 02 - Make sure non of the following jar files contain neither on "wso2esb-4.8.1/repository/components/dropins" nor "wso2esb-4.8.1/repository/components/lib" directories. 

-com.ibm.mq.headers.jar
-com.ibm.mq.jar
-com.ibm.mq.jmqi.jar
-com.ibm.mq.pcf.jar
