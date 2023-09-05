mvn quarkus:dev -Dquarkus.profile=prod

result in

```
[INFO] [stdout] __  ____  __  _____   ___  __ ____  ______ 
[INFO] [stdout]  --/ __ \/ / / / _ | / _ \/ //_/ / / / __/ 
[INFO] [stdout]  -/ /_/ / /_/ / __ |/ , _/ ,< / /_/ /\ \   
[INFO] [stdout] --\___\_\____/_/ |_/_/|_/_/|_|\____/___/   
[INFO] [stdout] 2023-09-05 15:25:30,048 ERROR [io.qua.run.Application] (Quarkus Main Thread) Failed to start application (with profile [prod]): java.lang.RuntimeException: Failed to start quarkus
[INFO] [stdout]         at io.quarkus.runner.ApplicationImpl.doStart(Unknown Source)
[INFO] [stdout]         at io.quarkus.runtime.Application.start(Application.java:101)
[INFO] [stdout]         at io.quarkus.runtime.ApplicationLifecycleManager.run(ApplicationLifecycleManager.java:111)
[INFO] [stdout]         at io.quarkus.runtime.Quarkus.run(Quarkus.java:71)
[INFO] [stdout]         at io.quarkus.runtime.Quarkus.run(Quarkus.java:44)
[INFO] [stdout]         at io.quarkus.runtime.Quarkus.run(Quarkus.java:124)
[INFO] [stdout]         at io.quarkus.runner.GeneratedMain.main(Unknown Source)
[INFO] [stdout]         at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
[INFO] [stdout]         at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
[INFO] [stdout]         at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
[INFO] [stdout]         at java.base/java.lang.reflect.Method.invoke(Method.java:568)
[INFO] [stdout]         at io.quarkus.runner.bootstrap.StartupActionImpl$1.run(StartupActionImpl.java:104)
[INFO] [stdout]         at java.base/java.lang.Thread.run(Thread.java:833)
[INFO] [stdout] Caused by: jakarta.enterprise.inject.CreationException: Error creating synthetic bean [803bdbdea0e23416b5b2639797778edfee1ac6aa]: jakarta.enterprise.inject.UnsatisfiedResolutionException: No datasource present
[INFO] [stdout]         at io.quarkus.flyway.runtime.FlywayContainer_803bdbdea0e23416b5b2639797778edfee1ac6aa_Synthetic_Bean.doCreate(Unknown Source)
[INFO] [stdout]         at io.quarkus.flyway.runtime.FlywayContainer_803bdbdea0e23416b5b2639797778edfee1ac6aa_Synthetic_Bean.create(Unknown Source)
[INFO] [stdout]         at io.quarkus.flyway.runtime.FlywayContainer_803bdbdea0e23416b5b2639797778edfee1ac6aa_Synthetic_Bean.create(Unknown Source)
[INFO] [stdout]         at io.quarkus.arc.impl.AbstractSharedContext.createInstanceHandle(AbstractSharedContext.java:113)
[INFO] [stdout]         at io.quarkus.arc.impl.AbstractSharedContext$1.get(AbstractSharedContext.java:37)
[INFO] [stdout]         at io.quarkus.arc.impl.AbstractSharedContext$1.get(AbstractSharedContext.java:34)
[INFO] [stdout]         at io.quarkus.arc.impl.LazyValue.get(LazyValue.java:32)
[INFO] [stdout]         at io.quarkus.arc.impl.ComputingCache.computeIfAbsent(ComputingCache.java:69)
[INFO] [stdout]         at io.quarkus.arc.impl.AbstractSharedContext.get(AbstractSharedContext.java:34)
[INFO] [stdout]         at io.quarkus.flyway.runtime.FlywayContainer_803bdbdea0e23416b5b2639797778edfee1ac6aa_Synthetic_Bean.get(Unknown Source)
[INFO] [stdout]         at io.quarkus.flyway.runtime.FlywayContainer_803bdbdea0e23416b5b2639797778edfee1ac6aa_Synthetic_Bean.get(Unknown Source)
[INFO] [stdout]         at io.quarkus.arc.impl.Instances$3.get(Instances.java:132)
[INFO] [stdout]         at io.quarkus.arc.impl.LazyValue.get(LazyValue.java:32)
[INFO] [stdout]         at io.quarkus.arc.impl.LazyInstanceHandle.instanceInternal(LazyInstanceHandle.java:32)
[INFO] [stdout]         at io.quarkus.arc.impl.AbstractInstanceHandle.get(AbstractInstanceHandle.java:46)
[INFO] [stdout]         at io.quarkus.flyway.runtime.FlywayRecorder.doStartActions(FlywayRecorder.java:96)
[INFO] [stdout]         at io.quarkus.deployment.steps.FlywayProcessor$startActions2035800939.deploy_0(Unknown Source)
[INFO] [stdout]         at io.quarkus.deployment.steps.FlywayProcessor$startActions2035800939.deploy(Unknown Source)
[INFO] [stdout]         ... 13 more
[INFO] [stdout] Caused by: jakarta.enterprise.inject.UnsatisfiedResolutionException: No datasource present
[INFO] [stdout]         at io.quarkus.flyway.runtime.FlywayRecorder$1.apply(FlywayRecorder.java:62)
[INFO] [stdout]         at io.quarkus.flyway.runtime.FlywayRecorder$1.apply(FlywayRecorder.java:57)
[INFO] [stdout]         at io.quarkus.flyway.runtime.FlywayContainer_803bdbdea0e23416b5b2639797778edfee1ac6aa_Synthetic_Bean.createSynthetic(Unknown Source)
[INFO] [stdout]         ... 31 more

```
