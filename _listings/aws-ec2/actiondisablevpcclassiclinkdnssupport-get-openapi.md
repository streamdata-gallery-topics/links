---
swagger: "2.0"
x-collection-name: AWS EC2
x-complete: 0
info:
  title: AWS EC2 API Disable Vpc Classic Link Dns Support
  version: 1.0.0
  description: Disables ClassicLink DNS support for a VPC.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=AttachClassicLinkVpc:
    get:
      summary: Attach Classic Link Vpc
      description: "Links an EC2-Classic instance to a ClassicLink-enabled VPC through
        one or more of the VPC's\n\t\t\tsecurity groups."
      operationId: attachclassiclinkvpc
      x-api-path-slug: actionattachclassiclinkvpc-get
      parameters:
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,     and provides an error response
        type: string
      - in: query
        name: Filter.N
        description: One or more filters
        type: string
      - in: query
        name: InstanceId.N
        description: One or more instance IDs
        type: string
      - in: query
        name: MaxResults
        description: The maximum number of results to return for the request in a
          single page
        type: string
      - in: query
        name: NextToken
        description: The token to retrieve the next page of results
        type: string
      responses:
        200:
          description: OK
      tags:
      - VPC Link
  /?Action=DescribeClassicLinkInstances:
    get:
      summary: Describe Classic Link Instances
      description: Describes one or more of your linked EC2-Classic instances.
      operationId: describeclassiclinkinstances
      x-api-path-slug: actiondescribeclassiclinkinstances-get
      parameters:
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,     and provides an error response
        type: string
      - in: query
        name: Filter.N
        description: One or more filters
        type: string
      - in: query
        name: VpcId.N
        description: One or more VPCs for which you want to describe the ClassicLink
          status
        type: string
      responses:
        200:
          description: OK
      tags:
      - Server Instance
  /?Action=DescribeVpcClassicLink:
    get:
      summary: Describe Vpc Classic Link
      description: Describes the ClassicLink status of one or more VPCs.
      operationId: describevpcclassiclink
      x-api-path-slug: actiondescribevpcclassiclink-get
      parameters:
      - in: query
        name: MaxResults
        description: The maximum number of items to return for this request
        type: string
      - in: query
        name: NextToken
        description: The token for the next set of items to return
        type: string
      - in: query
        name: VpcIds.N
        description: One or more VPC IDs
        type: string
      responses:
        200:
          description: OK
      tags:
      - VPC
  /?Action=DescribeVpcClassicLinkDnsSupport:
    get:
      summary: Describe Vpc Classic Link Dns Support
      description: Describes the ClassicLink DNS support status of one or more VPCs.
      operationId: describevpcclassiclinkdnssupport
      x-api-path-slug: actiondescribevpcclassiclinkdnssupport-get
      parameters:
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,     and provides an error response
        type: string
      - in: query
        name: InstanceId
        description: The ID of the instance to unlink from the VPC
        type: string
      - in: query
        name: VpcId
        description: The ID of the VPC to which the instance is linked
        type: string
      responses:
        200:
          description: OK
      tags:
      - VPC DNS
  /?Action=DetachClassicLinkVpc:
    get:
      summary: Detach Classic Link Vpc
      description: Unlinks (detaches) a linked EC2-Classic instance from a VPC.
      operationId: detachclassiclinkvpc
      x-api-path-slug: actiondetachclassiclinkvpc-get
      parameters:
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,     and provides an error response
        type: string
      - in: query
        name: VpcId
        description: The ID of the VPC
        type: string
      responses:
        200:
          description: OK
      tags:
      - VPC
  /?Action=DisableVpcClassicLink:
    get:
      summary: Disable Vpc Classic Link
      description: Disables ClassicLink for a VPC.
      operationId: disablevpcclassiclink
      x-api-path-slug: actiondisablevpcclassiclink-get
      parameters:
      - in: query
        name: VpcId
        description: The ID of the VPC
        type: string
      responses:
        200:
          description: OK
      tags:
      - VPC
  /?Action=DisableVpcClassicLinkDnsSupport:
    get:
      summary: Disable Vpc Classic Link Dns Support
      description: Disables ClassicLink DNS support for a VPC.
      operationId: disablevpcclassiclinkdnssupport
      x-api-path-slug: actiondisablevpcclassiclinkdnssupport-get
      parameters:
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,     and provides an error response
        type: string
      - in: query
        name: VpcId
        description: The ID of the VPC
        type: string
      responses:
        200:
          description: OK
      tags:
      - VPC DNS
  /?Action=EnableVpcClassicLink:
    get:
      summary: Enable Vpc Classic Link
      description: Enables a VPC for ClassicLink.
      operationId: enablevpcclassiclink
      x-api-path-slug: actionenablevpcclassiclink-get
      parameters:
      - in: query
        name: VpcId
        description: The ID of the VPC
        type: string
      responses:
        200:
          description: OK
      tags:
      - VPC
  /?Action=EnableVpcClassicLinkDnsSupport:
    get:
      summary: Enable Vpc Classic Link Dns Support
      description: Enables a VPC to support DNS hostname resolution for ClassicLink.
      operationId: enablevpcclassiclinkdnssupport
      x-api-path-slug: actionenablevpcclassiclinkdnssupport-get
      parameters:
      - in: query
        name: BgpAsn
        description: For devices that support BGP, the customer gateways BGP ASN
        type: string
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,             and provides an error response
        type: string
      - in: query
        name: IpAddress
        description: The Internet-routable IP address for the customer gateways outside
          interface
        type: string
      - in: query
        name: Type
        description: The type of VPN connection that this customer gateway supports
          (ipsec
        type: string
      responses:
        200:
          description: OK
      tags:
      - VPC NS
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