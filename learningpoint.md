# if vs code refuses to give you the version of springboot you want,
ignore it, you can always change it after building it

to create a multimodule spring boot in  vscode do this

generate the parent spring booth

modify  the pom to look like this🧮 
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
	<modelVersion>4.0.0</modelVersion>
    <parent>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-parent</artifactId>
        <version>2.4.2</version>
        <relativePath/> <!-- lookup parent from repository -->
    </parent>
    <groupId>
        dayo.basics
    </groupId>
    <artifactId>root</artifactId>
    <version>0.0.1-SNAPSHOT</version>
    <packaging>pom</packaging>
	<modules>
    	<module>client</module>
    	<module>service</module>
    </modules>
</project>


the most important thing about the above snippet is 🧮 

```
  <packaging>pom</packaging>
	<modules>
    	<module>client</module>
    	<module>service</module>
    </modules>

```

create two directories named  after the above🧮 
  mkdir client
  mkdir service

client and service

enter each diretory🧮 
  cd client
  cd ../service


Run the Maven command in each directory

  mvn archetype:generate -DgroupId=dayo.basics -DartifactId=client -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false

  
  mvn archetype:generate -DgroupId=dayo.basics -DartifactId=service -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false


  with thier pom files we can always rearrange how they work
  
