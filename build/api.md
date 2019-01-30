# FX2
# Group MIDIControl

## 取得所有 KNOB 的 MIDI 設定 [GET /QueryFxAssignments]
+ Parameters
  + effect_index (object, required)
+ Response 200
  ```
    [
      {
        label: 'Bass',
        cc_number: -1, //cc_number 為 -1 代表未 assign，0 ~ 127 為正常 cc_number
        advanced_options: [ //每個 midi 都要有 advanced_options
          {
            label: 'On',
            start: 1,
            end: 60
          },
          {
            label: 'Off',
            start: 80,
            end: 110
          }
        ]
      },
      { ... }
    ]
  ```

## 設定 KNOB 的 CC NUMBER [POST /SetCcNumber]
+ Parameters
  + effect_index (object, required)
  + knob_index (number, required)
  + cc_number (number, required)

## 開始 MIDI LEARN [POST /StartMidiLearn]
+ Parameters
  + effect_index (object, required)
  + knob_index (number, required)

# 設定 KNOB 的 ADVANCED OPTIONS [POST /SetAdvancedOptions]
+ Parameters
  + effect_index (object, required)
  + knob_index (number, required)
  + advanced_options: (array, required)
    ```
        [
          {
            label: 'On',
            start: 1,
            end: 60
          },
          {
            label: 'Off',
            start: 80,
            end: 110
            // 不傳 target_value
          }
        ]
    ```

## 將當前的 MIDI 改動存進 PRESET [POST /SaveMidiAssignmentsToPreset]
+ Parameters
  + effect_index (object, required)
