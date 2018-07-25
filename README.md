
## Usage

```bash
docker-compose up
./gradlew bootRepackage
./gradlew showApmJarLocation
# copy printed jar location to $APM_JAR
java -jar -javaagent:$APM_JAR -Delastic.apm.service_name=my-cool-service -Delastic.apm.application_packages=org.example -Delastic.apm.server_url=http://localhost:8200  build/libs/elastic-custom-instrumentation-0.0.1-SNAPSHOT.jar
```