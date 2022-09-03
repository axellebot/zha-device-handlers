# Lixee

- [Lixee](#lixee)
  - [Introduction](#introduction)
  - [Helpers](#helpers)
  - [Devices](#devices)
    - [ZLinky_TIC](#zlinky_tic)
      - [Firmware < 0x00000005 ❌](#firmware--0x00000005-)
      - [Firmware 0x00000006 ❌](#firmware-0x00000006-)

## Introduction

The purpose of this file is to list all Zigbee capable device from Lixee manufacturer, the status of their potential quirk, their basic zigbee infos and more.

All devices are listed alphabetically based on the Zigbee `model (0x0005)` attribute from `Basic (0x0000)` cluster.

All quirk infos should remain in basecode.

Status :

- ✅ : Supported
- ❌ : Not supported
- 🆗 : No quirk needed
- ❔ : Unknown

## Helpers

Device signature can be acquired by clicking on the "Zigbee Device Signature" button in the device settings view

## Devices

### ZLinky_TIC

#### Firmware < 0x00000005 ❌

#### Firmware 0x00000006 ❌

<details>
    <summary>Device signature</summary>

```json
{
  "node_descriptor": "NodeDescriptor(logical_type=<LogicalType.Router: 1>, complex_descriptor_available=0, user_descriptor_available=0, reserved=0, aps_flags=0, frequency_band=<FrequencyBand.Freq2400MHz: 8>, mac_capability_flags=<MACCapabilityFlags.AllocateAddress|RxOnWhenIdle|MainsPowered|FullFunctionDevice: 142>, manufacturer_code=4151, maximum_buffer_size=127, maximum_incoming_transfer_size=100, server_mask=11264, maximum_outgoing_transfer_size=100, descriptor_capability_field=<DescriptorCapability.NONE: 0>, *allocate_address=True, *is_alternate_pan_coordinator=False, *is_coordinator=False, *is_end_device=False, *is_full_function_device=True, *is_mains_powered=True, *is_receiver_on_when_idle=True, *is_router=True, *is_security_capable=False)",
  "endpoints": {
    "1": {
      "profile_id": 260,
      "device_type": "0x0053",
      "in_clusters": [
        "0x0000",
        "0x0003",
        "0x0702",
        "0x0b01",
        "0x0b04",
        "0xff66"
      ],
      "out_clusters": ["0x0019"]
    },
    "242": {
      "profile_id": 41440,
      "device_type": "0x0061",
      "in_clusters": ["0x0021"],
      "out_clusters": ["0x0021"]
    }
  },
  "manufacturer": "LiXee",
  "model": "ZLinky_TIC",
  "class": "zigpy.device.Device"
}
```

</details>

<details>
    <summary>zha_toolkit.scan_device</summary>

```json
{
  "ieee": "OMITTED",
  "nwk": "OMITTED",
  "model": "ZLinky_TIC",
  "manufacturer": "LiXee",
  "manufacturer_id": "0x4151",
  "endpoints": [
    {
      "id": 1,
      "device_type": "0x0053",
      "profile": "0x0104",
      "in_clusters": {
        "0x0000": {
          "cluster_id": "0x0000",
          "title": "Basic",
          "name": "basic",
          "attributes": {},
          "commands_received": {},
          "commands_generated": {}
        },
        "0x0003": {
          "cluster_id": "0x0003",
          "title": "Identify",
          "name": "identify",
          "attributes": {},
          "commands_received": {},
          "commands_generated": {}
        },
        "0x0702": {
          "cluster_id": "0x0702",
          "title": "Metering",
          "name": "smartenergy_metering",
          "attributes": {},
          "commands_received": {},
          "commands_generated": {}
        },
        "0x0b01": {
          "cluster_id": "0x0b01",
          "title": "Meter Identification",
          "name": "meter_id",
          "attributes": {},
          "commands_received": {},
          "commands_generated": {}
        },
        "0x0b04": {
          "cluster_id": "0x0b04",
          "title": "Electrical Measurement",
          "name": "electrical_measurement",
          "attributes": {},
          "commands_received": {},
          "commands_generated": {}
        },
        "0xff66": {
          "cluster_id": "0xff66",
          "title": "Manufacturer Specific",
          "name": "manufacturer_specific",
          "attributes": {},
          "commands_received": {},
          "commands_generated": {}
        }
      },
      "out_clusters": {
        "0x0019": {
          "cluster_id": "0x0019",
          "title": "Ota",
          "name": "ota",
          "attributes": {},
          "commands_received": {},
          "commands_generated": {}
        }
      }
    },
    {
      "id": 242,
      "device_type": "0x0061",
      "profile": "0xa1e0"
    }
  ]
}
```

</details>
