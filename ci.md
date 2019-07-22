### dsl
https://github.com/jenkinsci/job-dsl-plugin/wiki

### kubernetes plugin
https://github.com/jenkinsci/kubernetes-plugin

### centos ci pipeline
https://github.com/CentOS-PaaS-SIG/ci-pipeline

### contra
https://gitlab.cee.redhat.com/contra/downstream-rhel8-pipeline

### datagrepper
https://datagrepper.engineering.redhat.com/raw?rows_per_page=1&delta=127800&topic=/topic/VirtualTopic.eng.brew.task.closed&contains=ubi8-container

### check result in wave db
$ curl -d '{"decision_context":"osci_compose_gate","product_version":"rhel-8","subject":[{"item":"open-vm-tools-10.3.10-1.el8","type":"brew-build"}],"verbose":true}' -H "Content-Type: application/json" -X POST https://greenwave.engineering.redhat.com/api/v1.0/decision | jq . -M > result.json

### jenkins pipeline secrets
https://dev.to/pencillr/jenkins-pipelines-and-their-dirty-secrets-2

### init.groovy example
https://github.com/hayderimran7/useful-jenkins-groovy-init-scripts

### get token from secret
oc get sa/builder --template='{{range .secrets}}{{ .name  }} {{end}}' | xargs -n 1 oc get secret --template='{{ if .data.token  }}{{ .data.token  }}{{end}}' | head -n 1 | base64 -d -
