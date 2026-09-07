# Authentication

## Overview

The Payment API uses API key authentication to verify requests.

Authentication is required for all API requests.

## API Key

An API key is a unique value that identifies an application when it makes a request to the API.

Include the API key in the Authorization header of every request.

Example:

```http
Authorization: Bearer YOUR_API_KEY
```

## Example Request

The following example shows how an application can request payment information:

```http
GET /v1/payments/PAY12345
Authorization: Bearer YOUR_API_KEY
```

## Security

Keep your API key secure.

Never:

* Share your API key with other people.
* Publish your API key on GitHub.
* Put a real API key directly in your source code.
* Include a real API key in screenshots or documentation.

For this documentation project, `YOUR_API_KEY` is only an example value.
