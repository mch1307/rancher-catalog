#**Rancher Traefik**

##Description
Traefik image to be deployed as reverse proxy - load balancer on Rancher Cattle orchestrator.
It will use Rancher API for dynamic configuration. Backend services should have at minimum the following labels:
- traefik.enable = true
- traefik.port = target service port on container
-


##Configuration Options
- **Rancher API endpoint**: Rancher API url endpoint (ie http://rancherhost:8080/v1
- **Rancher API key**: API key to access Rancher API
- **Rancher API secret**: secret API key to access Rancher API

**Rancher API key and secret should be restricted to one Cattle environment**

- **Host label**: Host label for host affinity. 
    - *default*: "traefik_lb=true"
- **HTTP Port**: port to expose for host http traffic
    - *default*: 80
- **HTTPS Port**: port to expose for host https traffic
    - *default*: 443
- **Admin Port**: port to expose for Traefik Web UI
    - *default*: 8000
- **Enable HTTPS**: enable or not SSL 
    - *default*: true
- **Certificate**: SSL Certificate, previously registered in Rancher

     
