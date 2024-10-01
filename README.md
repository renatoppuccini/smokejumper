# smokejumper
A collection of load and scale testing tools for kubernetes  

# Testing order

1. Deploy Bare Metal Cluster
2. Deployed MachineConfig with Multipah configuration in the nodes
3. Deployed CSI Operator
   - 3.1 Configured Infinidat StorageClass (default, permissions)
   - 3.2 Configure Infinidat SnapshotClass
4. Configured Registry
5. Deployed the OpenShift Virtualization Operator
   - 5.1 Created the Virtualization instance (enable VM creation)
6. Deployed the NMState Operator
   - 6.1 Created a NMState DNS configuration for the nodes (due to long DNS name search)

Deployed kube-burner
