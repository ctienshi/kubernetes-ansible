# Kubernetes Cluster using Ansible
* Clone repository.
* Create multiple centos8 servers. One master and many worker. Use vagrant like [here](https://github.com/edib/many_vagrant_machines)
* Change the “ad_addr” in the env_variables file with the IP address of the Kubernetes master node.
* Add the IP Addresses of the worker nodes and the master node in the “hosts” file.
* Run the following command to setup the Kubernetes Master node.

```
ansible-playbook setup_master_node.yml
```
* Once the master node is ready, run the following command to set up the worker nodes.

```
ansible-playbook setup_worker_nodes.yml
```

* Once the workers have joined the cluster, run the following command to check the status of the worker nodes.
```
kubectl get nodes
```

## Reference:
* https://medium.com/faun/how-to-create-your-own-kubernetes-cluster-using-ansible-7c6b5c031a5d



