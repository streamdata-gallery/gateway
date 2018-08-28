swagger: "2.0"
x-collection-name: AWS Storage Gateway Service
x-complete: 1
info:
  title: AWS Storage Gateway Service API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=ActivateGateway:
    get:
      summary: Activate Gateway
      description: Activates the gateway you previously deployed on your host.
      operationId: activateGateway
      x-api-path-slug: actionactivategateway-get
      parameters:
      - in: query
        name: ActivationKey
        description: Your gateway activation key
        type: string
      - in: query
        name: GatewayName
        description: The name you configured for your gateway
        type: string
      - in: query
        name: GatewayRegion
        description: A value that indicates the region where you want to store the
          snapshot backups
        type: string
      - in: query
        name: GatewayTimezone
        description: A value that indicates the time zone you want to set for the
          gateway
        type: string
      - in: query
        name: GatewayType
        description: A value that defines the type of gateway to activate
        type: string
      - in: query
        name: MediumChangerType
        description: The value that indicates the type of medium changer to use for
          gateway-VTL
        type: string
      - in: query
        name: TapeDriveType
        description: The value that indicates the type of tape drive to use for gateway-VTL
        type: string
      responses:
        200:
          description: OK
      tags:
      - Gateway
  /?Action=DeleteGateway:
    get:
      summary: Delete Gateway
      description: Deletes a gateway.
      operationId: deleteGateway
      x-api-path-slug: actiondeletegateway-get
      parameters:
      - in: query
        name: GatewayARN
        description: The Amazon Resource Name (ARN) of the gateway
        type: string
      responses:
        200:
          description: OK
      tags:
      - Gateway
  /?Action=DescribeGatewayInformation:
    get:
      summary: Describe Gateway Information
      description: |-
        Returns metadata about a gateway such as its name, network interfaces, configured
                 time zone, and the state (whether the gateway is running or not).
      operationId: describeGatewayInformation
      x-api-path-slug: actiondescribegatewayinformation-get
      parameters:
      - in: query
        name: GatewayARN
        description: The Amazon Resource Name (ARN) of the gateway
        type: string
      responses:
        200:
          description: OK
      tags:
      - Gateway
  /?Action=DisableGateway:
    get:
      summary: Disable Gateway
      description: Disables a gateway when the gateway is no longer functioning.
      operationId: disableGateway
      x-api-path-slug: actiondisablegateway-get
      parameters:
      - in: query
        name: GatewayARN
        description: The Amazon Resource Name (ARN) of the gateway
        type: string
      responses:
        200:
          description: OK
      tags:
      - Gateway
  /?Action=ShutdownGateway:
    get:
      summary: Shutdown Gateway
      description: Shuts down a gateway.
      operationId: shutdownGateway
      x-api-path-slug: actionshutdowngateway-get
      parameters:
      - in: query
        name: GatewayARN
        description: The Amazon Resource Name (ARN) of the gateway
        type: string
      responses:
        200:
          description: OK
      tags:
      - Gateway
  /?Action=StartGateway:
    get:
      summary: Start Gateway
      description: Starts a gateway that you previously shut down (see.
      operationId: startGateway
      x-api-path-slug: actionstartgateway-get
      parameters:
      - in: query
        name: GatewayARN
        description: The Amazon Resource Name (ARN) of the gateway
        type: string
      responses:
        200:
          description: OK
      tags:
      - Gateway
  /?Action=UpdateGatewayInformation:
    get:
      summary: Update Gateway Information
      description: Updates a gateway's metadata, which includes the gateway's name
        and time zone.
      operationId: updateGatewayInformation
      x-api-path-slug: actionupdategatewayinformation-get
      parameters:
      - in: query
        name: GatewayARN
        description: The Amazon Resource Name (ARN) of the gateway
        type: string
      - in: query
        name: GatewayName
        description: The name you configured for your gateway
        type: string
      - in: query
        name: GatewayTimezone
        description: 'Type: String'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Gateway
  /?Action=UpdateGatewaySoftwareNow:
    get:
      summary: Update Gateway Software Now
      description: Updates the gateway virtual machine (VM) software.
      operationId: updateGatewaySoftwareNow
      x-api-path-slug: actionupdategatewaysoftwarenow-get
      parameters:
      - in: query
        name: GatewayARN
        description: The Amazon Resource Name (ARN) of the gateway
        type: string
      responses:
        200:
          description: OK
      tags:
      - Gateway
  /?Action=ListGateways:
    get:
      summary: List Gateways
      description: Lists gateways owned by an AWS account in a region specified in
        the request.
      operationId: listGateways
      x-api-path-slug: actionlistgateways-get
      parameters:
      - in: query
        name: Limit
        description: Specifies that the list of gateways returned be limited to the
          specified number of         items
        type: string
      - in: query
        name: Marker
        description: An opaque string that indicates the position at which to begin
          the returned list of         gateways
        type: string
      responses:
        200:
          description: OK
      tags:
      - Gateways