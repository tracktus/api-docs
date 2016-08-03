##### GET `/statuses`

    {
      "stat": "OK",
      "statuses": [
        {
          "resource": {
            "id": "6a52e022-b05a-45c3-a7a5-ce399a269cb5",
            "name": "VK-0182 (Corolla)"
          },
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
        },
      ...]
    }

##### GET `/resources/:id/status`

This request contains the actual status of the resouce with the status merged from all devices.

    {
      "stat": "OK",
      "status": {
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

##### GET `/resources/:id/statuses`

This request contains the actual status of each device related to the resource.

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
        },
      ...]
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
