# async-demo

https://github.com/spring-guides/gs-async-method


With `ThreadPoolTaskExecutor` pool size set to `3`, and service delay set to `1s`,
you get a separate thread for each call, and the total elapsed time is still slightly over `2s`.



```
18:55:35.586 [main] INFO  c.d.async.AsyncDemoApplicationTests - Started AsyncDemoApplicationTests in 2.887 seconds (JVM running for 3.725)
18:55:35.601 [GithubLookup-2] INFO  com.demo.async.GitHubLookupService - Looking up CloudFoundry
18:55:35.601 [GithubLookup-3] INFO  com.demo.async.GitHubLookupService - Looking up Spring-Projects
18:55:35.601 [GithubLookup-1] INFO  com.demo.async.GitHubLookupService - Looking up PivotalSoftware
18:55:38.312 [main] INFO  com.demo.async.AppRunner - Elapsed time: 2723
18:55:38.312 [main] INFO  com.demo.async.AppRunner - --> User [name=Pivotal Software, Inc., blog=http://pivotal.io]
18:55:38.312 [main] INFO  com.demo.async.AppRunner - --> User [name=Cloud Foundry, blog=https://www.cloudfoundry.org/]
18:55:38.312 [main] INFO  com.demo.async.AppRunner - --> User [name=Spring, blog=http://spring.io/projects]
```