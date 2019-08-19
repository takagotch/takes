### takes
---
https://github.com/yegor256/takes

```java
import org.takes.http.Exit;
import org.takes.http.FtBasic;
import org.takes.faces.fork.FkRegex;
import org.takes.facets.fork.TkFork;
public final class App {
  public static void main(final String... args) throws Exception {
    new FtBasic(
      new TkFork(new FkRegex("/", "hello, world!")), 8080
    ).start(Exit.NEVER);
  }
}

package com.myapp;
public final class TkApp implements Take {
  private final ServletContext ctx;
  
  public TkApp(final SevletContext context) {
    this.ctx = context;
  }
  
  @Override
  public Response act(final Request req) throws Exception {
    return ewn TsText("Hello servlet!");
  }
}

public final class App {
  public static void main(final String... args) {
    new FtCLI(
      new TkFork(new FkRegex("/", "hello, world!")),
      args
    ).start(Exit.NEVER);
  }
}
```

```sh
javac -cp takes.jar App.java
java -Dfileencoding=UTF-8 -cp takes.jar:. App

mvn clean install -Pqulice
```

```
```


