maven-repo
==========

My public maven repository

## Usage
For using on the clean maven installation you may use archetypeRepository
key to specify this repository location, as follows:

    mvn archetype:generate -DarchetypeGroupId=com.truward.maven.archetypes -DarchetypeArtifactId=spring-web-app -DarchetypeVersion=1.0 -DgroupId=org.gnu.web -DartifactId=oximuron -Dversion=1.0-SNAPSHOT -DarchetypeRepository=https://github.com/avshabanov/maven-repo/raw/master/libs-release

    mvn archetype:generate -DarchetypeGroupId=com.truward.maven.archetypes -DarchetypeArtifactId=spring-sec-web-app -DarchetypeVersion=1.0 -DgroupId=org.gnu.web -DartifactId=oximuron-sec -Dversion=1.0-SNAPSHOT -DarchetypeRepository=https://github.com/avshabanov/maven-repo/raw/master/libs-release

    mvn archetype:generate -DarchetypeGroupId=com.truward.maven.archetypes -DarchetypeArtifactId=spring-lib -DarchetypeVersion=1.0 -DgroupId=org.sample -DartifactId=sample-service -Dversion=1.0-SNAPSHOT -DarchetypeRepository=https://github.com/avshabanov/maven-repo/raw/master/libs-release

### Simple App

    mvn archetype:generate -DarchetypeGroupId=com.truward.maven.archetypes -DarchetypeArtifactId=simple-app -DarchetypeVersion=1.0 -DgroupId=org.gnu -DartifactId=oximuron -Dversion=1.0-SNAPSHOT -DarchetypeRepository=https://github.com/avshabanov/maven-repo/raw/master/libs-release

run: mvn exec:java -Dexec.mainClass=org.gnu.App


### Spring Web App

    mvn archetype:generate -DarchetypeGroupId=com.truward.maven.archetypes -DarchetypeArtifactId=spring-web-app -DarchetypeVersion=1.1 -DgroupId=org.gnu.web -DartifactId=oximuron -Dversion=1.0-SNAPSHOT -DarchetypeRepository=https://github.com/avshabanov/maven-repo/raw/master/libs-release


### Spring Secured Web App

    mvn archetype:generate -DarchetypeGroupId=com.truward.maven.archetypes -DarchetypeArtifactId=spring-sec-web-app -DarchetypeVersion=1.0 -DgroupId=org.gnu.web -DartifactId=oximuron -Dversion=1.0-SNAPSHOT -DarchetypeRepository=https://github.com/avshabanov/maven-repo/raw/master/libs-release


### Spring Service

    mvn archetype:generate -DarchetypeGroupId=com.truward.maven.archetypes -DarchetypeArtifactId=spring-lib -DarchetypeVersion=1.1 -DgroupId=com.alexshabanov.proxytest -DartifactId=proxy-test -Dversion=1.0-SNAPSHOT -DarchetypeRepository=https://github.com/avshabanov/maven-repo/raw/master/libs-release 

## Repositories location

*RELEASES:* https://github.com/avshabanov/maven-repo/raw/master/libs-release

*SNAPSHOTS:* https://github.com/avshabanov/maven-repo/raw/master/libs-snapshot


## Adding dependecies to pom.xml
The sample configuration section in the pom.xml may look as follows:

        <repositories>
            <repository>
                <snapshots>
                    <enabled>false</enabled>
                </snapshots>
                <id>central</id>
                <name>libs-release</name>
                <url>https://github.com/avshabanov/maven-repo/raw/master/libs-release</url>
            </repository>
            <repository>
                <snapshots/>
                <id>snapshots</id>
                <name>libs-snapshot</name>
                <url>https://github.com/avshabanov/maven-repo/raw/master/libs-snapshot</url>
            </repository>
        </repositories>



