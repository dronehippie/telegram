Drone plugin send build notifications to Telegram. You are able to submit
messages on success or failure to specific accounts or groups.

## Examples

```yaml
kind: pipeline
name: default

steps:
- name: step name
  image: dronehippie/telegram:1
  settings: []
```

## Parameters

dummy
: dummy
