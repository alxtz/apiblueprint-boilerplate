# Group MIDIControl

## QueryFxAssignments [GET /]
```
MIDIControl.QueryFxAssignments(effect_index, cc_number)
```
+ Parameters
  + effect_index (object)
+ Response 200
[
  {
    "label": "Bass",
    "cc_number": -1,
    "advanced_options": [
      {
        "label": "On",
        "start": 1,
        "end": 60
      },
      {
        "label": "Off",
        "start": 80,
        "end": 110
      }
    ]
  }
]

## SetCcNumber [POST /]
```
MIDIControl.SetCcNumber(effect_index, knob_index, cc_number)
```
+ Parameters
  + effect_index (object)
  + knob_index (number)
  + cc_number (number)

## StartMidiLearn [POST /]
```
MIDIControl.StartMidiLearn(effect_index, knob_index)
```
+ Parameters
  + effect_index (object)
  + knob_index (number)

## SetAdvancedOptions [POST /]
```
MIDIControl.SetAdvancedOptions(effect_index, knob_index, advanced_options)
```
+ Parameters
  + effect_index (object)
  + knob_index (number)
  + advanced_options (array)

## SaveMidiAssignmentsToPreset [POST /]
```
MIDIControl.SetAdvancedOptions(effect_index)
```
+ Parameters
  + effect_index (object)
