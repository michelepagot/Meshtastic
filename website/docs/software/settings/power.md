---
id: power
title: Power Settings
sidebar_label: Power
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';


## Overview



## Settings

| Setting | Acceptable Values | Default |
| :-----: | :---------------: | :-----: |
| charge_current | `MAUnset`, `MA100`, `MA190`, `MA280`, `MA360`, `MA450`, `MA550`, `MA630`, `MA700`, `MA780`, `MA880`, `MA960`, `MA1000`, `MA1080`, `MA1160`, `MA1240`, `MA1320`: | `MAUnset` |
| is_low_power | `true`, `false` | `false` | If set, we are powered from a low-current source (i.e. solar), so even if it looks like we have power flowing in we should try to minimize power consumption as much as possible. YOU DO NOT NEED TO SET THIS IF YOU'VE set is_router (it is implied in that case). |
| is_router | `true`, `false` | `false` |
| ls_secs | `integer` (seconds) | `0` (see note) |
| mesh_sds_timeout_secs | `integer` (seconds) | `0` |
| min_wake_secs | `integer` (seconds) | `0` |
| phone_sds_timeout_sec | `integer` (seconds) | `0` | Power management state machine option. See the [power page](other/power) for details. 0 for default of two hours, MAXUINT for disabled |
| phone_timeout_secs | `integer` (seconds) | `0` |
| screen_on_secs | `integer` (seconds) | `0` |
| sds_secs | `integer` (seconds) | `0` |
| send_owner_interval | `integer` (seconds) | `4` |
| wait_bluetooth_secs | `integer` (seconds) | `0` |

:::note
When you the following settings to `0` they assume the following defaults:
- `ls_secs`: 1 hour
- `mesh_sds_timeout_secs`: 2 hours
- `min_wake_secs`: 10 seconds
- `phone_sds_timeout_sec`: 2 hours
- `phone_timeout_secs`: 15 minutes
- `screen_on_secs`: 1 minute
- `sds_secs`: 1 year
- `wait_bluetooth_secs`: 1 minute
:::

### charge_current

Sets the current of the battery charger

### is_low_power

If set, we are powered from a low-current source (i.e. solar), so even if it looks like we have power flowing in we should try to minimize power consumption as much as possible. YOU DO NOT NEED TO SET THIS IF YOU'VE set is_router (it is implied in that case).

### is_router

Are we operating as a router. Changes behavior in the following ways: The device will only sleep for critically low battery level (i.e. always tries to stay alive for the mesh) In the future routing decisions will preferentially route packets through nodes with this attribute (because assumed good line of sight)

### ls_secs

Power management state machine option. See the [power page](../other/power) for details. 0 for default of 3600

### mesh_sds_timeout_secs

Power management state machine option. See the [power page](../other/power) for details. 0 for default of two hours, MAXUINT for disabled

### min_wake_secs

Power management state machine option. See the [power page](../other/power)for details. 0 for default of 10 seconds

### phone_sds_timeout_sec

Power management state machine option. See the [power page](../other/power) for details. 0 for default of two hours, MAXUINT for disabled

### phone_timeout_secs

Power management state machine option. See the [power page](../other/power) for details. 0 for default of 15 minutes

### screen_on_secs

Power management state machine option. See the [power page](../other/power) for details. 0 for default of one minute.

### sds_secs

Power management state machine option. See the [power page](../other/power) for details. 0 for default of one year

### send_owner_interval

Send our owner info at least this often (also we always send once at boot - to rejoin the mesh)

### wait_bluetooth_secs

Power management state machine option. See the [power page](../other/power) for details. 0 for default of 1 minute

## Details

## Examples

<Tabs
  groupId="settings"
  defaultValue="cli"
  values={[
    {label: 'CLI', value: 'cli'},
    {label: 'Android', value: 'android'},
  ]}>
  <TabItem value="cli">

  TODO

  </TabItem>
  <TabItem value="android">

  TODO

  </TabItem>
</Tabs>
