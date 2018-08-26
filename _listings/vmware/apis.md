---
name: VMWare
x-slug: vmware
description: At VMware, we believe that software has the power to unlock new opportunities
  for people and our planet. We look beyond the barriers of compromise to engineer
  new ways to make technologies work together seamlessly. Our software forms a digital
  foundation that powers the apps, services and experiences that are transforming
  the world.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/VMware_logo.png
x-kinRank: "8"
x-alexaRank: "0"
tags: VMWare
created: "2018-08-26"
modified: "2018-08-26"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/vmware/master/_listings/vmware/apis.md
specificationVersion: "0.14"
apis:
- name: vRealize Operations 6 - Get Report Definitions
  x-api-slug: apireportdefinitions-get
  description: Gets all - to get a single report ID, just add /<report def id>
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/VMware_logo.png
  humanURL: http://vmware.com
  baseURL: https://example.com//suite-api/api
  tags: Cloud, Compute, Service API, Relative Data, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/vmware/master/_listings/vmware/apireportdefinitions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/vmware/master/_listings/vmware/apireportdefinitions-get-openapi.md
- name: vRealize Operations 6 - Get Generated Reports
  x-api-slug: apireports-get
  description: |-
    You can check status of report runs this way.
    To get a specific generated report add /<report id>
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/VMware_logo.png
  humanURL: http://vmware.com
  baseURL: https://example.com//suite-api/api
  tags: Cloud, Compute, Service API, Relative Data, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/vmware/master/_listings/vmware/apireports-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/vmware/master/_listings/vmware/apireports-get-openapi.md
- name: vRealize Operations 6 - Get StatKeys for Resource and Load var
  x-api-slug: apiresourcesresourceidstatkeys-get
  description: |-
    Grabs CPU statKeys for a VM resource using the {{resourceId}} env var.
    Populates two env vars:
    cpuStatKeys for GET stats for small requests (1 to ~10 VMs)
    cpuStatKeysJSON for POST stats for large requests (use in conjunction with {{resourceIds}}
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/VMware_logo.png
  humanURL: http://vmware.com
  baseURL: https://example.com//suite-api/api
  tags: Cloud, Compute, Service API, Relative Data, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/vmware/master/_listings/vmware/apiresourcesresourceidstatkeys-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/vmware/master/_listings/vmware/apiresourcesresourceidstatkeys-get-openapi.md
x-common:
- type: x-blog
  url: https://blogs.vmware.com/
- type: x-blog-rss
  url: http://blogs.vmware.com/all-vmware-blogs/wprss
- type: x-github
  url: https://github.com/VMware
- type: x-twitter
  url: https://twitter.com/VMware
- type: x-website
  url: http://vmware.com
- type: x-api-gallery
  url: http://visage.cloud.api.gallery.streamdata.io
- type: x-api-stack
  url: http://vmware.stack.network
- type: x-curated-source
  url: https://blogs.vmware.com/vcloud/2015/12/vmware-vcloud-air-network-compliance-spotlight-hipaa.html
- type: x-website
  url: https://www.vmware.com
- type: x-branding
  url: https://www.vmware.com/brand/our-brand.html
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---