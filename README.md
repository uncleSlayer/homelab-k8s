# This is my notes for kubernetes
###### I'm trying to learn kubernetes by testing everything on my homelab


## replicaSet vs deployment

So I created a deployment first, then i checked how many pods are running, and it was showing x let's say.

Then I created a replicaSet, and it also created x pods.

Then I became confused unga bunga

So what extra does deployment provide?

So when you create a deployment, it automatically creates a replicaSet as well.
When you update and reapply the deployment, it doesn't create a new replicaSet, it just updates the existing one.

But when you update and reapply the replicaSet, it creates a new replicaSet.

Why is that?

This helps us with rolling updates.

When you update the deployment, it will create a new replicaSet, and then it will update the pods in the existing replicaSet. Also let's say for some reason the update fails, then the old pods will still be running. The update will only take place when the pods are in a ready state.

Whereas in case of replicaSet, it will create a new replicaSet, and then it will update the pods in the new replicaSet.

## How port works in a service
![image](https://github.com/user-attachments/assets/236a5823-9d06-4a14-a374-8ad8523e8479)

