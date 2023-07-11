# ColoredPrefix Wiki

The ColoredPrefix API is a Java library that provides an API to manage prefix entries for players.

## Installation

### Maven

Add the following repository to your `pom.xml`:

```xml
<repositories>
  <repository>
    <id>jubyte</id>
    <name>JuByte</name>
    <url>https://repo.jubyte.com/repository/jubyte/</url>
  </repository>
</repositories>
```

And then add the following dependency:

```xml
<dependency>
  <groupId>com.jubyte.coloredprefix</groupId>
  <artifactId>ColoredPrefixApi</artifactId>
  <version>2.8.3-RELEASE</version>
</dependency>
```

### Gradle

Add the following repository to your `build.gradle` file:

```groovy
repositories {
    maven {
        url "https://repo.jubyte.com/repository/jubyte/"
    }
}
```

And then add the following dependency:

```groovy
dependencies {
    implementation 'com.jubyte.coloredprefix:ColoredPrefixAPI:2.8.0-RELEASE'
}
```

## Usage

```java
import com.jubyte.coloredprefix.api.player.PrefixPlayerApi;

import java.util.UUID;

public class Example {

    public static void main(String[] args) {
        PrefixPlayerApi prefixPlayerApi = PrefixPlayerApi.getInstance();

        UUID playerUUID = UUID.randomUUID();
        String prefixName = "my_prefix";
        String prefixString = "&a[&bMyPrefix&a] ";

        // Get the prefix entry for the player with the given UUID
        PlayerPrefixEntry playerPrefix = prefixPlayerApi.getPlayerPrefix(playerUUID);

        // Set the prefix of the player with the given UUID
        prefixPlayerApi.setPlayerPrefix(playerUUID, prefixName, prefixString);

        // Reset the prefix of the player with the given UUID to the default value
        prefixPlayerApi.resetPlayerPrefix(playerUUID);
    }
}
```

## License

ColoredPrefix API is released under the [MIT License](https://opensource.org/licenses/MIT).
```xml
ColoredPrefix API is released under the MIT License.

MIT License

Copyright (c) 2023 JuByte

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
