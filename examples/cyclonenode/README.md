# Cyclone Node

## Sample Packet

The following packet is defined to allow Cyclone Nodes to be the network gateway for Cyclone Sensors.

### Discussion CS

The unique element in the packet is the parametername "cs". CS data elements are expected to have a JSON, or "j", payload with the following data:

* JSON payload
  + n the sensor name, required, factory set variable
  + p the parameter name, required
  + v the numeric value for the parameter, optional
  + a the ascii value for the parameter, optional
  + h the hex value for the parameter, optional
  + j the JSON value for the parameter, optional

### Short Example

```json
{
  "h":{
    "n":"CN0000",
    "t":"2019-09-04T13:33:23.003Z"
  },
  "d":[
    {
      "n":"cs",
      "j":{
          "n":"CS0000",
          "p":"Val1",
          "v": 1.34
      }
    }
  ]
}
```

### Full Example

<https://github.com/RadioBro/ICD/blob/master/examples/cyclonenode/cyclonenodeexample.json

```json
{
  "h":{
    "n":"CN0000",
    "t":"2019-09-04T13:33:23.003Z"
  },
  "d":[
    {
      "n":"state",
      "v": 1
    },
    {
      "n":"cs",
      "j":{
          "n":"CS0000",
          "p":"Val1",
          "v": 1.34
      }
    },
    {
      "n":"cs",
      "j":{
        "n":"CS0000",
        "p":"Temp1",
        "v": 24.1
      }
    },
    {
      "n":"cs",
      "j":{
        "n":"CS0001",
        "p":"Val1",
        "v": 1.25
      }
    },
    {
      "n":"cs",
      "j":{
        "n":"CS0001",
        "p":"Temp1",
        "v": 23.2
      }
    }
  ]
}
```