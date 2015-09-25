#Errors

<aside class="notice">When there's an error you'll receive a response with a error object
containing an id
</aside>


>Example

```json
{
    "error": {
        "id": "bad_filter",
        "message": "ptref : Filters: Unable to find object"
    }
}
```



Code 40x
--------

This errors appears when there is an error in the request

The are two possible 40x http codes :

-   Code 404:

| Error id                     | Description                                                                |
|------------------------------|----------------------------------------------------------------------------|
| date\_out\_of\_bounds        | When the given date is out of bounds of the production dates of the region |
| no\_origin                   | Couldn't find an origin for the journeys                                   |
| no\_destination              | Couldn't find an destination for the journeys                              |
| no\_origin\_nor\_destination | Couldn't find an origin nor a destination for the journeys                 |
| unknown\_object              | As it's said                                                               |

-   Code 400:

| Error id          | Description                             |
|-------------------|-----------------------------------------|
| bad\_filter       | When you use a custom filter            |
| unable\_to\_parse | When you use a mal-formed custom filter |

Code 50x
--------

Ouch. Technical issue :/

Code 204
--------

When your request is good but we are not able to find a journey