##### GET `/eligo/billing/monitoring`

    {
      "stat": "OK",
      "response": [
        {
          "id": "118c735f",
          "quantity": 300,
          "unitCost": 10.2,
          "discountSteps": [
            [100, 3.2],
            [200, 3.8]
          ],
          "totalCost": 2420.0,
          "totalDiscount": 640.0,
          "attachmentDetailsUri": "http://nat.frota.online/fatura/fatura-monitoramento.php?id=118c735f"
        },
        ...
      ]
    }
    

###### response

  path | type | required | description
  --------- | ---- | --------- | -----
  `response[].id` | `string` | X | The contract id
  `response[].quantity` | `int` | X | Quantity of items
  `response[].unitCost` | `float` | X | Cost per unit
  `response[].discountStops` | `Array<Array<int, float>>` | X | Discount steps on each item, position 0 is the step, beyond the value specified the discount should be aplied for every unit, value and position 2 is the discount
  `response[].totalCost` | `float` | X | Total cost with discount applied
  `response[].totalDiscount` | `float` | X | The total discount applied to the total cost
  `response[].attachmentDetailsUri` | `string` | X | The detailed billing PDF URI for download
  
  
##### GET `/eligo/billing/software`

    {
      "stat": "OK",
      "response": [
        {
          "id": "118c735f",
          "quantity": 300,
          "unitCost": 10.2,
          "discountSteps": [
            [100, 3.2],
            [200, 3.8]
          ],
          "totalCost": 2420.0,
          "totalDiscount": 640.0,
          "attachmentDetailsUri": "http://nat.frota.online/fatura/fatura-sistema.php?id=118c735f"
        },
        ...
      ]
    }
    

###### response

  path | type | required | description
  --------- | ---- | --------- | -----
  `response[].id` | `string` | X | The contract id
  `response[].quantity` | `int` | X | Quantity of items
  `response[].unitCost` | `float` | X | Cost per unit
  `response[].discountStops` | `Array<Array<int, float>>` | X | Discount steps on each item, position 0 is the step, beyond the value specified the discount should be aplied for every unit, value and position 2 is the discount
  `response[].totalCost` | `float` | X | Total cost with discount applied
  `response[].totalDiscount` | `float` | X | The total discount applied to the total cost
  `response[].attachmentDetailsUri` | `string` | X | The detailed billing PDF URI for download
  
  
##### GET `/eligo/billing/m2m`

    {
      "stat": "OK",
      "response": [
        {
          "id": "118c735f",
          "quantity": 300,
          "unitCost": 10.2,
          "discountSteps": [
            [100, 3.2],
            [200, 3.8]
          ],
          "totalCost": 2420.0,
          "totalDiscount": 640.0,
          "attachmentDetailsUri": "http://nat.frota.online/fatura/fatura-simcards.php?id=118c735f"
        },
        ...
      ]
    }
    

###### response

  path | type | required | description
  --------- | ---- | --------- | -----
  `response[].id` | `string` | X | The contract id
  `response[].quantity` | `int` | X | Quantity of items
  `response[].unitCost` | `float` | X | Cost per unit
  `response[].discountStops` | `Array<Array<int, float>>` | X | Discount steps on each item, position 0 is the step, beyond the value specified the discount should be aplied for every unit, value and position 2 is the discount
  `response[].totalCost` | `float` | X | Total cost with discount applied
  `response[].totalDiscount` | `float` | X | The total discount applied to the total cost
  `response[].attachmentDetailsUri` | `string` | X | The detailed billing PDF URI for download
