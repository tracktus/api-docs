##### GET `/resources`

    {
      "stat": "OK",
      "resources": [
        {
          "id": "6a52e022-b05a-45c3-a7a5-ce399a269cb5",
          "type": "VEHICLE_BUS",
          "name": "IVK-0182",
          "devices": [
            "118c735f-49e6-4494-9907-16151e150dc4"
          ],
          "metas": {
            "Data Instalação": "10/02/2016"
          }
        },
        ...
      ]
    }
    
    
##### GET `/resources/:id`

    {
      "stat": "OK",
      "resource": {
        "id": "6a52e022-b05a-45c3-a7a5-ce399a269cb5",
        "type": "VEHICLE_BUS",
        "name": "IVK-0182",
        "devices": [
          "118c735f-49e6-4494-9907-16151e150dc4"
        ],
        "metas": {
          "Data Instalação": "10/02/2016"
        }
      }
    }
    
##### POST `/resources`

###### body

    {
      "type": "VEHICLE_BUS",
      "name": "IVK-0182",
      "devices": [
        "118c735f-49e6-4494-9907-16151e150dc4"
      ],
      "metas": {
        "Data Instalação": "10/02/2016"
      }
    }
    
  parameter | type | required
  --------- | ---- | ---------
  `name` | `string` | ✓
  `type` | `string<resourceType>` | ✓
  `metas` | `object` | X

###### result

    {
      "stat": "OK",
      "resource": {
        "id": "6a52e022-b05a-45c3-a7a5-ce399a269cb5",
        "type": "VEHICLE_BUS",
        "name": "IVK-0182",
        "devices": [
          "118c735f-49e6-4494-9907-16151e150dc4"
        ],
        "metas": {
          "Data Instalação": "10/02/2016"
        }
      }
    }

##### PUT `/resources/:id`

###### body

    {
      "name": "IVK-0182 (Corolla)"
    }
    
  parameter | type | required
  --------- | ---- | ---------
  `name` | `string` | X
  `metas` | `object` | X

> The `metas` parameter is always merged to the one stored, to delete a meta from the store, type the meta key with `null` value.

###### result

    {
      "stat": "OK",
      "resource": {
        "id": "6a52e022-b05a-45c3-a7a5-ce399a269cb5",
        "type": "VEHICLE_BUS",
        "name": "IVK-0182 (Corolla)",
        "devices": [
          "118c735f-49e6-4494-9907-16151e150dc4"
        ],
        "metas": {
          "Data Instalação": "10/02/2016"
        }
      }
    }
    
##### DEL `/resources/:id`

This request will delete the resource
