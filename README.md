Archived as it is no longer in use and the build of palladio has migrated to only using default maven plugins.

# Palladio-Build-MavenJavaDocPlugin

This plugin is a fork of the [tycho-document-bundle-plugin](https://www.eclipse.org/tycho/sitedocs/tycho-extras/tycho-document-bundle-plugin/plugin-info.html). In contrast to the original plugin, this fork provides flags to consider sources of dependencies and the project itself. The default behavior is to only consider sources of dependencies.

To use the plugin, add the following snippet to your POM file (replace `1.2.3` with the most recent version). Most probably, you want to specify executions and parameters according to the [official plugin documentation](https://www.eclipse.org/tycho/sitedocs/tycho-extras/tycho-document-bundle-plugin/javadoc-mojo.html).
```
<plugin>
  <groupId>org.palladiosimulator</groupId>
  <artifactId>tycho-document-bundle-plugin</artifactId>
  <version>1.2.3</version>
</plugin>
```

We introduce the following parameters:
| Parameter                       | Type    | Default Value  | Required | Meaning |
| ------------------------------- | ------- | -------------- | -------- | ------------ |
| considerSourcesOfCurrentProject | boolean | false          | no       | The JavaDoc generation shall consider the source code of the current project. |
| considerSourcesOfDependencies   | boolean | true           | no       | The JavaDoc generation shall consider the source code of all dependencies.    |
