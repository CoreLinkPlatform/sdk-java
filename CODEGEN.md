# Java SDK generation

The Java SDK baseline is generated from the immutable CoreLink public contract using OpenAPI Generator `7.12.0`.

Pinned contract input:

- repository: `CoreLinkPlatform/api-contracts`
- tag: `v1.0.0-draft`
- commit: `5bdc07b80c8acbd0617b75e2d7ae3edd17f6324b`
- contract blob: `11cd7034f2b6dc736e23a4cf36242a34f0d637e5`

Baseline coordinates and runtime:

- Java: 17+
- groupId: `io.corelink`
- artifactId: `corelink-sdk`
- prerelease version: `0.1.0-SNAPSHOT`
- generator: `java`
- library: `native`
- API package: `io.corelink.sdk.api`
- model package: `io.corelink.sdk.model`

Generate into a temporary directory:

```sh
curl --fail --location \
  https://raw.githubusercontent.com/CoreLinkPlatform/api-contracts/5bdc07b80c8acbd0617b75e2d7ae3edd17f6324b/openapi/corelink-public-v1.yaml \
  --output /tmp/corelink-public-v1.yaml

curl --fail --location \
  https://repo1.maven.org/maven2/org/openapitools/openapi-generator-cli/7.12.0/openapi-generator-cli-7.12.0.jar \
  --output /tmp/openapi-generator-cli.jar

java -jar /tmp/openapi-generator-cli.jar generate \
  -i /tmp/corelink-public-v1.yaml \
  -g java \
  -o /tmp/corelink-java-sdk \
  --additional-properties=groupId=io.corelink,artifactId=corelink-sdk,artifactVersion=0.1.0-SNAPSHOT,invokerPackage=io.corelink.sdk,apiPackage=io.corelink.sdk.api,modelPackage=io.corelink.sdk.model,library=native,dateLibrary=java8,hideGenerationTimestamp=true \
  --global-property=apiDocs=false,modelDocs=false

cd /tmp/corelink-java-sdk
mvn -B -DskipTests package
```

CI executes this exact generation/build path. Generated sources are not a separate hand-maintained contract; all public model changes begin in `api-contracts`.

JAVA-02 owns authentication/error/retry/Spring ergonomics. JAVA-03 owns signed publication and stable/prerelease release channels.
