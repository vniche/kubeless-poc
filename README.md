kubeless-poc
=========

An POC of how to run Kubeless in a raw local Kubernetes.

![Usage](.assets/serverless.gif)

Design
------------

[Serverless](https://serverless.com/learn/overview)

> What ‘serverless’ really means is that, as a developer you don’t have to think about those servers. You just focus on code.

Requirements
------------

- [Node LTS](https://nodejs.org/en/download/)

This project was bootstrapped via:

```bash
$ npm install -g serverless
$ serverless create --template kubeless-nodejs --path my-project
$ cd my-project/ && npm install
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

#### Local
```bash
$ sls offline start -v
```

#### Deploy
```bash
$ sls deploy -v
```

#### Invoke
```bash
$ sls invoke -f capitalize -d 'hello world' -l
Serverless: Calling function: capitalize...
--------------------------------------------------------------------
Hello world
```

#### Remove
```bash
$ sls remove
```