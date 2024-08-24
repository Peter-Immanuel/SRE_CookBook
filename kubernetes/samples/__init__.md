# Kubernetes Configuration File Structure

A configuration file (YAML of course 😉) is made up of 3 parts by convention called 'Manifest':
- MetaData
- Specification (spec)
- Status (Created and Managed by K8): This is stored in the 'etcd' componet of the Master Node (Control Plane)


Every Manifest contains the following fields
- apiVersion: version of k8 used to create the object
- kind: kind of object to create (Deployment, Service, ...)
- metadata: data used to identify an object (name, UID and Optional _namespace_)
- spec: desired state of the object. Object spec differ depending on the kubernetes object: [Reference Guide](https://kubernetes.io/docs/reference/kubernetes-api/)

The metadata attribute describes labels which would be use by selectors in the spec section of the/another configuration file.




