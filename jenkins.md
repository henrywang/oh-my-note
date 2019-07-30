### list all installed plugins
Jenkins Script Console
```
Jenkins.instance.pluginManager.plugins.each{
  plugin -> 
      println ("${plugin.getShortName()}:${plugin.getVersion()}")
}
```

### init.groovy
https://github.com/AnalogJ/you-dont-know-jenkins-init

### job dsl gradle example
https://github.com/sheehan/job-dsl-gradle-example
