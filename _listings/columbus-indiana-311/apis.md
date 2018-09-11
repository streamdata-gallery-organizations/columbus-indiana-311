---
name: Columbus Indiana 311
x-slug: columbus-indiana-311
description: The Columbus Service Center is also known as 3-1-1; its mission is to
  provide access to City services and City information with the highest possible levels
  of customer service. The 3-1-1 initiative strives to help City agencies provide
  efficient service delivery by allowing them to focus on their core missions, manage
  workloads efficiently, provide insight into the needs of residents, and measure
  how well services are delivered.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/COC_311_RGB_TEXT.jpg
x-kinRank: "7"
x-alexaRank: "0"
tags: Columbus Indiana 311
created: "2018-09-10"
modified: "2018-09-10"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/columbus-indiana-311/master/_listings/columbus-indiana-311/apis.md
specificationVersion: "0.14"
apis:
- name: Columbus Indiana 311 GeoReport API - Requests
  x-api-slug: requests-response-format-get
  description: Query the current status of multiple requests.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/COC_311_RGB_TEXT.jpg
  humanURL: https://311.columbus.gov/
  baseURL: https://csr.columbus.in.gov//csr/open311/v2/
  tags: 311, Open311
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/columbus-indiana-311/master/_listings/columbus-indiana-311/requests-response-format-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/columbus-indiana-311/master/_listings/columbus-indiana-311/requests-response-format-get-openapi.md
- name: Columbus Indiana 311 GeoReport API - Create Service Request
  x-api-slug: requests-response-format-post
  description: Submit a new request for with specific details of a single service.
    Must provide a location via lat/long or address_string or address_id
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/COC_311_RGB_TEXT.jpg
  humanURL: https://311.columbus.gov/
  baseURL: https://csr.columbus.in.gov//csr/open311/v2/
  tags: 311, Open311
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/columbus-indiana-311/master/_listings/columbus-indiana-311/requests-response-format-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/columbus-indiana-311/master/_listings/columbus-indiana-311/requests-response-format-post-openapi.md
- name: Columbus Indiana 311 GeoReport API - Current Status
  x-api-slug: requestservice-request-id-response-format-get
  description: Query the current status of an individual request
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/COC_311_RGB_TEXT.jpg
  humanURL: https://311.columbus.gov/
  baseURL: https://csr.columbus.in.gov//csr/open311/v2/
  tags: 311, Open311
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/columbus-indiana-311/master/_listings/columbus-indiana-311/requestservice-request-id-response-format-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/columbus-indiana-311/master/_listings/columbus-indiana-311/requestservice-request-id-response-format-get-openapi.md
- name: Columbus Indiana 311 GeoReport API - Service Types
  x-api-slug: services-response-format-get
  description: List acceptable service request types and their associated service
    codes. These request types can be unique to the city/jurisdiction.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/COC_311_RGB_TEXT.jpg
  humanURL: https://311.columbus.gov/
  baseURL: https://csr.columbus.in.gov//csr/open311/v2/
  tags: 311, Open311
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/columbus-indiana-311/master/_listings/columbus-indiana-311/services-response-format-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/columbus-indiana-311/master/_listings/columbus-indiana-311/services-response-format-get-openapi.md
- name: Columbus Indiana 311 GeoReport API - Definition Of A Service Type
  x-api-slug: servicesservice-code-response-format-get
  description: Define attributes associated with a service code. These attributes
    can be unique to the city/jurisdiction.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/COC_311_RGB_TEXT.jpg
  humanURL: https://311.columbus.gov/
  baseURL: https://csr.columbus.in.gov//csr/open311/v2/
  tags: 311, Open311
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/columbus-indiana-311/master/_listings/columbus-indiana-311/servicesservice-code-response-format-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/columbus-indiana-311/master/_listings/columbus-indiana-311/servicesservice-code-response-format-get-openapi.md
- name: Columbus Indiana 311 GeoReport API - Id Of Service_request Via Token
  x-api-slug: tokenstoken-id-response-format-get
  description: Get the service_request_id from a temporary token. This is unnecessary
    if the response from creating a service request does not contain a token.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/COC_311_RGB_TEXT.jpg
  humanURL: https://311.columbus.gov/
  baseURL: https://csr.columbus.in.gov//csr/open311/v2/
  tags: 311, Open311
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/columbus-indiana-311/master/_listings/columbus-indiana-311/tokenstoken-id-response-format-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/columbus-indiana-311/master/_listings/columbus-indiana-311/tokenstoken-id-response-format-get-openapi.md
x-common:
- type: x-api-gallery
  url: http://chicago.illinois.311.api.gallery.streamdata.io
- type: x-open-311-feed
  url: http://csr.columbus.in.gov/csr/open311/v2/services.xml?jurisdiction_id=columbus.in.gov
- type: x-website
  url: https://311.columbus.gov/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---