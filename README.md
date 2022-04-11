# iiif-templates
The repository is comprised of:
1. various templates designed to be used to serialise resources compatible with the [International Image Interoperability Framework (IIIF) Presentation API 3.0](https://iiif.io/api/presentation/3.0/) based on use cases hosted by DaSCH
2. An ActivityStreams Template compatible with the [IIIF Change Discovery API 1.0](https://iiif.io/api/discovery/1.0/)

## Types of resources
| **Type**          | **`kb:Representation` subclass** | **Template** |
|-------------------|----------------------------------|--------------|
| Single image      | StillImageRepresentation         |              |
| Series of images  | StillImageRepresentation         |              |
| Audio             | AudioRepresentation              |              |
| Video             | MovingImageRepresentation        |              |
| 3D representation | DDDrepresentation                |              |
