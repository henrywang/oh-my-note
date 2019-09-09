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

### jenkins on openshift with openstack cloud plugin

Openshift route works on port 80 and 443 only due to haproxy. So port 50000 cannot be exposed outiside, that means openstack cloud plugin cannot work on JNLP if jenkins is on openshift. If the jslave container located in the same project as jenkins master located, this issue does not impact this scenario because things work on internal and no route needed.

## UMB

### rtt.ci
https://datagrepper.engineering.redhat.com/raw?topic=/topic/VirtualTopic.eng.rtt.ci&rows_per_page=1&delta=2592000&contains=RHEL-7
