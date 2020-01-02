# sample-controller
original repository: https://github.com/kubernetes/sample-controller

## Step
### Implement CRD and CR
CRD: [crd.yaml](./artifacts/examples/crd.yaml)
CR: [example-foo.yaml](./artifacts/examples/example-foo.yaml)

```bash
$ kubectl apply -f artifacts/examples
customresourcedefinition.apiextensions.k8s.io/foos.samplecontroller.k8s.io unchanged
foo.samplecontroller.k8s.io/example-foo created
```

### Define Go Types
### Generate code by code-generator
### Implement the controller
### Implement main
