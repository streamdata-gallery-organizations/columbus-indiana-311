swagger: "2.0"
x-collection-name: Columbus Indiana 311
x-complete: 1
info:
  title: Columbus Indiana 311 GeoReport API
  description: open311-allows-you-to-getpost-civic-information-of-cities-via-a-unified-interface--the-georeport-part-allows-you-to-submit-and-view-issues-at-the-public-local-space
  contact:
    name: Open311 community
    url: http://wiki.open311.org/GeoReport_v2/
    email: discuss@lists.open311.org
  version: 1.0.0
host: csr.columbus.in.gov
basePath: /csr/open311/v2/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /requests.{response_format}:
    get:
      summary: Requests
      description: Query the current status of multiple requests.
      operationId: query-the-current-status-of-multiple-requests
      x-api-path-slug: requests-response-format-get
      parameters:
      - in: query
        name: end_date
        description: Latest datetime to include in search
      - in: query
        name: No Name
      - in: path
        name: response_format
        description: The response in XML or JSON format
        type: string
        format: string
      - in: query
        name: service_code
        description: Specify the service type by calling the unique ID of the service_code
      - in: query
        name: service_request_id
        description: To call multiple Service Requests at once, multiple service_request_id
          can be declared; comma delimited
      - in: query
        name: start_date
        description: Earliest datetime to include in search
      - in: query
        name: status
        description: Allows one to search for requests which have a specific status
      responses:
        200:
          description: OK
      tags:
      - "311"
      - Requests
    post:
      summary: Create Service Request
      description: Submit a new request for with specific details of a single service.
        Must provide a location via lat/long or address_string or address_id
      operationId: submit-a-new-request-for-with-specific-details-of-a-single-service-must-provide-a-location-via-latlo
      x-api-path-slug: requests-response-format-post
      parameters:
      - in: query
        name: address_id
      - in: query
        name: address_string
      - in: query
        name: attribute
        description: array of key/value responses based on Service Definitions
      - in: query
        name: lat
        description: WGS-84 latitude
      - in: query
        name: long
        description: WGS-84 longitude
      - in: query
        name: No Name
      - in: path
        name: response_format
        description: The response in XML or JSON format
        type: string
        format: string
      - in: query
        name: service_code
      responses:
        200:
          description: OK
      tags:
      - "311"
      - Service
      - Request
  /request/{service_request_id}.{response_format}:
    get:
      summary: Current Status
      description: Query the current status of an individual request
      operationId: query-the-current-status-of-an-individual-request
      x-api-path-slug: requestservice-request-id-response-format-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: service_request_id
        description: Is specified in the main URL path rather than an added query
          string parameter
      responses:
        200:
          description: OK
      tags:
      - "311"
      - Current
      - Status
  /services.{response_format}:
    get:
      summary: Service Types
      description: List acceptable service request types and their associated service
        codes. These request types can be unique to the city/jurisdiction.
      operationId: list-acceptable-service-request-types-and-their-associated-service-codes-these-request-types-can-be-
      x-api-path-slug: services-response-format-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: response_format
        description: The response in XML or JSON format
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - "311"
      - Service
      - Types
  /services/{service_code}.{response_format}:
    get:
      summary: Definition Of A Service Type
      description: Define attributes associated with a service code. These attributes
        can be unique to the city/jurisdiction.
      operationId: define-attributes-associated-with-a-service-code-these-attributes-can-be-unique-to-the-cityjurisdict
      x-api-path-slug: servicesservice-code-response-format-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: service_code
      responses:
        200:
          description: OK
      tags:
      - "311"
      - Definition
      - Service
      - Type
  /tokens/{token_id}.{response_format}:
    get:
      summary: Id Of Service_request Via Token
      description: Get the service_request_id from a temporary token. This is unnecessary
        if the response from creating a service request does not contain a token.
      operationId: get-the-service-request-id-from-a-temporary-token-this-is-unnecessary-if-the-response-from-creating-
      x-api-path-slug: tokenstoken-id-response-format-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: token_id
      responses:
        200:
          description: OK
      tags:
      - "311"
      - Id
      - Service
      - Request
      - Via
      - Token