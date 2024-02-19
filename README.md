# nifi-gradle-nar-example
*Thanks to fork from mattyb149*

Simpler example (than plugin) to build working processor nar for nifi 1.23.2 (java 11).

# using

- modify processor (`nifi-gradle-built-example-processors/src/main`)
    - package/path (`groovy/org/apache/nifi/processors/example/MyProcessor.groovy`)
    - metadata (`resources/META-INF/services/org.apache.nifi.processor.Processor`)
- increment nar_version (or it won't load over previous)</br>
`build.gradle`
- build</br>
`./gradlew clean build`
- deploy (validate)</br>
`docker cp nifi-gradle-built-example-processors`
- fix/improve test(s)</br>
`nifi-gradle-built-example-processors/src/main/test/../MyProcessorTest.groovy`
- git tag (followed by build, deploy)