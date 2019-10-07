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

区分release or snapshot

```xml
<repositories>
  <repository>
    <id>luqian-maven-repo-snapshot</id>
    <url>https://raw.github.com/oahnus/luqian-maven/snapshot/repository</url>
  </repository>
  <repository>
    <id>luqian-maven-repo-release</id>
    <url>https://raw.github.com/oahnus/luqian-maven/release/repository</url>
  </repository>
</repositories>
```

## deploy

```shell
mvn clean deploy -Dmaven.test.skip -DaltDeploymentRepository=self-mvn-repo::default::file:C:\D\Projects\maven-repo\repository
```

C:\D\Projects\maven-repo\repository 为本地目录