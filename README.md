This setup is used behind AWS ec2 Load balancer with https. 
cd keycloak-docker-compose

#Hostname Configuration
        KC_HOSTNAME: "yourpublic.hostname.com"
        KC_HOSTNAME_STRICT_HTTPS: 'true'

Update the KC_HOSTNAME with your ELB.

Run docker compose 
docker-compose up -d

Make sure all the ingress rules configured to access the port 8080 and browse https://your_elb_domain:8080/
