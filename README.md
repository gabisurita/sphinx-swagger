# sphinx-swagger
Sphinx extension for automatically documenting Swagger 2.0 APIs.

**Usage**

Include extension in *conf.py*

    extensions = ['sphinx_swagger']

Add directive pointing to Swagger api-docs

    .. swaggerv2doc:: URL/swagger.json

For example    

    .. swaggerv2doc:: http://petstore.swagger.io/v2/swagger.json

If the Swagger description contains multiple tags, you can select a subset
for the documentation generation. For example, the following directive only
generates the documentation for the methods contained in tags **pet** and
**store**.

    .. swaggerv2doc:: http://petstore.swagger.io/v2/swagger.json
       pet
       store

**Note**

The old directive for Swagger 1.0 should still be usable. For example,

    .. swaggerdoc:: http://petstore.swagger.wordnik.com/api/api-docs/pet
    .. swaggerdoc:: http://petstore.swagger.wordnik.com/api/api-docs/user
    .. swaggerdoc:: http://petstore.swagger.wordnik.com/api/api-docs/store
