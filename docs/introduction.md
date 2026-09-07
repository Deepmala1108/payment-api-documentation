# Introduction

## Overview

The Payment API is a sample REST API that allows applications to create
and manage payment transactions.

This documentation is designed for developers who want to integrate
payment functionality into their applications.

## Base URL

All API requests are sent to the following base URL:

https://api.example.com/v1

## Available Operations

The Payment API provides the following operations:

- Create a payment
- Retrieve payment details
- Check payment status
- Request a refund
- Receive payment notifications through webhooks

## Request Format

The API uses JSON for request and response data.

Example:

```json
{
  "amount": 1000,
  "currency": "INR",
  "customer_id": "CUS12345"
}
