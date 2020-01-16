https://spring.io/guides

@SpringBootApplication

# maven/gradle

maven only now,

`./gradlew build`

`./gradlew bootRun`

```groovy
buildscript {
    repositories {
        mavenCentral()
    }
    dependencies {
        classpath("org.springframework.boot:spring-boot-gradle-plugin:2.2.1.RELEASE")
    }
}
```

`java -jar build/libs/XXXX.jar`

---

`./mvnw clean package`

`./mvnw spring-boot:run`

```xml
<build>
    <plugins>
        <plugin>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-maven-plugin</artifactId>
        </plugin>
    </plugins>
</build>
```

`java -jar target/XXXX.jar`

# Building a RESTful Web Service

`src/main/java/com/example/restservice`

@RestController

@GetMapping("/greeting")

@RequestParam


```xml
<dependency>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-web</artifactId>
</dependency>
<dependency>
  <groupId>com.jayway.jsonpath</groupId>
  <artifactId>json-path</artifactId>
  <scope>test</scope>
</dependency>
```

# Scheduling Tasks

`src/main/java/hello`

@EnableScheduling

@Component

@Scheduled(fixedRate = 5000)

```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter</artifactId>
</dependency>
```

# Consuming a RESTful Web Service

`src/main/java/com/example/consumingrest`

@JsonIgnoreProperties(ignoreUnknown = true)

@Override

@Bean

@Override

```xml
<dependency>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-web</artifactId>
</dependency>

<dependency>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-test</artifactId>
	<scope>test</scope>
</dependency>
```

# Accessing Relational Data using JDBC with Spring

`src/main/java/com/example/relationaldataaccess`

@Autowired

@Override

```xml
<dependency>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-data-jdbc</artifactId>
</dependency>

<dependency>
	<groupId>com.h2database</groupId>
	<artifactId>h2</artifactId>
	<scope>runtime</scope>
</dependency>
```

# Uploading Files

`src/main/java/com/example/uploadingfiles`

`src/main/resources/application.properties`

`src/main/resources/templates/uploadForm.html`

@Autowired

@Bean

@ConfigurationProperties("storage")

@Controller

@EnableConfigurationProperties(StorageProperties.class)

@ExceptionHandler(StorageFileNotFoundException.class)

@GetMapping("/")

@GetMapping("/files/{filename:.+}")

@Override

@PathVariable String filename) {

@PostMapping("/")

@RequestParam("file") MultipartFile file,

@ResponseBody

@Service

@SpringBootApplication
