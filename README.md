参考文档:  
[nacos-docker/README_ZH](https://github.com/nacos-group/nacos-docker/blob/ac214ac776821dae6a76a7a1ace34eb3081026b3/README_ZH.md)

启动后 nacos 容器错误日志:

```log
2023-11-29 16:59:17,170 ERROR Application run failed
2023-11-29T08:59:17.170451585Z 
2023-11-29T08:59:17.170454685Z org.springframework.beans.factory.UnsatisfiedDependencyException: Error creating bean with name 'memoryMonitor' defined in URL [jar:file:/home/nacos/target/nacos-server.jar!/BOOT-INF/lib/nacos-config-2.2.3.jar!/com/alibaba/nacos/config/server/monitor/MemoryMonitor.class]: Unsatisfied dependency expressed through constructor parameter 0; nested exception is org.springframework.beans.factory.UnsatisfiedDependencyException: Error creating bean with name 'asyncNotifyService': Unsatisfied dependency expressed through field 'dumpService'; nested exception is org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'externalDumpService': Invocation of init method failed; nested exception is ErrCode:500, ErrMsg:Nacos Server did not start because dumpservice bean construction failure :
2023-11-29T08:59:17.170457645Z No DataSource set
2023-11-29T08:59:17.170459214Z 	at org.springframework.beans.factory.support.ConstructorResolver.createArgumentArray(ConstructorResolver.java:800)
2023-11-29T08:59:17.170461264Z 	at org.springframework.beans.factory.support.ConstructorResolver.autowireConstructor(ConstructorResolver.java:229)
2023-11-29T08:59:17.170462914Z 	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.autowireConstructor(AbstractAutowireCapableBeanFactory.java:1372)
2023-11-29T08:59:17.170464574Z 	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBeanInstance(AbstractAutowireCapableBeanFactory.java:1222)
2023-11-29T08:59:17.170466304Z 	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:582)
2023-11-29T08:59:17.170467904Z 	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:542)
2023-11-29T08:59:17.170469504Z 	at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:335)
2023-11-29T08:59:17.170471094Z 	at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:234)
2023-11-29T08:59:17.170472804Z 	at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:333)
2023-11-29T08:59:17.170475324Z 	at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:208)
2023-11-29T08:59:17.170476954Z 	at org.springframework.beans.factory.support.DefaultListableBeanFactory.preInstantiateSingletons(DefaultListableBeanFactory.java:955)
2023-11-29T08:59:17.170478584Z 	at org.springframework.context.support.AbstractApplicationContext.finishBeanFactoryInitialization(AbstractApplicationContext.java:918)
2023-11-29T08:59:17.170493344Z 	at org.springframework.context.support.AbstractApplicationContext.refresh(AbstractApplicationContext.java:583)
2023-11-29T08:59:17.170495264Z 	at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.refresh(ServletWebServerApplicationContext.java:145)
2023-11-29T08:59:17.170518774Z 	at org.springframework.boot.SpringApplication.refresh(SpringApplication.java:745)
2023-11-29T08:59:17.170520804Z 	at org.springframework.boot.SpringApplication.refreshContext(SpringApplication.java:423)
2023-11-29T08:59:17.170522444Z 	at org.springframework.boot.SpringApplication.run(SpringApplication.java:307)
2023-11-29T08:59:17.170524004Z 	at org.springframework.boot.SpringApplication.run(SpringApplication.java:1317)
2023-11-29T08:59:17.170525814Z 	at org.springframework.boot.SpringApplication.run(SpringApplication.java:1306)
2023-11-29T08:59:17.170527434Z 	at com.alibaba.nacos.Nacos.main(Nacos.java:35)
2023-11-29T08:59:17.170528964Z 	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2023-11-29T08:59:17.170530504Z 	at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
2023-11-29T08:59:17.170532024Z 	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2023-11-29T08:59:17.170533614Z 	at java.lang.reflect.Method.invoke(Method.java:498)
2023-11-29T08:59:17.170535114Z 	at org.springframework.boot.loader.MainMethodRunner.run(MainMethodRunner.java:49)
2023-11-29T08:59:17.170536704Z 	at org.springframework.boot.loader.Launcher.launch(Launcher.java:108)
2023-11-29T08:59:17.170538204Z 	at org.springframework.boot.loader.Launcher.launch(Launcher.java:58)
2023-11-29T08:59:17.170539704Z 	at org.springframework.boot.loader.PropertiesLauncher.main(PropertiesLauncher.java:467)
2023-11-29T08:59:17.170541644Z Caused by: org.springframework.beans.factory.UnsatisfiedDependencyException: Error creating bean with name 'asyncNotifyService': Unsatisfied dependency expressed through field 'dumpService'; nested exception is org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'externalDumpService': Invocation of init method failed; nested exception is ErrCode:500, ErrMsg:Nacos Server did not start because dumpservice bean construction failure :
2023-11-29T08:59:17.170543674Z No DataSource set
2023-11-29T08:59:17.170545164Z 	at org.springframework.beans.factory.annotation.AutowiredAnnotationBeanPostProcessor$AutowiredFieldElement.resolveFieldValue(AutowiredAnnotationBeanPostProcessor.java:660)
2023-11-29T08:59:17.170546824Z 	at org.springframework.beans.factory.annotation.AutowiredAnnotationBeanPostProcessor$AutowiredFieldElement.inject(AutowiredAnnotationBeanPostProcessor.java:640)
2023-11-29T08:59:17.170548444Z 	at org.springframework.beans.factory.annotation.InjectionMetadata.inject(InjectionMetadata.java:119)
2023-11-29T08:59:17.170550004Z 	at org.springframework.beans.factory.annotation.AutowiredAnnotationBeanPostProcessor.postProcessProperties(AutowiredAnnotationBeanPostProcessor.java:399)
2023-11-29T08:59:17.170553883Z 	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.populateBean(AbstractAutowireCapableBeanFactory.java:1431)
2023-11-29T08:59:17.170555543Z 	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:619)
2023-11-29T08:59:17.170557213Z 	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:542)
2023-11-29T08:59:17.170558953Z 	at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:335)
2023-11-29T08:59:17.170560633Z 	at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:234)
2023-11-29T08:59:17.170562253Z 	at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:333)
2023-11-29T08:59:17.170563803Z 	at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:208)
2023-11-29T08:59:17.170565413Z 	at org.springframework.beans.factory.config.DependencyDescriptor.resolveCandidate(DependencyDescriptor.java:276)
2023-11-29T08:59:17.170566993Z 	at org.springframework.beans.factory.support.DefaultListableBeanFactory.doResolveDependency(DefaultListableBeanFactory.java:1391)
2023-11-29T08:59:17.170568593Z 	at org.springframework.beans.factory.support.DefaultListableBeanFactory.resolveDependency(DefaultListableBeanFactory.java:1311)
2023-11-29T08:59:17.170570463Z 	at org.springframework.beans.factory.support.ConstructorResolver.resolveAutowiredArgument(ConstructorResolver.java:887)
2023-11-29T08:59:17.170572093Z 	at org.springframework.beans.factory.support.ConstructorResolver.createArgumentArray(ConstructorResolver.java:791)
2023-11-29T08:59:17.170573653Z 	... 27 common frames omitted
2023-11-29T08:59:17.170575153Z Caused by: org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'externalDumpService': Invocation of init method failed; nested exception is ErrCode:500, ErrMsg:Nacos Server did not start because dumpservice bean construction failure :
2023-11-29T08:59:17.170576903Z No DataSource set
2023-11-29T08:59:17.170578353Z 	at org.springframework.beans.factory.annotation.InitDestroyAnnotationBeanPostProcessor.postProcessBeforeInitialization(InitDestroyAnnotationBeanPostProcessor.java:160)
2023-11-29T08:59:17.170579993Z 	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.applyBeanPostProcessorsBeforeInitialization(AbstractAutowireCapableBeanFactory.java:440)
2023-11-29T08:59:17.170581623Z 	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.initializeBean(AbstractAutowireCapableBeanFactory.java:1796)
2023-11-29T08:59:17.170583243Z 	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:620)
2023-11-29T08:59:17.170584823Z 	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:542)
2023-11-29T08:59:17.170586403Z 	at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:335)
2023-11-29T08:59:17.170589633Z 	at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:234)
2023-11-29T08:59:17.170591263Z 	at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:333)
2023-11-29T08:59:17.170592863Z 	at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:208)
2023-11-29T08:59:17.170594403Z 	at org.springframework.beans.factory.config.DependencyDescriptor.resolveCandidate(DependencyDescriptor.java:276)
2023-11-29T08:59:17.170596093Z 	at org.springframework.beans.factory.support.DefaultListableBeanFactory.doResolveDependency(DefaultListableBeanFactory.java:1391)
2023-11-29T08:59:17.170597693Z 	at org.springframework.beans.factory.support.DefaultListableBeanFactory.resolveDependency(DefaultListableBeanFactory.java:1311)
2023-11-29T08:59:17.170599413Z 	at org.springframework.beans.factory.annotation.AutowiredAnnotationBeanPostProcessor$AutowiredFieldElement.resolveFieldValue(AutowiredAnnotationBeanPostProcessor.java:657)
2023-11-29T08:59:17.170601043Z 	... 42 common frames omitted
2023-11-29T08:59:17.170602503Z Caused by: com.alibaba.nacos.api.exception.NacosException: Nacos Server did not start because dumpservice bean construction failure :
2023-11-29T08:59:17.170604083Z No DataSource set
2023-11-29T08:59:17.170605503Z 	at com.alibaba.nacos.config.server.service.dump.DumpService.dumpOperate(DumpService.java:260)
2023-11-29T08:59:17.170607033Z 	at com.alibaba.nacos.config.server.service.dump.ExternalDumpService.init(ExternalDumpService.java:61)
2023-11-29T08:59:17.170608673Z 	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2023-11-29T08:59:17.170610213Z 	at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
2023-11-29T08:59:17.170611723Z 	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2023-11-29T08:59:17.170613283Z 	at java.lang.reflect.Method.invoke(Method.java:498)
2023-11-29T08:59:17.170614793Z 	at org.springframework.beans.factory.annotation.InitDestroyAnnotationBeanPostProcessor$LifecycleElement.invoke(InitDestroyAnnotationBeanPostProcessor.java:389)
2023-11-29T08:59:17.170616453Z 	at org.springframework.beans.factory.annotation.InitDestroyAnnotationBeanPostProcessor$LifecycleMetadata.invokeInitMethods(InitDestroyAnnotationBeanPostProcessor.java:333)
2023-11-29T08:59:17.170618093Z 	at org.springframework.beans.factory.annotation.InitDestroyAnnotationBeanPostProcessor.postProcessBeforeInitialization(InitDestroyAnnotationBeanPostProcessor.java:157)
2023-11-29T08:59:17.170619693Z 	... 54 common frames omitted
2023-11-29T08:59:17.170621283Z Caused by: java.lang.IllegalStateException: No DataSource set
2023-11-29T08:59:17.170622863Z 	at org.springframework.util.Assert.state(Assert.java:76)
2023-11-29T08:59:17.170624353Z 	at org.springframework.jdbc.support.JdbcAccessor.obtainDataSource(JdbcAccessor.java:86)
2023-11-29T08:59:17.170627833Z 	at org.springframework.jdbc.core.JdbcTemplate.execute(JdbcTemplate.java:376)
2023-11-29T08:59:17.170631013Z 	at org.springframework.jdbc.core.JdbcTemplate.query(JdbcTemplate.java:465)
2023-11-29T08:59:17.170634123Z 	at org.springframework.jdbc.core.JdbcTemplate.query(JdbcTemplate.java:475)
2023-11-29T08:59:17.170637093Z 	at org.springframework.jdbc.core.JdbcTemplate.queryForObject(JdbcTemplate.java:508)
2023-11-29T08:59:17.170640043Z 	at org.springframework.jdbc.core.JdbcTemplate.queryForObject(JdbcTemplate.java:515)
2023-11-29T08:59:17.170643283Z 	at com.alibaba.nacos.config.server.service.repository.extrnal.ExternalConfigInfoPersistServiceImpl.findConfigMaxId(ExternalConfigInfoPersistServiceImpl.java:632)
2023-11-29T08:59:17.170646272Z 	at com.alibaba.nacos.config.server.service.dump.processor.DumpAllProcessor.process(DumpAllProcessor.java:51)
2023-11-29T08:59:17.170647892Z 	at com.alibaba.nacos.config.server.service.dump.DumpService.dumpConfigInfo(DumpService.java:317)
2023-11-29T08:59:17.170649462Z 	at com.alibaba.nacos.config.server.service.dump.DumpService.dumpOperate(DumpService.java:230)
2023-11-29T08:59:17.170651092Z 	... 62 common frames omitted
2023-11-29T08:59:17.172166326Z 2023-11-29 16:59:17,172 WARN [ThreadPoolManager] Start destroying ThreadPool
```

## 环境

docker

```
Client: Docker Engine - Community
 Version:           25.0.0-beta.1
  Version:          25.0.0-beta.1
  API version:      1.44 (minimum version 1.12)
  Go version:       go1.21.3
  Git commit:       6af7d6e
  Built:            Mon Nov 13 16:49:38 2023
  OS/Arch:          linux/amd64
  Experimental:     false
 containerd:
  Version:          1.6.25
  GitCommit:        d8f198a4ed8892c764191ef7b3b06d8a2eeb5c7f
 runc:
  Version:          1.1.10
  GitCommit:        v1.1.10-0-g18a0cb0
 docker-init:
  Version:          0.19.0
  GitCommit:        de40ad0
```

docker compose

```
Docker Compose version v2.23.0
```

OS

```
Linux ll 5.15.133.1-microsoft-standard-WSL2 #1 SMP Thu Oct 5 21:02:42 UTC 2023 x86_64 x86_64 x86_64 GNU/Linux
```
