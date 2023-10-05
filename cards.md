type: iframe
url: https://www.youtube.com/embed/590MXisPeZE
aspect_ratio: '16:9'


----


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

----




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


----



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





----


wallpanel:
  enabled: true
  enabled_on_tabs:
    - default_view
  debug: false
  hide_toolbar: true
  hide_sidebar: true
  fullscreen: true
  idle_time: 10
  keep_screen_on_time: 86400
  black_screen_after_time: 7200
  control_reactivation_time: 1.0
  screensaver_stop_navigation_path: /lovelace/default_view
  image_url: 'http://picsum.photos/${width}/${height}?random=${timestamp}'
  image_fit: cover
  image_list_update_interval: 3600
  image_order: 'sorted'
  image_excludes: []
  show_image_info: false
  fetch_address_data: true
  image_info_template: '${address.town|address.city!prefix=!suffix= // }${DateTimeOriginal!options=year:numeric,month:long}'
  screensaver_entity: input_boolean.wallpanel_screensaver
  info_animation_duration_x: 30
  info_animation_duration_y: 11
  info_animation_timing_function_x: 'ease-in-out'
  info_animation_timing_function_y: 'ease-in-out'
  info_move_pattern: random
  info_move_interval: 0
  info_move_fade_duration: 2.0
  card_interaction: true
  style:
    wallpanel-screensaver-info-box:
      font-size: 8vh
      font-weight: 600
      color: '#eeeeee'
      text-shadow: '-2px -2px 0 #03a9f4, 2px -2px 0 #03a9f4, -2px 2px 0 #03a9f4, 2px 2px 0 #03a9f4'

----

background per tab


views:
  - title: Main
    id: Main
    background: >-
      center / cover no-repeat fixed
      url('https://product-photos.s3.ir-thr-at1.arvanstorage.com/app-1673384101152-1000322830-DaT8XzYc5dFmdbyaFdpgcBVQk45abeIfJ78ny5K323u5x3gpjQAgcW4V7i3kmAHsh-700x468.png')
    cards:
      - type: button
        tap_action:
          action: toggle
        entity: light.1tecto_cozinha
  - title: test
    path: test
    badges: []
    cards: []








----

type: iframe
url: /local/pdf/ebook-01.pdf


type: markdown
content: >
  [Open PDF](/local/pdf/ebook-01.pdf)


