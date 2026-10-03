## Four approaches to deploy Ai on Kubernetes 

We will use vLLM and KServe to learn about some importants Kubernetes overlooked concepts.  
Thanks to RED HAT for teaching me about these tips and tricks.

<img width="729" height="328" alt="Screenshot_2026-10-03_15-47-19" src="https://github.com/user-attachments/assets/315af07c-0398-468d-86b9-aaa8111aa21e" />

### -ModelCars with OCI container: 
make a KServe container with vLLM runtime read a Model Container with no copy in between adding a SymLink to emptyDir rather than copy paste inside it.  

-Share Process Namespace:
https://kubernetes.io/docs/tasks/configure-pod-container/share-process-namespace/  
-Sidecar Containers:
https://kubernetes.io/docs/concepts/workloads/pods/sidecar-containers/  
-Modelcars:
https://docs.redhat.com/en/documentation/red_hat_openshift_ai_self-managed/2.16/html/serving_models/about-model-serving_about-model-serving

<img width="742" height="571" alt="Screenshot_2026-10-03_16-02-58" src="https://github.com/user-attachments/assets/444db7c2-a067-48cb-8970-3ee2d5812c80" />


### -initContainers + emptyDir : 
to copy many Ai Models on many Pods / Nodes  

-emptyDir: https://kubernetes.io/docs/concepts/storage/volumes/#emptydir  
-init Containers:
https://kubernetes.io/docs/concepts/workloads/pods/init-containers/  
### -PVC for shared storage: 
to share a single Model on many Replicas (no copy paste of model just direct read thanks to volumes)  

-PV ReadOnlyMany:
https://kubernetes.io/docs/concepts/storage/persistent-volumes/#access-modes  

  



### -Image Volume (Kubernetes v1.35) : 
new beta and official feature to mount models as volumes inside pods  

-Model Image Volume:
https://kubernetes.io/docs/tasks/configure-pod-container/image-volumes/






