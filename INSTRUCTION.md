1. Give execute permission for the file: 
`chmod 774 bootstrap.sh`

2. Create cluster first through script:
`./bootstrap.sh`

3. Check the nodes have been created: 
`kubectl get nodes --show-labels`
here will be:
- 2 nodes with mysql label
- 3 nodes with todoapp label
- 1 node with no label
    
4. Check taint nodes: 
`kubectl describe nodes | grep -E "^Name:|^Taints"`
here will be 2 nodes (kind-worker and kind-woker2):
*Taints: app=mysql:NoSchedule*

5. 
