# maven使用



```bash
# 本地启动服务
mvn spring-boot:run

```





repackage的注释说明:

Repackage existing JAR and WAR archives so that they can be executed from the command line using `java -jar`. With `layout=NONE` can also be used simply to package a JAR with nested dependencies \(and no main class, so not executable\).



repackage 依赖于package的输出.

```bash
mvn package spring-boot:repackage
```

