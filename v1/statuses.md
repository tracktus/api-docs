##### GET `/statuses`

    {
      "stat": "OK",
      "statuses": [
        {
          "resource": {
            "id": "6a52e022-b05a-45c3-a7a5-ce399a269cb5",
            "name": "VK-0182 (Corolla)"
          },
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
    
    
##### GET `/resources/:id`

    {
      "stat": "OK",
      "status": {
        "resource": {
          "id": "6a52e022-b05a-45c3-a7a5-ce399a269cb5",
          "name": "VK-0182 (Corolla)"
        },
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
