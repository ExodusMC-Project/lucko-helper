# Exodus Lucko Helper fork

## Maven

### Step 1
Visit your Maven `settings.xml` in your `.m2` directory.

### Step 2
Add the following profile

```xml
<profile>
  <id>Exodus</id>
  <repositories>
    <repository>
      <id>central</id>
      <url>https://repo1.maven.org/maven2</url>
    </repository>
    <repository>
      <id>github</id>
      <url>https://maven.pkg.github.com/ExodusMC-Project</url>
      <snapshots>
        <enabled>true</enabled>
      </snapshots>
    </repository>
  </repositories>
</profile>
```

### Step 3
Add the following server

```xml
<server>
  <id>github</id>
  <username>YOUR_GITHUB_USERNAME</username>
  <password>GITHUB_PERSONAL_ACCESS_TOKEN</password>
</server>
```

### Step 3
Add the following active profile

```xml
<activeProfile>Exodus</activeProfile>
```

### Step 4
Add repository declarators in your `pom.xml`

```xml
<repository>
    <id>ExodusMC</id>
    <url>https://maven.pkg.github.com/ExodusMC-Project/lucko-helper</url>
</repository>
```

## Gradle

### Step 1
Add a compileOnly server dependency under the `dependencies` section in your `build.gradle.kts`.

```kotlin
compileOnly("me.lucko:name:version")
```