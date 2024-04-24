# GEWISDB Typescript client
Typescript client for the GEWISDB API

## Description
This repository contains the client for the GEWISDB API. It is built using TypeScript and Axios, and utilizes the Swagger API specification for generating code.

## Installation
To install and use this client, follow these steps:
1. Clone the repository: `git clone https://github.com/GEWIS/gewisdb-ts-client.git`
2. Install dependencies: `npm install`

## Usage
To build the client, run `npm run gen-build`
This will first generate the TypeScript code under ./src and then generate the necessary files in the `dist/` directory.

## Example Usage

```typescript
import {Configuration, MembersApi} from "gewisdb-ts-client";

const apiKey = 'API_KEY'
const basePath = 'https://database.test.gewis.nl/api'

const configuration = new Configuration({basePath, accessToken: () => apiKey});

const membersApi = new MembersApi(configuration);
membersApi.membersGet().then((res) => {
  console.log(res.data);
}).catch((err) => {
  console.error(err);
});
```

## Contributing
Contributions are welcome! If you encounter any issues or have suggestions for improvements, please open an issue on the [issue tracker](https://gitlab.com/sudosos/sudosos-client/issues).
