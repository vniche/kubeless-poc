kubeless-poc
=========

An POC of how to run Kubeless in a raw local Kubernetes.

Design
------------

[Serverless](https://serverless.com/learn/overview)

What ‘serverless’ really means is that, as a developer you don’t have to think about those servers. You just focus on code.

Requirements
------------

- [Node LTS](https://nodejs.org/en/download/)
- [Serverless](https://github.com/serverless/serverless/)
- [Kubeless](https://github.com/serverless/serverless-kubeless)

This project was bootstrapped via:

```bash
$ mkdir my-project
$ cd my-project
$ serverless create --template kubeless-nodejs
```

Manifest Parameters
--------------

This serverless manifest lets user provide the following parameter:

### K8S_NAMESPACE
```bash
$ kubectl create ns my-namespace
$ K8S_NAMESPACE=my-namespace sls deploy -v
```

Dependencies
------------

[lodash](https://lodash.com/) is used here for dependencies usage reference.

Examples
----------------

#### Deploy
```bash
$ K8S_NAMESPACE=my-namespace sls deploy -v
```

#### Remove
```bash
$ K8S_NAMESPACE=my-namespace sls remove
```