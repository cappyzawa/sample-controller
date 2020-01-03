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
This file should be written.
* [pkg/apis/samplecontroller/v1alpha1/types.go](./pkg/apis/samplecontroller/v1alpha1/types.go)

### Generate code by code-generator
These files should be written.
* [pkg/apis/samplecontroller/v1alpha1/doc.go](./pkg/apis/samplecontroller/v1alpha1/doc.go)
* [pkg/apis/samplecontroller/v1alpha1/register.go](./pkg/apis/samplecontroller/v1alpha1/register.go)
* [pkg/apis/samplecontroller/register.go](./pkg/apis/samplecontroller/register.go)

```bash
$ ./hack/update-codegen.sh
```

[pkg/apis/samplecontroller/v1alpha1/zz_generated.deepcopy.go](./pkg/apis/samplecontroller/v1alpha1/zz_generated.deepcopy.go) and [pkg/client](./pkg/client) are generated.

### Implement the controller
[controller.go](./controller.go) should be witten.

### Implement main
