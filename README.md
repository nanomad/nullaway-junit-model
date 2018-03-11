# JUnit Library Model for Uber's NullAway

This library add some support to [NullAway](https://github.com/uber/NullAway) for some JUnit methods like
 - `org.junit.assert.Assert.assertNotNull(java.lang.Object)`
 - `org.junit.assert.Assert.assertNotNull(java.lang.String, java.lang.Object)`
 
## How to use
1. Add JitPack maven repo to your `pom.xml` file
    ```xml
    <repositories>
        <repository>
            <id>jitpack.io</id>
            <url>https://jitpack.io</url>
        </repository>
    </repositories>
    ```
2. Add the this maven artifact to the annotation processor path
    ```xml
    <build>
        <plugins>
        ...
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-compiler-plugin</artifactId>
                <version>3.7.0</version>
                <configuration>
                    ....
                    <annotationProcessorPaths>
                        <path>
                            <groupId>com.uber.nullaway</groupId>
                            <artifactId>nullaway</artifactId>
                            <version>0.3.0</version>
                        </path>
                        <path>
                            <groupId>com.github.nanomad</groupId>
                            <artifactId>nullaway-junit-model</artifactId>
                            <version>LATEST</version>
                        </path>
                        ....
                    </annotationProcessorPaths>
                </configuration>
                ...
            </plugin>
        </plugins>
    </build>
    ```
