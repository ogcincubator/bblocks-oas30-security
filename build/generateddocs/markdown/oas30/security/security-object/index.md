
# Security Object Schema (Schema)

`ogc.oas30.security.security-object` *v0.1*

Schema for OpenAPI 3.0 security objects in OGC APIs

[*Status*](http://www.opengis.net/def/status): Under development

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
$id: https://example.com/schemas/definition-ref.schema.json
title: API Definition Locations
type: object
additionalProperties: false
required:
- definition
properties:
  definition:
    type: object
    description: Media-type keyed locations of the API definition.
    additionalProperties: false
    properties:
      application/json:
        type: string
        format: uri
        description: Absolute URI to the OpenAPI definition in JSON form.
      application/yaml:
        type: string
        format: uri
        description: Absolute URI to the OpenAPI definition in YAML form.
    anyOf:
    - required:
      - application/json
    - required:
      - application/yaml
examples:
- definition:
    application/json: https://myapiserver.com/oaslocation
- definition:
    application/yaml: https://myapiserver.com/oaslocation
- definition:
    application/json: https://myapiserver.com/oaslocation
    application/yaml: https://myapiserver.com/oaslocation

```

Links to the schema:

* YAML version: [schema.yaml](https://ogcincubator.github.io/bblocks-oas30-security/build/annotated/oas30/security/security-object/schema.json)
* JSON version: [schema.json](https://ogcincubator.github.io/bblocks-oas30-security/build/annotated/oas30/security/security-object/schema.yaml)

## Sources

* [OpenAPI 3.0 Security Requirement Object](https://swagger.io/specification/v3/#security-requirement-object)
* [OpenAPI 3.0 Security Scheme Object](https://swagger.io/specification/v3/#security-scheme-object)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/ogcincubator/bblocks-oas30-security](https://github.com/ogcincubator/bblocks-oas30-security)
* Path: `_sources/security-object`

