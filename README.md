# crssplane-basics
## Requiremets
- k8s cluster > v1.21
- provider-kuberntes(can be done with any other provider)

`This Repo uses basic Kuberntes object show how crossplane works and also it overrides`

This repo contains one single crossplane xrd(similar to crd if you are familiar with it)

It creates one crossplane object to show how override and openapiv3schema works.

Apologies for the minor details details, but the crossplane docs will be avilable in the Medium link would be updated and shared in releavant channels.

info:

provider-kubernetes: https://github.com/crossplane-contrib/provider-terraform

provider-apireference: https://doc.crds.dev/github.com/crossplane-contrib/provider-terraform

crossplane:  https://crossplane.io/

``` steps to repoduce or how its connected
1. create xrd using xrd.yaml
xrd creates the "CompositeResourceDefinition" or rather how the structre would look like`
2. create the composition using composit.yaml
this is a basically act as a calim template or view if you understand database concepts.
3. then create testyourcustomresource.yaml to actually test the config
```

` some useful topics`
1. The crd created by composition is called `TestPod`
2. crosspane has a concept called object that actually works as reconciler (but not exactly) but for starter its the starting poing to check for errors in your custom-app filled errors or errors in shorts.
```
k get object
NAME               SYNCED   READY   AGE
sample-namespace   False    False   8h
testcross-fsknp    True     True    38m

```

*false is danger,if it is not synced check provider first then describe the object to see the filed issues*

*if you see object is not generated then you have a claim issue check the names.*







***~The Bird of Hermes is my name***


