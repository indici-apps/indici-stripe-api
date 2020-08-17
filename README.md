# indici-stripe-api (only to create token)

Little Stripe library for React-Native.

### Installation
```bash
$ npm i indici-stripe-api --save
```
or
```bash
$ yarn add indici-stripe-api
```

## Roadmap
- include a payment form component
- include react-native-awesome-card-io
- a new server project to keep secret

## Setup

### Security issue (`fixed since 0.1.0`)

https://github.com/indici-apps/indici-stripe-api/issues

### Stripe API

This lib need a Stripe API Key
```JavaScript
import Stripe from 'react-native-stripe-api';

const apiKey = '<your Stripe API Key>';
const client = new Stripe(apiKey);

// Create a Stripe token with new card infos
const token = await client.createToken({
       number: '4242424242424242' ,
       exp_month: '09', 
       exp_year: '18', 
       cvc: '111',
       address_zip: '12345'
    });



```

## Functions

| Name | Return Type | Arguments | Description |
| --- | --- | --- | --- |
| createToken | Promise |<ul><li>cardNumber: string</li> <li>expMonth: string</li><li>expYear: string</li><li>cvc: string</li></ul>| Create a new token (equivalent of a new card) |
| 

> made with ♥




