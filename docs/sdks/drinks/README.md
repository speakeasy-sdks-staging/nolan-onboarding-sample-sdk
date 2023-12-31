# Drinks
(*drinks*)

## Overview

The drinks endpoints.

### Available Operations

* [getDrink](#getdrink) - Get a drink.
* [listDrinks](#listdrinks) - Get a list of drinks.

## getDrink

Get a drink by name, if authenticated this will include stock levels and product codes otherwise it will only include public information.

### Example Usage

```typescript
import { TheSpeakeasyBar } from "The-Speakeasy-Bar";

(async() => {
  const sdk = new TheSpeakeasyBar({
    apiKey: "",
  });

  const res = await sdk.drinks.getDrink({
    name: "North District",
  });

  if (res.statusCode == 200) {
    // handle response
  }
})();
```

### Parameters

| Parameter                                                                | Type                                                                     | Required                                                                 | Description                                                              |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| `request`                                                                | [operations.GetDrinkRequest](../../models/operations/getdrinkrequest.md) | :heavy_check_mark:                                                       | The request object to use for the request.                               |
| `config`                                                                 | [AxiosRequestConfig](https://axios-http.com/docs/req_config)             | :heavy_minus_sign:                                                       | Available config options for making requests.                            |


### Response

**Promise<[operations.GetDrinkResponse](../../models/operations/getdrinkresponse.md)>**


## listDrinks

Get a list of drinks, if authenticated this will include stock levels and product codes otherwise it will only include public information.

### Example Usage

```typescript
import { TheSpeakeasyBar } from "The-Speakeasy-Bar";
import { DrinkType } from "The-Speakeasy-Bar/dist/sdk/models/shared";

(async() => {
  const sdk = new TheSpeakeasyBar({
    apiKey: "",
  });

  const res = await sdk.drinks.listDrinks({});

  if (res.statusCode == 200) {
    // handle response
  }
})();
```

### Parameters

| Parameter                                                                    | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `request`                                                                    | [operations.ListDrinksRequest](../../models/operations/listdrinksrequest.md) | :heavy_check_mark:                                                           | The request object to use for the request.                                   |
| `config`                                                                     | [AxiosRequestConfig](https://axios-http.com/docs/req_config)                 | :heavy_minus_sign:                                                           | Available config options for making requests.                                |


### Response

**Promise<[operations.ListDrinksResponse](../../models/operations/listdrinksresponse.md)>**

