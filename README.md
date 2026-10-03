## Four approaches to deploy Ai on Kubernetes 

We will use vLLM and KServe to learn about some importants Kubernetes overlooked concepts.  
Thanks to RED HAT for teaching me about these tips and tricks.

<img width="729" height="328" alt="Screenshot_2026-10-03_15-47-19" src="https://github.com/user-attachments/assets/315af07c-0398-468d-86b9-aaa8111aa21e" />

### -initContainers + emptyDir 
### -PVC for shared storage
### -ModelCars with OCI container
### -Image Volume (Kubernetes v1.35)


<img width="742" height="571" alt="Screenshot_2026-10-03_16-02-58" src="https://github.com/user-attachments/assets/444db7c2-a067-48cb-8970-3ee2d5812c80" />


Kubernetes Concepts:
-
emptyDir: https://kubernetes.io/docs/concepts/storage/volumes/#emptydir  
init Containers:
https://kubernetes.io/docs/concepts/workloads/pods/init-containers/  
sidecar Containers:
https://kubernetes.io/docs/concepts/workloads/pods/sidecar-containers/  
PV ReadOnlyMany:
https://kubernetes.io/docs/concepts/storage/persistent-volumes/#access-modes  
Share Process Namespace:
https://kubernetes.io/docs/tasks/configure-pod-container/share-process-namespace/  
Model Image Volume:
https://kubernetes.io/docs/tasks/configure-pod-container/image-volumes/  
modelcars Containers:
https://docs.redhat.com/en/documentation/red_hat_openshift_ai_self-managed/2.16/html/serving_models/about-model-serving_about-model-serving

