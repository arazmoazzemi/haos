# Home Assistant Frontend Theme Update


- Install studio code server 

- Goto left panel and click on studio code server 

- Goto *config* path and open *configuration.yaml* file

```code
# Loads default set of integrations. Do not remove.
default_config:

# Load frontend themes from the themes folder
frontend:
  themes: !include_dir_merge_named themes

automation: !include automations.yaml
script: !include scripts.yaml
scene: !include scenes.yaml

```

NOTE! Considering __themes: !include_dir_merge_named themes__ line, Create theme folder on, And create your new config.yaml, For example:

