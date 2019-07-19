### list all installed plugins
Jenkins Script Console
```
Jenkins.instance.pluginManager.plugins.each{
  plugin -> 
      println ("${plugin.getShortName()}:${plugin.getVersion()}")
}
```
