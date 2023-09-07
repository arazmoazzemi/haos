type: iframe
url: https://www.youtube.com/embed/590MXisPeZE
aspect_ratio: '16:9'



------------------------------------------------------


type: entities
entities:
  - sensor.islamic_prayer_times_fajr_prayer
  - sensor.islamic_prayer_times_dhuhr_prayer
  - sensor.islamic_prayer_times_asr_prayer
  - sensor.islamic_prayer_times_maghrib_prayer
show_header_toggle: false
state_color: true
header:
  type: picture
  image: /local/images/pray02.gif
  tap_action:
    action: none
  hold_action:
    action: none
title: اوقات شرعی

------------------------------------------






views:
  - panel: true
    title: My Host
    path: myhost
    icon: ''
    badges: []
    cards:
      - type: iframe
        url: https://ghonchehoil.com/Blog/Post/cooking-with-olive-oil/
        aspect_ratio: 100%




