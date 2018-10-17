# OpenDXL API Specification

The OpenDXL API Specification defines a standard interface description for
applications which connect to the
[McAfee Data Exchange Layer](http://www.mcafee.com/us/solutions/data-exchange-layer.aspx)
(DXL) messaging fabric. The specification provides a mechanism for describing the
API for DXL-based solutions, including:

* [Services](https://opendxl.github.io/opendxl-client-python/pydoc/dxlclient.service.html)
  that solutions register with a DXL fabric.
* [Events](https://opendxl.github.io/opendxl-client-python/pydoc/dxlclient.message.html#dxlclient.message.Event)
  that solutions send to a DXL fabric.
* [Requests](https://opendxl.github.io/opendxl-client-python/pydoc/dxlclient.message.html#dxlclient.message.Request)
  which can be made to a service through a DXL fabric (and the
  corresponding [responses](https://opendxl.github.io/opendxl-client-python/pydoc/dxlclient.message.html#dxlclient.message.Response)
  that the service produces).

The OpenDXL API Specification is heavily inspired by the work done in the
[OpenAPI Specification](https://github.com/OAI/OpenAPI-Specification) to
describe
[REST APIs](https://en.wikipedia.org/wiki/Representational_state_transfer).
Where possible, schema definitions in the OpenDXL API Specification
utilize corresponding definitions in the OpenAPI Specification. For example,
the core
[Schema Object](https://github.com/OAI/OpenAPI-Specification/blob/master/versions/2.0.md#schema-object)
from the OpenAPI Specification is used by the OpenDXL API Specification to
define the
[payload](https://opendxl.github.io/opendxl-client-python/pydoc/dxlclient.message.html#dxlclient.message.Message.payload)
for a DXL message.

## Draft Version - 0.1

The draft version of the OpenDXL API Specification is
[OpenDXL API Specification 0.1](versions/0.1.md).

## Schemas

[JSON Schema](https://json-schema.org) documents which can be used for
syntactic validation of an OpenDXL API document reside in the
[schemas](schemas) directory. The schema for the latest specification version
is [here](schemas/v0.1/schema.json).

## Examples

Current OpenDXL API document examples include:

* ACME [[json](examples/v0.1/json/acme.json)] [[yaml](examples/v0.1/yaml/acme.yaml)] -
  Simple example which utilizes each of the major schema components to describe
  an API - solutions, services, requests, and events.

* DXL Broker [[json](examples/v0.1/json/dxlbroker.json)] [[yaml](examples/v0.1/yaml/dxlbroker.yaml)] -
  Example which describes the API (requests and events) for a
  [DXL Broker](https://github.com/opendxl/opendxl-broker).

## LICENSE

Copyright 2018

Licensed under the Apache License, Version 2.0 (the "License"); you may not use
this file except in compliance with the License. You may obtain a copy of the
License at:

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed
under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR
CONDITIONS OF ANY KIND, either express or implied. See the License for the
specific language governing permissions and limitations under the License.
