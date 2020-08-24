# Network namespace requirement 
All container follow same approach to assign network
![](assets/container-network-namespace.png)
# Move common network requirement into single program
- Move common network into single program
![](assets/bridge-network-program.png)
- Container call this common program 
![](assets/container-use-same -bridge-program.png)
# Container network interface
- Set of standards define how program to develop to solve network challenges in container runtime
![](assets/cni-standard.png)
- Plugins
![](assets/plugins.png)
- Some plugins are developed by third parties
![](assets/third-parties-plugins.png)
- Docker doesn't implement CNI
    - It has it's own standard called CNM
    ![](assets/docker-cnm.png)
    - CNI creates `none` network then manually invoke cni plugin yourself
    ![](assets/docker-none-network-workaround.png)
    - This is how Kubernetes create Docker container
    ![](assets/k8-and-docker.png)


