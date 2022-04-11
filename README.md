# iiif-templates
The repository is comprised of:
1. Various templates designed to be used to serialise resources compatible with the [International Image Interoperability Framework (IIIF) Presentation API 3.0](https://iiif.io/api/presentation/3.0/) based on use cases hosted by DaSCH
2. An ActivityStreams Template compatible with the [IIIF Change Discovery API 1.0](https://iiif.io/api/discovery/1.0/)

## IIIF Presentation API 3.0 Resources 
On the table below are the five main types of resources, their relation to the [`kb:Representation` subclass](https://docs-api.dasch.swiss/02-knora-ontologies/knora-base/#representations), the type of IIIF Resource (either `Manifest` or `Collection`) as well as the template in JSON-LD.
| **Type**                  | **`kb:Representation` subclass** | **IIIF Resource** | **Template**                                     |
|---------------------------|----------------------------------|-------------------|--------------------------------------------------|
| Single image              | `StillImageRepresentation`       | Manifest          | [boilerplate 1](boilerplates/boilerplate01.json) |
| Series of images          | `StillImageRepresentation`       | Manifest          |                                                  |
| Audio                     | `AudioRepresentation`            | Manifest          |                                                  |
| Video                     | `MovingImageRepresentation`      | Manifest          |                                                  |
| 3D representation         | `DDDrepresentation`              | Manifest          |                                                  |
| Collection of Manifests   | -                                | Collection        |                                                  |
| Collection of Collections | -                                | Collection        |                                                  |

## ActivityStreams Template Endpoint
TBD
