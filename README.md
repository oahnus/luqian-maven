# 个人Maven库

[toc]

## 使用方法

```xml
<project>
  ...
  <repositories>
    <repository>
      <id>luqian-maven-repo</id>
      <url>https://raw.github.com/oahnus/luqian-maven/master/repository</url>
    </repository>
  </repositories>

  <dependency>
    <artifactId>luqian-common</artifactId>
    <groupId>com.github.oahnus</groupId>
    <version>x.x.x</version>
  </dependency>
</project>
```

## deploy

在项目文件目录下运行
```shell
mvn clean deploy -Dmaven.test.skip -DaltDeploymentRepository=self-mvn-repo::default::file:C:\D\Projects\maven-repo\repository
```
> C:\D\Projects\maven-repo\repository 为本地目录
