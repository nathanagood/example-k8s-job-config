# Example Kubernetes Job Configurations

## The hello-world job

This will print out a simple hello-world message using [cowsay](https://hub.docker.com/r/grycap/cowsay/). 
For example, if you run the following command:

```bash
$ kubectl apply -f hello-world/job.yaml
job.batch/hello-world created
```

You should then be able to run `kubectl get pods` to find the name of the pod
that ran the job:

```bash
$ kubectl get pods
...
hello-world-hmxjv                                   0/1     Completed   0          13s
```

And then you can get the output: 

```bash
kubectl logs hello-world-hmxjv
 _____________
< Hello World >
 -------------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||
```
