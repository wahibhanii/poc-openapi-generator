# POC for OpenAPI client generator

## Goal
1. Generate client from OpenAPI spec

## POC
### Generating typescript node client
Generating typescript node client using [OpenAPITools/openapi-generator-cli](https://github.com/OpenAPITools/openapi-generator)

They offer multiple ways to generate the client (java maven, homebrew, CLI tool), but for this POC, I'm going to use [NPM package mode](https://www.npmjs.com/package/@openapitools/openapi-generator-cli#package-mode).

1. Install
```
# install the latest version of "openapi-generator-cli"
npm install @openapitools/openapi-generator-cli -D
```
2. add script
Add script to your package.json, example:
```
"scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "generate-node-client": "openapi-generator generate -i spec/openapi.json -g typescript-node -o generated-sources/openapi/typescript-node --additional-properties=\"ngVersion=6.1.7\""
  }
```
3. Run script
```
npm run generate-node-client
```
