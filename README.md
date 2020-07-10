# test-nexusiq-bc166

## Build and run CLM scan
CLM_SERVER_URL=<NEXUS_IQ_URL> CLM_USER=<USERNAME> CLM_PWD=<PASSWORD> mvn clean package verify

## Verify using nexus-iq-cli docker image 
docker run -v ${PWD}/target:/target sonatype/nexus-iq-cli /sonatype/evaluate -s <NEXUS_IQ_URL> -a <USERNAME>:<PASSWORD> -i test-nexusiq-bc166 /target/test-nexusiq-bc166-1.0-SNAPSHOT-deployable.jar

