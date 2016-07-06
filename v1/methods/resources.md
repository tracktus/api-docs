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

##### GET `/resources/:id/statuses`

    {
      "stat": "OK",
      "statuses": [
        {
          "device": "118c735f-49e6-4494-9907-16151e150dc4",
          "timestamp": "2016-05-11T21:07:27Z",
          "latitude": -29.850494,
          "longitude": -51.150692,
          "course": 95,
          "speed": 0,
          "ignition": false,
          "blocked": false,
          "panic": false,
          "mileage": 128351,
          "hourmeter": 14182.5,
          "gps": {
            "valid": true,
            "satellites": 10
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
  `devices` | `array<string>` | ✓
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
  `devices` | `array<string>` | X
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
