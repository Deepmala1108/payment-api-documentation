# Create Payment

Creates a new payment transaction.

## Endpoint

```http
POST /v1/payments
```

## Authentication

Authentication is required to create a payment.

Include your API key in the request header:

```http
Authorization: Bearer YOUR_API_KEY
```

## Request Headers

| Header        | Type   | Required | Description                |
| ------------- | ------ | -------- | -------------------------- |
| Authorization | String | Yes      | API authentication key     |
| Content-Type  | String | Yes      | Must be `application/json` |

## Request Body

The request body contains information about the payment.

```json
{
  "amount": 1000,
  "currency": "INR",
  "customer_id": "CUS12345"
}
```

### Request Parameters

| Parameter   | Type   | Required | Description                |
| ----------- | ------ | -------- | -------------------------- |
| amount      | Number | Yes      | Payment amount             |
| currency    | String | Yes      | Three-letter currency code |
| customer_id | String | Yes      | Unique customer identifier |

## Example Request

```http
POST /v1/payments
Authorization: Bearer YOUR_API_KEY
Content-Type: application/json
```

```json
{
  "amount": 1000,
  "currency": "INR",
  "customer_id": "CUS12345"
}
```

## Successful Response

A successful request returns the details of the newly created payment.

```json
{
  "id": "PAY12345",
  "status": "successful",
  "amount": 1000,
  "currency": "INR",
  "customer_id": "CUS12345"
}
```

## HTTP Status Code

A successful request returns:

```text
201 Created
```

This indicates that a new payment resource was created successfully.

## Errors

If the request is invalid, the API may return an error response.

Example:

```json
{
  "error": {
    "code": "INVALID_AMOUNT",
    "message": "The payment amount must be greater than zero."
  }
}
```

## Notes

This is a sample API created for documentation practice.

The API endpoint and responses in this project are examples and are not connected to a real payment service.
