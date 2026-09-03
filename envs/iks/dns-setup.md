


# Create a new loadbalancer dns entry for the envoy created load balancer


d4b0a139-eu-de.lb.appdomain.cloud matches hostname on service of type loadbalancer in envoy-gateway-system namespace

ibmcloud ks nlb-dns create vpc-gen2 -c daciuuaf0r9orb0p733g --lb-host  02d752a2-eu-de.lb.appdomain.cloud

# List loadbalancers in cluster

ibmcloud ks nlb-dns ls -c daciuuaf0r9orb0p733g

# Replace lb created by envoy with new dns entry 
ibmcloud ks nlb-dns replace -c daciuuaf0r9orb0p733g --lb-host 02d752a2-eu-de.lb.appdomain.cloud  --nlb-subdomain nki-idig.eu-de.containers.appdomain.cloud