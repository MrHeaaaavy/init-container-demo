## Demo for k8s init container usage

* Build init container
    * `cd 1-init-container`
    * `bash ./build.sh`
* Build runner container
    * `cd 2-runner`
    * `bash ./build.sh`
* Deploy
    * `cd 3-kubernetes`
    * `kubectl apply -f deployment.yml`
* Verification
    * `kubectl logs $(kubectl get pod -l app=myapp -o jsonpath="{.items[0].metadata.name}")`
