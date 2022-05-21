** Работа с плагинами для Maven: SpotBugs и CheckStyle.

*** SpotBugs
1. Добавить зависимость в pom.xml
   <dependency>
   <groupId>com.github.spotbugs</groupId>
   <artifactId>spotbugs</artifactId>
   <version>4.7.0</version>
   </dependency>
2. Добавить плагин с командой check в фазе verify
   <plugin>
   <groupId>com.github.spotbugs</groupId>
   <artifactId>spotbugs-maven-plugin</artifactId>
   <version>4.7.0.0</version>
   <executions>
   <execution>
   <id>check</id>
   <phase>verify</phase>
   <goals>
   <goal>check</goal>
   </goals>
   </execution>
   </executions>
   </plugin>