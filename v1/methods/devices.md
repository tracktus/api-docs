##### GET `/devices`

    {
      "stat": "OK",
      "devices": [
        {
          "id": "118c735f-49e6-4494-9907-16151e150dc4",
          "productESN": "8875643",
          "productIMEI": "322099011761481",
          "productType": "MAXTRACK_MXT140",
          "metas": {
            "antenna": "external"
          }
        },
        ...
      ]
    }
    
    
##### GET `/devices/:id`

    {
      "stat": "OK",
      "device": {
        "id": "118c735f-49e6-4494-9907-16151e150dc4",
        "productESN": "8875643",
        "productIMEI": "322099011761481",
        "productType": "MAXTRACK_MXT140",
        "metas": {
          "antenna": "external"
        }
      }
    }
    
##### POST `/devices`

###### body

    {
      "id": "118c735f-49e6-4494-9907-16151e150dc4",
      "productESN": "8875643",
      "productIMEI": "322099011761481",
      "productType": "MAXTRACK_MXT140",
      "metas": {
        "Antenna": "External"
      }
    }
    
  parameter | type | required
  --------- | ---- | ---------
  `productESN` | `string` | X
  `productIMEI` | `string` | X
  `productType` | `string` | ✓
  `metas` | `object` | X

  > It's required to have specified at least one of the parameters `ProductESN` or `ProductIMEI`

###### result

    {
      "id": "118c735f-49e6-4494-9907-16151e150dc4",
      "productESN": "8875643",
      "productIMEI": "322099011761481",
      "productType": "MAXTRACK_MXT140",
      "metas": {
        "Antenna": "External"
      }
    }

##### PUT `/devices/:id`

###### body

    {
      "productIMEI": "322099011761482"
    }
    
  parameter | type | required
  --------- | ---- | ---------
  `productESN` | `string` | X
  `productIMEI` | `string` | X
  `productType` | `string` | X
  `metas` | `object` | X
  
> The `metas` parameter is always merged to the one stored, to delete a meta from the store, type the meta key with `null` value.

###### result

    {
      "stat": "OK",
      "device": {
        "id": "118c735f-49e6-4494-9907-16151e150dc4",
        "productESN": "8875643",
        "productIMEI": "322099011761482",
        "productType": "MAXTRACK_MXT140",
        "metas": {
          "Antenna": "External"
        }
      }
    }
    
##### DEL `/devices/:id`

This request will delete the device 
