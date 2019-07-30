## OpenShift Templates Development Guide
http://v1.uncontained.io/playbooks/fundamentals/template_development_guide.html

## jenkins image on openshift
https://docs.openshift.com/container-platform/3.11/using_images/other_images/jenkins.html

With the OpenShift Sync plug-in, the Jenkins image on Jenkins start-up searches within the project that it is running, or the projects specifically listed in the plug-in’s configuration for the following:

    Image streams that have the label role set to jenkins-slave.

    Image stream tags that have the annotation role set to jenkins-slave.

    ConfigMaps that have the label role set to jenkins-slave.

When it finds an image stream with the appropriate label, or image stream tag with the appropriate annotation, it generates the corresponding Kubernetes plug-in configuration so you can assign your Jenkins jobs to run in a pod running the container image provided by the image stream.

The name and image references of the image stream or image stream tag are mapped to the name and image fields in the Kubernetes plug-in pod template. You can control the label field of the Kubernetes plug-in pod template by setting an annotation on the image stream or image stream tag object with the key slave-label. Otherwise, the name is used as the label.


set JENKINS_JAVA_OVERRIDES to add more params for jenkins master, such as:

* -Duser.timezone=Asia/Shanghai to change timezone
