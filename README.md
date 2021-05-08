## Goal

* Integration Test using specify *.feature 

  = continuous scenario testing

  ex) KeyValueDtoScenario.feature



## Spec

* Java 11

* Spring Boot 2.4.5

* Junit 5

* Gradle



## Usage

### Run only specify scenario

* If both methods are activated in DemoRunner, 
  
  an error occurs due to **data duplication**. 
  
  So, if you want to use that command line, 

  you need to enable **only one** in DemoRunner and **comment out the rest**.

``` 
./gradlew test --tests DemoRunner -Dkarate.options=classpath:karate/demo/get.feature
./gradlew test --tests DemoRunner -Dkarate.options=classpath:karate/demo/post.feature
./gradlew test --tests DemoRunner -Dkarate.options="--tags ~@CreateValue classpath:karate/demo/post.feature"
```

### @RegressionTest && Parallel

```
./gradlew test --tests KarateTests
```



## Reference

* [karate github](https://github.com/intuit/karate)

* [hello-karate](https://github.com/Sdaas/hello-karate)
