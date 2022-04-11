# iiif-templates
The repository is comprised of:
1. Various templates designed to be used to serialise resources compatible with the [International Image Interoperability Framework (IIIF) Presentation API 3.0](https://iiif.io/api/presentation/3.0/) based on use cases hosted by DaSCH
2. An ActivityStreams Template compatible with the [IIIF Change Discovery API 1.0](https://iiif.io/api/discovery/1.0/)

## IIIF Presentation API 3.0 Resources 
On the table below are the main types of resources that could be compliant with the IIIF Presentation API 3.0, which [`kb:Representation` subclass](https://docs-api.dasch.swiss/02-knora-ontologies/knora-base/#representations) the content has, which type of IIIF Resource they belong to (either `Manifest` or `Collection`) as well as the boilerplate in JSON-LD.
| **Type**                  | **`kb:Representation` subclass of the content** | **IIIF Resource** | **Boilerplate**                                     |
|---------------------------|----------------------------------|-------------------|--------------------------------------------------|
| Single image              | `StillImageRepresentation`       | Manifest          | [boilerplate 1](boilerplates/boilerplate01.json) |
| Series of images          | `StillImageRepresentation`       | Manifest          |                                                  |
| Audio                     | `AudioRepresentation`            | Manifest          |                                                  |
| Video                     | `MovingImageRepresentation`      | Manifest          |                                                  |
| 3D representation         | `DDDrepresentation`              | Manifest          |                                                  |
| Collection of Manifests   | -                                | Collection        |                                                  |
| Collection of Collections | -                                | Collection        |                                                  |

### Boilerplate elements

#### IIIF Manifest

1. Metadata about the IIIF resource (`context`, `id`, `type`)
2. Summary (`summary`)
3. Descriptive Metadata about the object
4. Rights Information (`rights`, `requiredStatement`)
5. Related links (`logo`,`homepage`, `seeAlso`, `provider`, `rendering`, `start`)
6. Presentation information (`viewing Direction`, `navDate`, `thumbnail`)
7. List of Canvases (`items` + `id`, `type`, `label` for each resource - see below)

_The `Canvas` represents an individual page or view and acts as a central point for assembling the different content resources that make up the display._

Here is a detailed view of the [first boilerplate](https://github.com/dasch-swiss/iiif-templates/blob/main/boilerplates/boilerplate01.json#L226):

```
    {
      "id": "https://pia-something.ch/iiif/boilerplate01/canvas/p1",
      "type": "Canvas",
      "label": {
    "none": [
      "SGV_12N_00001"
    ]
  },
      "height": 4190,
      "width": 4252,
      "items": [
        {
          "id": "https://pia-iiif.dhlab.unibas.ch/server/SGV_12N_00001/canvas/p1",
          "type": "Canvas",
          "label": {
          "none": [
            "SGV_12N_00001"
          ]
        },
          "height": 4252,
          "width": 4190,
          "items": [
            {
              "id": "https://pia-iiif.dhlab.unibas.ch/server/SGV_12N_00001/canvas/p1/1",
              "type": "AnnotationPage",
              "items": [
                {
                  "id": "https://pia-iiif.dhlab.unibas.ch/server/SGV_12N_00001/annotation/p0001-image",
                  "type": "Annotation",
                  "motivation": "painting",
                  "body": {
                    "id": "https://pia-iiif.dhlab.unibas.ch/SGV_12/SGV_12N_00001.jp2/full/max/0/default.jpg",
                    "type": "Image",
                    "format": "image/jpeg",
                    "height": 4252,
                    "width": 4190,
                    "service": [
                      {
                        "id": "https://pia-iiif.dhlab.unibas.ch/SGV_12/SGV_12N_00001.jp2",
                        "type": "ImageService3",
                        "profile": "level2"
                      }
                    ]
                  },
                  "target": "https://pia-iiif.dhlab.unibas.ch/server/SGV_12N_00001/canvas/p1/1"
                }
              ]
            }
          ]
        }
      ]
    }
```

#### IIIF Collection
The form for use cases 3 and 4 will have the following components:

1. Metadata about the IIIF resource (`context`, `id`, `type`)
2. Summary (`summary`)
3. Related links (`logo`, `provider`)
4. List of Manifests/Collections (`items` + `id`, `type`, `label` for each resource)


## ActivityStreams Template Endpoint
TBD
