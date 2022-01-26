To perform the tests, **you must have at least two users:** a seller and a buyer.

Execute the following curl to generate a test user:

```curl
curl -X POST \
-H "Content-Type: application/json" \
-H 'Authorization: Bearer PROD_ACCESS_TOKEN' \
"https://api.mercadopago.com/users/test_users" \
-d '{"site_id":"[FAKER][GLOBALIZE][UPPER_SITE_ID]"}'
```


The answer will have a structure similar to the following example:

```json
{
  "id": 123,
  "nickname": "TEST45I5GYIH",
  "password": "qatest6730",
  "site_status": "active",
  "site_id": "MLA",
  "email": "test_user_123@testuser.com",
  "date_created": "2021-11-04T12:02:35Z",
  "date_last_updated": "2021-11-04T12:02:35Z"
}
```

>WARNING
>
> Important
>
> * You can generate up to 10 test user accounts simultaneously. Therefore, we recommend you _save each email and password._
> * Test users expire after 60 days without activity in Mercado Pago.
> * Both buyer and seller must be test users.