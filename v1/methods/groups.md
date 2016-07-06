##### GET `/groups`

    {
      "stat": "OK",
      "groups": [
        {
          "id": "6a52e022-b05a-45c3-a7a5-ce399a269cb5",
          "name": "Company 2"
        },
        ...
      ]
    }
    
    
##### GET `/groups/:id`

    {
      "stat": "OK",
      "group": {
        "id": "6a52e022-b05a-45c3-a7a5-ce399a269cb5",
        "name": "Company 2"
      }
    }
    
##### POST `/groups/:id`

###### body

    {
      "name": "Company 2"
    }
    
  parameter | type | required
  --------- | ---- | ---------
  `name` | `string` | ✓
  `meas` | `object` | X

###### result

    {
      "stat": "OK",
      "groups": {
        "id": "6a52e022-b05a-45c3-a7a5-ce399a269cb5",
        "name": "Company 2",
        "metas": {}
      }
    }

##### PUT `/groups/:id`

###### body

    {
      "name": "Company 3"
    }
    
  parameter | type | required
  --------- | ---- | ---------
  `name` | `string` | X
  `metas` | `object` | X
  
 > The `metas` parameter is always merged to the one stored, to delete a meta from the store, type the meta key with `null` value.

###### result

    {
      "stat": "OK",
      "group": {
        "id": "6a52e022-b05a-45c3-a7a5-ce399a269cb5",
        "name": "Company 3",
        "metas": {}
      }
    }
    
##### DEL `/groups/:id`

This request will delete the resource
