---
swagger: "2.0"
x-collection-name: SendGrid
x-complete: 0
info:
  title: SendGrid Delete Ips Warmup Ip Address
  description: |-
    **This endpoint allows you to remove an IP address from warmup mode.**

    SendGrid can automatically warm up dedicated IP addresses by limiting the amount of mail that can be sent through them per hour, with the limit determined by how long the IP address has been in warmup. See the [warmup schedule](https://sendgrid.com/docs/API_Reference/Web_API_v3/IP_Management/ip_warmup_schedule.html) for more details on how SendGrid limits your email traffic for IPs in warmup.

    For more general information about warming up IPs, please see our [Classroom](https://sendgrid.com/docs/Classroom/Deliver/Delivery_Introduction/warming_up_ips.html).
  version: 1.0.0
host: api.sendgrid.com
basePath: /v3
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /ips/pools/{pool_name}/ips/{ip}:
    delete:
      summary: Delete Ips Pools Pool Name Ips Ip
      description: |-
        **This endpoint allows you to remove an IP address from an IP pool.**

        The same IP address can be added to multiple IP pools.

        A single IP address or a range of IP addresses may be dedicated to an account in order to send email for multiple domains. The reputation of this IP is based on the aggregate performance of all the senders who use it.
      operationId: ips.pools.pool_name.ips.ip.delete
      x-api-path-slug: ipspoolspool-nameipsip-delete
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Email
      - Ips
      - Pools
      - Pool
      - Name
      - Ips
      - Ip
  /ips/warmup/{ip_address}:
    delete:
      summary: Delete Ips Warmup Ip Address
      description: |-
        **This endpoint allows you to remove an IP address from warmup mode.**

        SendGrid can automatically warm up dedicated IP addresses by limiting the amount of mail that can be sent through them per hour, with the limit determined by how long the IP address has been in warmup. See the [warmup schedule](https://sendgrid.com/docs/API_Reference/Web_API_v3/IP_Management/ip_warmup_schedule.html) for more details on how SendGrid limits your email traffic for IPs in warmup.

        For more general information about warming up IPs, please see our [Classroom](https://sendgrid.com/docs/Classroom/Deliver/Delivery_Introduction/warming_up_ips.html).
      operationId: ips.warmup.ip_address.delete
      x-api-path-slug: ipswarmupip-address-delete
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Ips
      - Warmup
      - Ip
      - Address
    get:
      summary: Get Ips Warmup Ip Address
      description: |-
        **This endpoint allows you to retrieve the warmup status for a specific IP address.**

        SendGrid can automatically warm up dedicated IP addresses by limiting the amount of mail that can be sent through them per hour, with the limit determined by how long the IP address has been in warmup. See the [warmup schedule](https://sendgrid.com/docs/API_Reference/Web_API_v3/IP_Management/ip_warmup_schedule.html) for more details on how SendGrid limits your email traffic for IPs in warmup.

        For more general information about warming up IPs, please see our [Classroom](https://sendgrid.com/docs/Classroom/Deliver/Delivery_Introduction/warming_up_ips.html).
      operationId: ips.warmup.ip_address.get
      x-api-path-slug: ipswarmupip-address-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Ips
      - Warmup
      - Ip
      - Address
  /ips/{ip_address}:
    get:
      summary: Get Ips Ip Address
      description: |-
        **This endpoint allows you to see which IP pools a particular IP address has been added to.**

        The same IP address can be added to multiple IP pools.

        A single IP address or a range of IP addresses may be dedicated to an account in order to send email for multiple domains. The reputation of this IP is based on the aggregate performance of all the senders who use it.
      operationId: ips.ip_address.get
      x-api-path-slug: ipsip-address-get
      responses:
        200:
          description: OK
      tags:
      - Email
      - Ips
      - Ip
      - Address
  /whitelabel/domains/{id}/ips/{ip}:
    delete:
      summary: Delete Whitelabel Domains  Ips Ip
      description: |-
        **This endpoint allows you to remove a domain's IP address from that domain's whitelabel.**

        A domain whitelabel allows you to remove the ???via??? or ???sent on behalf of??? message that your recipients see when they read your emails. Whitelabeling a domain allows you to replace sendgrid.net with your personal sending domain. You will be required to create a subdomain so that SendGrid can generate the DNS records which you must give to your host provider. If you choose to use Automated Security, SendGrid will provide you with 3 CNAME records. If you turn Automated Security off, you will be given 2 TXT records and 1 MX record.

        For more information on whitelabeling, please see our [User Guide](https://sendgrid.com/docs/User_Guide/Settings/Whitelabel/index.html)

        ## URI Parameters
        | URI Parameter   | Type  | Description  |
        |---|---|---|
        | id | integer  | ID of the domain whitelabel to delete the IP from. |
        | ip | string | IP to remove from the domain whitelabel. |
      operationId: whitelabel.domains.id.ips.ip.delete
      x-api-path-slug: whitelabeldomainsidipsip-delete
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Whitelabel
      - Domains
      - ""
      - Ips
      - Ip
  /ips:
    get:
      summary: Get Ips
      description: |-
        **This endpoint allows you to retrieve a list of all assigned and unassigned IPs.**

        Response includes warm up status, pools, assigned subusers, and whitelabel info. The start_date field corresponds to when warmup started for that IP.

        A single IP address or a range of IP addresses may be dedicated to an account in order to send email for multiple domains. The reputation of this IP is based on the aggregate performance of all the senders who use it.
      operationId: GET_ips
      x-api-path-slug: ips-get
      parameters:
      - in: query
        name: exclude_whitelabels
        description: Should we exclude whitelabels?
      - in: query
        name: ip
        description: The IP address to get
      - in: query
        name: limit
        description: The number of IPs you want returned at the same time
      - in: query
        name: offset
        description: The offset for the number of IPs that you are requesting
      - in: query
        name: sort_by_direction
        description: The direction to sort the results
      - in: query
        name: subuser
        description: The subuser you are requesting for
      responses:
        200:
          description: OK
      tags:
      - Email
      - Ips
    post:
      summary: Add Ips
      description: This endpoint is for adding a(n) IP Address(es) to your account.
      operationId: POST_ips
      x-api-path-slug: ips-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Email
      - Ips
  /ips/assigned:
    get:
      summary: Get Ips Assigned
      description: |-
        **This endpoint allows you to retrieve only assigned IP addresses.**

        A single IP address or a range of IP addresses may be dedicated to an account in order to send email for multiple domains. The reputation of this IP is based on the aggregate performance of all the senders who use it.
      operationId: ips.assigned.get
      x-api-path-slug: ipsassigned-get
      responses:
        200:
          description: OK
      tags:
      - Email
      - Ips
      - Assigned
  /ips/pools:
    get:
      summary: Get Ips Pools
      description: |-
        **This endpoint allows you to retreive all of your IP pools.**

        IP Pools allow you to group your dedicated SendGrid IP addresses together. For example, you could create separate pools for your transactional and marketing email. When sending marketing emails, specify that you want to use the marketing IP pool. This allows you to maintain separate reputations for your different email traffic.

        IP pools can only be used with whitelabeled IP addresses.

        If an IP pool is NOT specified for an email, it will use any IP available, including ones in pools.
      operationId: ips.pools.get
      x-api-path-slug: ipspools-get
      responses:
        200:
          description: OK
      tags:
      - Email
      - Ips
      - Pools
    post:
      summary: Add Ips Pools
      description: |-
        **This endpoint allows you to create an IP pool.**

        **Each user can create up to 10 different IP pools.**

        IP Pools allow you to group your dedicated SendGrid IP addresses together. For example, you could create separate pools for your transactional and marketing email. When sending marketing emails, specify that you want to use the marketing IP pool. This allows you to maintain separate reputations for your different email traffic.

        IP pools can only be used with whitelabeled IP addresses.

        If an IP pool is NOT specified for an email, it will use any IP available, including ones in pools.
      operationId: ips.pools.post
      x-api-path-slug: ipspools-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Email
      - Ips
      - Pools
  /ips/pools/{pool_name}:
    delete:
      summary: Delete Ips Pools Pool Name
      description: |-
        **This endpoint allows you to delete an IP pool.**

        IP Pools allow you to group your dedicated SendGrid IP addresses together. For example, you could create separate pools for your transactional and marketing email. When sending marketing emails, specify that you want to use the marketing IP pool. This allows you to maintain separate reputations for your different email traffic.

        IP pools can only be used with whitelabeled IP addresses.

        If an IP pool is NOT specified for an email, it will use any IP available, including ones in pools.
      operationId: ips.pools.pool_name.delete
      x-api-path-slug: ipspoolspool-name-delete
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Email
      - Ips
      - Pools
      - Pool
      - Name
    get:
      summary: Get Ips Pools Pool Name
      description: |-
        **This endpoint allows you to list all of the IP addresses that are in a specific IP pool.**

        IP Pools allow you to group your dedicated SendGrid IP addresses together. For example, you could create separate pools for your transactional and marketing email. When sending marketing emails, specify that you want to use the marketing IP pool. This allows you to maintain separate reputations for your different email traffic.

        IP pools can only be used with whitelabeled IP addresses.

        If an IP pool is NOT specified for an email, it will use any IP available, including ones in pools.
      operationId: ips.pools.pool_name.get
      x-api-path-slug: ipspoolspool-name-get
      responses:
        200:
          description: OK
      tags:
      - Email
      - Ips
      - Pools
      - Pool
      - Name
    put:
      summary: Put Ips Pools Pool Name
      description: |-
        **This endpoint allows you to update the name of an IP pool.**

        IP Pools allow you to group your dedicated SendGrid IP addresses together. For example, you could create separate pools for your transactional and marketing email. When sending marketing emails, specify that you want to use the marketing IP pool. This allows you to maintain separate reputations for your different email traffic.

        IP pools can only be used with whitelabeled IP addresses.

        If an IP pool is NOT specified for an email, it will use any IP available, including ones in pools.
      operationId: ips.pools.pool_name.put
      x-api-path-slug: ipspoolspool-name-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Email
      - Ips
      - Pools
      - Pool
      - Name
  /ips/pools/{pool_name}/ips:
    post:
      summary: Add Ips Pools Pool Name Ips
      description: |-
        **This endpoint allows you to add an IP address to an IP pool.**

        You can add the same IP address to multiple pools. It may take up to 60 seconds for your IP address to be added to a pool after your request is made.

        A single IP address or a range of IP addresses may be dedicated to an account in order to send email for multiple domains. The reputation of this IP is based on the aggregate performance of all the senders who use it.
      operationId: ips.pools.pool_name.ips.post
      x-api-path-slug: ipspoolspool-nameips-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Email
      - Ips
      - Pools
      - Pool
      - Name
      - Ips
  /ips/remaining:
    get:
      summary: Get Ips Remaining
      description: This endpoint gets amount of IP Addresses that can still be created
        during a given period and the price of those IPs.
      operationId: ips.remaining.get
      x-api-path-slug: ipsremaining-get
      responses:
        200:
          description: OK
      tags:
      - Email
      - Ips
      - Remaining
  /ips/warmup:
    get:
      summary: Get Ips Warmup
      description: |-
        **This endpoint allows you to retrieve all of your IP addresses that are currently warming up.**

        SendGrid can automatically warm up dedicated IP addresses by limiting the amount of mail that can be sent through them per hour, with the limit determined by how long the IP address has been in warmup. See the [warmup schedule](https://sendgrid.com/docs/API_Reference/Web_API_v3/IP_Management/ip_warmup_schedule.html) for more details on how SendGrid limits your email traffic for IPs in warmup.

        For more general information about warming up IPs, please see our [Classroom](https://sendgrid.com/docs/Classroom/Deliver/Delivery_Introduction/warming_up_ips.html).
      operationId: ips.warmup.get
      x-api-path-slug: ipswarmup-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Ips
      - Warmup
    post:
      summary: Add Ips Warmup
      description: |-
        **This endpoint allows you to enter an IP address into warmup mode.**

        SendGrid can automatically warm up dedicated IP addresses by limiting the amount of mail that can be sent through them per hour, with the limit determined by how long the IP address has been in warmup. See the [warmup schedule](https://sendgrid.com/docs/API_Reference/Web_API_v3/IP_Management/ip_warmup_schedule.html) for more details on how SendGrid limits your email traffic for IPs in warmup.

        For more general information about warming up IPs, please see our [Classroom](https://sendgrid.com/docs/Classroom/Deliver/Delivery_Introduction/warming_up_ips.html).
      operationId: ips.warmup.post
      x-api-path-slug: ipswarmup-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Ips
      - Warmup
  /subusers/{subuser_name}/ips:
    put:
      summary: Put Subusers Subuser Name Ips
      description: "Each subuser should be assigned to an IP address, from which all
        of this subuser's mail will be sent. Often, this is the same IP as the parent
        account, but each subuser can have their own, or multiple, IP addresses as
        well. \n\nMore information:\n\n* [How to request more IPs](https://sendgrid.com/docs/Classroom/Basics/Account/adding_an_additional_dedicated_ip_to_your_account.html)\n*
        [IPs can be whitelabeled](https://sendgrid.com/docs/User_Guide/Settings/Whitelabel/ips.html)"
      operationId: subusers.subuser_name.ips.put
      x-api-path-slug: subuserssubuser-nameips-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Subusers
      - Subuser
      - Name
      - Ips
  /whitelabel/domains/{id}/ips:
    post:
      summary: Add Whitelabel Domains  Ips
      description: |-
        **This endpoint allows you to add an IP address to a domain whitelabel.**

        A domain whitelabel allows you to remove the ???via??? or ???sent on behalf of??? message that your recipients see when they read your emails. Whitelabeling a domain allows you to replace sendgrid.net with your personal sending domain. You will be required to create a subdomain so that SendGrid can generate the DNS records which you must give to your host provider. If you choose to use Automated Security, SendGrid will provide you with 3 CNAME records. If you turn Automated Security off, you will be given 2 TXT records and 1 MX record.

        For more information on whitelabeling, please see our [User Guide](https://sendgrid.com/docs/User_Guide/Settings/Whitelabel/index.html)

        ## URI Parameters
        | URI Parameter   | Type  |  Description  |
        |---|---|---|
        | id | integer  | ID of the domain to which you are adding an IP |
      operationId: whitelabel.domains.id.ips.post
      x-api-path-slug: whitelabeldomainsidips-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Whitelabel
      - Domains
      - ""
      - Ips
  /whitelabel/ips:
    get:
      summary: Get Whitelabel Ips
      description: |-
        **This endpoint allows you to retrieve all of the IP whitelabels that have been createdy by this account.**

        You may include a search key by using the "ip" parameter. This enables you to perform a prefix search for a given IP segment (e.g. "192.").

        A IP whitelabel consists of a subdomain and domain that will be used to generate a reverse DNS record for a given IP. Once SendGrid has verified that the appropriate A record for the IP has been created, the appropriate reverse DNS record for the IP is generated.

        For more information, please see our [User Guide](https://sendgrid.com/docs/API_Reference/Web_API_v3/Whitelabel/ips.html).
      operationId: whitelabel.ips.get
      x-api-path-slug: whitelabelips-get
      parameters:
      - in: query
        name: ip
        description: The IP segment that you would like to use in a prefix search
      - in: query
        name: limit
        description: The number of results to retrieve
      - in: query
        name: No Name
      - in: query
        name: offset
        description: The point in the list of results to begin retrieving IPs from
      responses:
        200:
          description: OK
      tags:
      - Email
      - Whitelabel
      - Ips
    post:
      summary: Add Whitelabel Ips
      description: |-
        **This endpoint allows you to create an IP whitelabel.**

        When creating an IP whitelable, you should use the same subdomain that you used when you created a domain whitelabel.

        A IP whitelabel consists of a subdomain and domain that will be used to generate a reverse DNS record for a given IP. Once SendGrid has verified that the appropriate A record for the IP has been created, the appropriate reverse DNS record for the IP is generated.

        For more information, please see our [User Guide](https://sendgrid.com/docs/API_Reference/Web_API_v3/Whitelabel/ips.html).
      operationId: whitelabel.ips.post
      x-api-path-slug: whitelabelips-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Whitelabel
      - Ips
  /whitelabel/ips/{id}:
    delete:
      summary: Delete Whitelabel Ips
      description: |-
        **This endpoint allows you to delete an IP whitelabel.**

        A IP whitelabel consists of a subdomain and domain that will be used to generate a reverse DNS record for a given IP. Once SendGrid has verified that the appropriate A record for the IP has been created, the appropriate reverse DNS record for the IP is generated.

        For more information, please see our [User Guide](https://sendgrid.com/docs/API_Reference/Web_API_v3/Whitelabel/ips.html).
      operationId: whitelabel.ips.id.delete
      x-api-path-slug: whitelabelipsid-delete
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Whitelabel
      - Ips
    get:
      summary: Get Whitelabel Ips
      description: |-
        **This endpoint allows you to retrieve an IP whitelabel.**

        A IP whitelabel consists of a subdomain and domain that will be used to generate a reverse DNS record for a given IP. Once SendGrid has verified that the appropriate A record for the IP has been created, the appropriate reverse DNS record for the IP is generated.

        For more information, please see our [User Guide](https://sendgrid.com/docs/API_Reference/Web_API_v3/Whitelabel/ips.html).
      operationId: whitelabel.ips.id.get
      x-api-path-slug: whitelabelipsid-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Whitelabel
      - Ips
  /whitelabel/ips/{id}/validate:
    post:
      summary: Add Whitelabel Ips  Valate
      description: |-
        **This endpoint allows you to validate an IP whitelabel.**

        A IP whitelabel consists of a subdomain and domain that will be used to generate a reverse DNS record for a given IP. Once SendGrid has verified that the appropriate A record for the IP has been created, the appropriate reverse DNS record for the IP is generated.

        For more information, please see our [User Guide](https://sendgrid.com/docs/API_Reference/Web_API_v3/Whitelabel/ips.html).
      operationId: whitelabel.ips.id.validate.post
      x-api-path-slug: whitelabelipsidvalidate-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Whitelabel
      - Ips
      - ""
      - Valate
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