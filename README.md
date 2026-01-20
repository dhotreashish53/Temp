<profiles>
  <profile>
    <id>ck-improve</id>
    <build>
      <plugins>

        <!-- OpenRewrite -->
        <plugin>
          <groupId>org.openrewrite.maven</groupId>
          <artifactId>rewrite-maven-plugin</artifactId>
          <version>5.12.0</version>
          <configuration>
            <activeRecipes>
              <recipe>org.openrewrite.java.migrate.UpgradeToJava17</recipe>
              <recipe>org.openrewrite.java.cleanup.Cleanup</recipe>
              <recipe>org.openrewrite.java.RemoveUnusedImports</recipe>
              <recipe>org.openrewrite.java.format.AutoFormat</recipe>
            </activeRecipes>
          </configuration>
        </plugin>

      </plugins>
    </build>
  </profile>
</profiles>
