---
name: IBM Cloud
x-slug: ibm-cloud
description: The IBM Cloud has been built to help you solve problems and advance opportunities
  in a world flush with data. Whether it&rsquo;s data you possess, data outside your
  firewall, or data that&rsquo;s coming, the IBM Cloud helps you protect it, move
  it, integrate it and unlock intelligence from it &mdash; giving you what it takes
  to prevail in a competitive market.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
x-kinRank: "8"
x-alexaRank: "11207"
tags: IP Addresses
created: "2018-08-27"
modified: "2018-08-27"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/ip-addresses/master/_listings/ibm-cloud/apis.md
specificationVersion: "0.14"
apis:
- name: IBM Containers - Release public IP address
  x-api-slug: containersfloatingipsiprelease-post
  description: 'This endpoint releases a public IP address from a space (corresponding
    IBM Containers command: `cf ic ip release <ip_adress>`). The public IP address
    is no longer allocated to the space. If a container was bound to the IP address,
    it is automatically unbound.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3
  tags: SaaS, Technology, Enterprise, API Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/ip-addresses/master/_listings/ibm-cloud/containersfloatingipsiprelease-post-openapi.md
- name: IBM Containers - Bind a public IP address to a single container
  x-api-slug: containersname-or-idfloatingipsipbind-post
  description: 'This endpoint binds an available public IP address to a single container
    (corresponding IBM Containers command: `cf ic ip bind <ip_adress> <container>`).
    After a container is bound to a public IP address, it can be accessed at `https://<public_ip_adress>:<public_port>`.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3
  tags: SaaS, Technology, Enterprise, API Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/ip-addresses/master/_listings/ibm-cloud/containersname-or-idfloatingipsipbind-post-openapi.md
- name: IBM Containers - Unbind a public IP address from a container
  x-api-slug: containersname-or-idfloatingipsipunbind-post
  description: 'This endpoint unbinds a public IP address from a container (corresponding
    IBM Containers command: `cf ic ip unbind <ip_adress> <container>`). The container
    that is unbound from the IP address will not be accessible from the internet anymore.
    The public IP address will be further allocated to the space and can be used to
    be bound to other containers.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3
  tags: SaaS, Technology, Enterprise, API Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/ip-addresses/master/_listings/ibm-cloud/containersname-or-idfloatingipsipunbind-post-openapi.md
- name: IBM Containers - Unbind a public IP address from a container
  x-api-slug: containersname-or-idfloatingipsipunbind-post
  description: 'This endpoint unbinds a public IP address from a container (corresponding
    IBM Containers command: `cf ic ip unbind <ip_adress> <container>`). The container
    that is unbound from the IP address will not be accessible from the internet anymore.
    The public IP address will be further allocated to the space and can be used to
    be bound to other containers.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3
  tags: SaaS, Technology, Enterprise, API Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/ip-addresses/master/_listings/ibm-cloud/containersname-or-idfloatingipsipunbind-post-openapi.md
- name: IBM Containers - Bind a public IP address to a single container
  x-api-slug: containersname-or-idfloatingipsipbind-post
  description: 'This endpoint binds an available public IP address to a single container
    (corresponding IBM Containers command: `cf ic ip bind <ip_adress> <container>`).
    After a container is bound to a public IP address, it can be accessed at `https://<public_ip_adress>:<public_port>`.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3
  tags: SaaS, Technology, Enterprise, API Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/ip-addresses/master/_listings/ibm-cloud/containersname-or-idfloatingipsipbind-post-openapi.md
- name: IBM Containers - Release public IP address
  x-api-slug: containersfloatingipsiprelease-post
  description: 'This endpoint releases a public IP address from a space (corresponding
    IBM Containers command: `cf ic ip release <ip_adress>`). The public IP address
    is no longer allocated to the space. If a container was bound to the IP address,
    it is automatically unbound.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3
  tags: SaaS, Technology, Enterprise, API Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/ip-addresses/master/_listings/ibm-cloud/containersfloatingipsiprelease-post-openapi.md
x-common:
- type: x-api-gallery
  url: http://hsbc.api.gallery.streamdata.io
- type: x-api-stack
  url: http://ibm.cloud.stack.network
- type: x-blog
  url: https://www.ibm.com/blogs/bluemix/
- type: x-crunchbase
  url: https://crunchbase.com/organization/product/ibm-bluemix
- type: x-github
  url: https://github.com/IBM-Cloud
- type: x-twitter
  url: https://twitter.com/IBMcloud
- type: x-website
  url: https://www.ibm.com/cloud/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---