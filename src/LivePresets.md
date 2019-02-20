# Group LivePresets

## GetPresetsList [GET /]
```
LivePresets.GetPresetsList(display_order)
```
+ Parameters
  + display_order (number)
+ Response 200
{
  "LivePresets": [
    {
      "display_order": 0,
      "meta": {
        "licenseTierReq": {
          "Fx2LE": false,
          "Fx2License": 0,
          "expansion_acoustic": false,
          "expansion_bass": false,
          "expansion_metal": false,
          "modern_vintage": false
        }
      }
    }
  ]
}

## GetBanksList [GET /]
```
LivePresets.GetBanksList()
```
+ Response 200
{
  "LiveBanks": [
    {
      "bank_folder": "AAAAAAAA-AAAA-AAAA-AAAA-AAAAAAAAAAAA",
      "bank_name": "Standard Low Gain",
      "display_order": 0,
      "is_factory": true
    }
  ]
}
