[![noswpatv3](http://zoobab.wdfiles.com/local--files/start/noupcv3.jpg)](https://ffii.org/donate-now-to-save-europe-from-software-patents-says-ffii/)
Docker container with Openshift client, helm and kubectl
========================================================

A merge of 2 Dockerfiles:

* https://github.com/dtzar/helm-kubectl/blob/master/Dockerfile
* https://github.com/zoobab/openshift-client/blob/master/Dockerfile

Usage examples
==============

```
$ docker run -it zoobab/openshift-client-helm-kubectl oc version
oc v3.11.0+0cbc58b
kubernetes v1.11.0+d4cacc0
features: Basic-Auth GSSAPI Kerberos SPNEGO
```

```
$ docker run -it -e TILLER_NAMESPACE=kong -v $PWD/conf.d/:/config -v ~/.kube:/root/.kube dtzar/helm-kubectl:2.9.1 helm ls
NAME                    REVISION        UPDATED                         STATUS          CHART           NAMESPACE
tinseled-dolphin        2               Tue Apr 16 11:37:53 2019        DEPLOYED        kong-0.9.18     kong
```
