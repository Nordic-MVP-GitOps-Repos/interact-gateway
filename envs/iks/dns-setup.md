# DNS configuration

Deploying the [envoy-proxy](../../components/envoy/base/envoy-proxy.yaml) creates a service of type LoadBalancer in envoy-gateway-system. Traffic to idig needs to go here. 

Domain configured in [idig-cluster-dev.yaml](../../components/idig/base/idig-cluster-dev.yaml) needs to reference this loadbalancer. We need to create a new dns entry for that.

# Create a new loadbalancer dns entry for the envoy created load balancer

ibmcloud ks nlb-dns create vpc-gen2 -c <cluster-id> --lb-host  <external-ip-from-loadbalancer>

# List loadbalancers in cluster

ibmcloud ks nlb-dns ls -c <cluster-id>