```sh
servingInfo:
  ...
  namedCertificates:
  - certFile: custom.crt
    keyFile: custom.key
    names:
    - "customhost.com"
    - "api.customhost.com"
    - "console.customhost.com"
  - certFile: wildcard.crt
    keyFile: wildcard.key
    names:
    - "*.wildcardhost.com"
  ...
 ```


```sh
openshift_master_overwrite_named_certificates=true
openshift_master_named_certificates=[{"certfile": "/path/to/custom1.crt", "keyfile": "/path/to/custom1.key", "names": ["public-master-host.com"]}]
```

```sh

ansible-playbook 
    /usr/share/ansible/openshift-ansible/playbooks/byo/openshift-cluster/redeploy-master-certificates.yml
```
