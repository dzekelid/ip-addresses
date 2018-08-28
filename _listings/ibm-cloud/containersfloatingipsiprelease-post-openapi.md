---
swagger: "2.0"
x-collection-name: IBM Cloud
x-complete: 0
info:
  title: IBM Containers Release public IP address
  description: 'This endpoint releases a public IP address from a space (corresponding
    IBM Containers command: `cf ic ip release <ip_adress>`). The public IP address
    is no longer allocated to the space. If a container was bound to the IP address,
    it is automatically unbound.'
  version: 3.0.0
host: containers-api.ng.bluemix.net
basePath: /v3
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /containers/floating-ips/{ip}/release:
    post:
      summary: Release public IP address
      description: 'This endpoint releases a public IP address from a space (corresponding
        IBM Containers command: `cf ic ip release <ip_adress>`). The public IP address
        is no longer allocated to the space. If a container was bound to the IP address,
        it is automatically unbound.'
      operationId: this-endpoint-releases-a-public-ip-address-from-a-space-corresponding-ibm-containers-command-cf-ic-i
      x-api-path-slug: containersfloatingipsiprelease-post
      parameters:
      - in: path
        name: ip
        description: The public IP address that you want to release
      - in: header
        name: X-Auth-Project-Id
        description: The unique ID of your organization space where you want to create
          or work with your containers
      - in: header
        name: X-Auth-Token
        description: The Bluemix JSON web token that you receive when logging into
          Bluemix
      responses:
        200:
          description: OK
      tags:
      - Containers
      - Floating-ips
      - Ip
      - Release
  /containers/{name_or_id}/floating-ips/{ip}/bind:
    post:
      summary: Bind a public IP address to a single container
      description: 'This endpoint binds an available public IP address to a single
        container (corresponding IBM Containers command: `cf ic ip bind <ip_adress>
        <container>`). After a container is bound to a public IP address, it can be
        accessed at `https://<public_ip_adress>:<public_port>`.'
      operationId: this-endpoint-binds-an-available-public-ip-address-to-a-single-container-corresponding-ibm-container
      x-api-path-slug: containersname-or-idfloatingipsipbind-post
      parameters:
      - in: path
        name: ip
        description: The public IP address that you want to bind to your container
      - in: path
        name: name_or_id
        description: The name or ID of the container that you want to bind to the
          public IP address
      - in: header
        name: X-Auth-Project-Id
        description: The unique ID of your organization space where you want to create
          or work with your containers
      - in: header
        name: X-Auth-Token
        description: The Bluemix JSON web token that you receive when logging into
          Bluemix
      responses:
        200:
          description: OK
      tags:
      - Containers
      - Name
      - Floating-ips
      - Ip
      - Bind
  /containers/{name_or_id}/floating-ips/{ip}/unbind:
    post:
      summary: Unbind a public IP address from a container
      description: 'This endpoint unbinds a public IP address from a container (corresponding
        IBM Containers command: `cf ic ip unbind <ip_adress> <container>`). The container
        that is unbound from the IP address will not be accessible from the internet
        anymore. The public IP address will be further allocated to the space and
        can be used to be bound to other containers.'
      operationId: this-endpoint-unbinds-a-public-ip-address-from-a-container-corresponding-ibm-containers-command-cf-i
      x-api-path-slug: containersname-or-idfloatingipsipunbind-post
      parameters:
      - in: path
        name: ip
        description: The public IP address that you want to unbind from your container
      - in: path
        name: name_or_id
        description: The name or ID of the container that you want to bind to the
          public IP address
      - in: header
        name: X-Auth-Project-Id
        description: The unique ID of your organization space where you want to create
          or work with your containers
      - in: header
        name: X-Auth-Token
        description: The Bluemix JSON web token that you receive when logging into
          Bluemix
      responses:
        200:
          description: OK
      tags:
      - Containers
      - Name
      - Floating-ips
      - Ip
      - Unbind
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---