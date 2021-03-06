---
layout: SpeakBook
classic_edition: true
text:
  ring_bind_edge: Bu kenar boyunca halkayı bağlayın
  cut_out_this_part: Bu kısmı kesin
  SPEAKBOOK: KONUŞMAKİTABI
  classic: classic
  EDITION: BASKI
  color_blind: Renk körlüğü olanlar için de uygundur
  friendly: Samimi
  instructions: Kullanma talimatları
  HOME_PAGE: ANA SAYFA
  SPELL: HECELEME
  HOME: ANA SAYFA
  THANK_YOU: Teşekkür ederim
  A: A
  B: B
  C: Ç
  D: D
  E: E
  F: F
  G: G
  H: H
  I: İ
  J: J
  K: K
  L: L
  M: M
  N: N
  O: O
  P: P
  Q: Q
  R: R
  S: S
  T: T
  U: U
  V: V
  W: Ğ
  X: Ş
  Y: Y
  Z: Z
  _zero: "0"
  _one: "1"
  _two: "2"
  _three: "3"
  _four: "4"
  _five: "5"
  _six: "6"
  _seven: "7"
  _eight: "8"
  _nine: "9"
  im_too_hot: çok sıcak
  im_too_cold: çok soğuk / üşüyorum
  cup_of_tea: Bir bardak çay
  cup_of_coffee: Bir bardak kahve
  i_love_you: Seni seviyorum
  yes: Evet
  no: Hayır
  CAR: ARABA
  BED: YATAK
  CLOTHING: KIYAFET
  BATHTIME: YIKANMA ZAMANI
  MEALS: YİYECEKLER
  COMFORT: RAHATLIK
  TOILET: TUVALET
  DRINKS: İÇECEKLER
  TRAINING_PAGE: EĞİTİM SAYFASI
  training_page: eğitim sayfası
  _GBP: £
  _USD: $
  _percent: "%"
  _plus: +
  _minus: "-"
  _slash: /
  _X: X
  _equal: =
  _question_mark: "?"
  _atsign: "@"
  YES: EVET
  NO: HAYIR
  edition_nth: "5.cü "
slots_in_need_for_translation:
  - training-page-description
  - last-page-heading
  - cover-footer
  - inst-01-flt-right-content
  - inst-01-content
  - inst-02-flt-right-label
  - inst-02-content
inlinecss:
  --page-width: 210mm
  --page-height: 297mm
  --cut-out-center-guide-width: 68mm
  --cut-out-center-guide-height: 162mm
instruction_pages:
  - content_slotname: inst-01-content
    floating_elements:
      - comment: left spacing
        dir: left
        inlinecss:
          --spacing-offset-top: 17mm
          --left-spacing: 13mm
          --max-left-spacing: 40mm
          width: var(--max-left-spacing)
          height: var(--page-height)
          shape-outside: polygon(0 var(--spacing-offset-top), var(--max-left-spacing)
            var(--spacing-offset-top), var(--left-spacing)
            calc(var(--spacing-offset-top) + 20mm), var(--left-spacing)
            var(--page-height), 0 var(--page-height))
      - comment: floating content at center right
        dir: right
        mode: fixed
        inlinecss:
          --flt-width: 137mm
          --flt-height: var(--page-height)
          --flt-shape-width: var(--flt-width)
          --flt-shape-height: 175mm
          shape-outside: polygon(0 55mm, 100% 55mm, 100% 230mm, 0 230mm)
          top: 56mm
        slotname: inst-01-flt-right-content
  - content_slotname: inst-02-content
    floating_elements:
      - comment: right side cut out guide
        dir: right
        slotname: cut-out-right-side-guide-02
        inlinecss:
          width: 10mm
      - comment: right side label
        dir: right
        mode: fixed
        inlinecss:
          --flt-width: 44mm
          --flt-height: 44mm
          --flt-shape-width: var(--flt-width)
          --flt-shape-height: var(--flt-height)
          shape-outside: polygon(0 0, 100% 100%, 100% 0)
        slotname: inst-02-flt-right-label
      - dir: left
        mode: center-fixed
        inlinecss:
          --flt-shape-width: 137mm
          --flt-shape-height: 168mm
          --chrome-bugfix-bottom-offset: 6mm
        slotname: inst-02-flt-left-content
grid_pages:
  - name: page04
    comment: no cut out
    columns:
      - inlinecss:
          width: 57mm
        rows:
          - comment: At top left
            type: coloured-table
            rowheight: 12mm
            inlinecss:
              --grid-item-width: 57mm
              --grid-item-height: 94mm
              height: var(--grid-item-height)
          - comment: At center left
            type: coloured-circle
            colour: yellow
            inlinecss:
              flex-grow: 1
          - comment: At bottom left
            type: coloured-table
            rowheight: 12mm
            rows:
              - comment: empty
              - comment: empty
              - comment: empty
              - text_key: SPELL
            inlinecss:
              --grid-item-width: 57mm
              --grid-item-height: 94mm
              height: var(--grid-item-height)
      - inlinecss:
          width: 72mm
        rows:
          - comment: At top center
            type: coloured-circle
            colour: cyan
            inlinecss:
              flex-grow: 1
          - comment: space in middle
            inlinecss:
              width: var(--cut-out-center-guide-width)
              height: var(--cut-out-center-guide-height)
          - comment: At bottom center
            type: coloured-circle
            colour: green
            inlinecss:
              flex-grow: 1
      - inlinecss:
          width: 57mm
        rows:
          - comment: At top right
            type: coloured-table
            rowheight: 12mm
            inlinecss:
              --grid-item-width: 57mm
              --grid-item-height: 94mm
              height: var(--grid-item-height)
          - comment: At center right
            type: coloured-circle
            colour: purple
            inlinecss:
              flex-grow: 1
          - comment: At bottom right
            type: coloured-table
            rowheight: 12mm
            inlinecss:
              --grid-item-width: 57mm
              --grid-item-height: 94mm
              height: var(--grid-item-height)
  - name: page05
    start_spacing_slotname: cut-out-right-side-guide-03
    start_spacing_inlinecss:
      transform: rotate(180deg)
    inlinecss:
      transform: rotate(180deg)
    columns:
      - inlinecss:
          width: 57mm
        rows:
          - comment: At top left
            type: coloured-table
            rowheight: 12mm
            inlinecss:
              --grid-item-width: 57mm
              --grid-item-height: 94mm
              height: var(--grid-item-height)
          - comment: At center left
            type: coloured-circle
            colour: yellow
            inlinecss:
              flex-grow: 1
          - comment: At bottom left
            type: coloured-table
            rowheight: 12mm
            rows:
              - comment: empty
              - comment: empty
              - comment: empty
              - text_key: SPELL
            inlinecss:
              --grid-item-width: 57mm
              --grid-item-height: 94mm
              height: var(--grid-item-height)
      - inlinecss:
          width: 72mm
        rows:
          - comment: At top center
            type: coloured-circle
            colour: green
            inlinecss:
              flex-grow: 1
          - comment: Guide at center
            type: custom
            slotname: cut-out-center-guide
            inlinecss:
              flex-grow: 1
              transform: rotate(180deg)
          - comment: At bottom center
            type: coloured-circle
            colour: cyan
            inlinecss:
              flex-grow: 1
      - inlinecss:
          width: 57mm
        rows:
          - comment: At top right
            type: coloured-table
            rowheight: 12mm
            inlinecss:
              --grid-item-width: 57mm
              --grid-item-height: 94mm
              height: var(--grid-item-height)
          - comment: At center right
            type: coloured-circle
            colour: purple
            inlinecss:
              flex-grow: 1
          - comment: At bottom right
            type: coloured-table
            rowheight: 12mm
            inlinecss:
              --grid-item-width: 57mm
              --grid-item-height: 94mm
              height: var(--grid-item-height)
  - name: page06
    comment: no cut out
    columns:
      - comment: Left column
        inlinecss:
          width: 55mm
        rows:
          - comment: At top left
            type: letters-grid
            inlinecss:
              --grid-item-width: 55mm
              --grid-item-height: 62mm
              height: var(--grid-item-height)
              background-color: var(--color-yellow)
            entries:
              - text_key: S
                inlinecss:
                  color: var(--color-purple)
              - text_key: T
                inlinecss:
                  color: var(--color-white)
              - text_key: U
                inlinecss:
                  color: var(--color-green)
              - text_key: V
                inlinecss:
                  color: var(--color-yellow)
              - text_key: W
                inlinecss:
                  color: var(--color-orange)
              - text_key: X
                inlinecss:
                  color: var(--color-cyan)
          - comment: spacing
            inlinecss:
              flex-grow: 1
          - comment: At center left
            type: letters-grid
            inlinecss:
              --grid-item-width: 55mm
              --grid-item-height: 62mm
              height: var(--grid-item-height)
              background-color: var(--color-orange)
            entries:
              - text_key: Y
                inlinecss:
                  color: var(--color-purple)
              - text_key: Z
                inlinecss:
                  color: var(--color-white)
              - text_key: _one
                inlinecss:
                  color: var(--color-green)
              - text_key: _two
                inlinecss:
                  color: var(--color-yellow)
              - text_key: _three
                inlinecss:
                  color: var(--color-orange)
              - text_key: _four
                inlinecss:
                  color: var(--color-cyan)
          - comment: spacing
            inlinecss:
              flex-grow: 1
          - comment: At bottom left
            type: letters-grid
            inlinecss:
              --grid-item-width: 55mm
              --grid-item-height: 62mm
              height: var(--grid-item-height)
              background-color: var(--color-cyan)
            entries:
              - text_key: _five
                inlinecss:
                  color: var(--color-purple)
              - text_key: _six
                inlinecss:
                  color: var(--color-white)
              - text_key: _seven
                inlinecss:
                  color: var(--color-green)
              - text_key: _eight
                inlinecss:
                  color: var(--color-yellow)
              - text_key: _nine
                inlinecss:
                  color: var(--color-orange)
              - text_key: HOME
                inlinecss:
                  color: var(--color-cyan)
                  font-size: 18pt
      - comment: Center
        inlinecss:
          width: 76mm
      - comment: Right column
        inlinecss:
          width: 55mm
        rows:
          - comment: At top right
            type: letters-grid
            inlinecss:
              --grid-item-width: 55mm
              --grid-item-height: 62mm
              height: var(--grid-item-height)
              background-color: var(--color-purple)
            entries:
              - text_key: A
                inlinecss:
                  color: var(--color-purple)
              - text_key: B
                inlinecss:
                  color: var(--color-white)
              - text_key: C
                inlinecss:
                  color: var(--color-green)
              - text_key: D
                inlinecss:
                  color: var(--color-yellow)
              - text_key: E
                inlinecss:
                  color: var(--color-orange)
              - text_key: F
                inlinecss:
                  color: var(--color-cyan)
          - comment: spacing
            inlinecss:
              flex-grow: 1
          - comment: At center right
            type: letters-grid
            inlinecss:
              --grid-item-width: 55mm
              --grid-item-height: 62mm
              height: var(--grid-item-height)
              background-color: var(--color-white)
              border: 1px solid var(--color-black)
            entries:
              - text_key: G
                inlinecss:
                  color: var(--color-purple)
              - text_key: H
                inlinecss:
                  color: var(--color-white)
              - text_key: I
                inlinecss:
                  color: var(--color-green)
              - text_key: J
                inlinecss:
                  color: var(--color-yellow)
              - text_key: K
                inlinecss:
                  color: var(--color-orange)
              - text_key: L
                inlinecss:
                  color: var(--color-cyan)
          - comment: spacing
            inlinecss:
              flex-grow: 1
          - comment: At bottom right
            type: letters-grid
            inlinecss:
              --grid-item-width: 55mm
              --grid-item-height: 62mm
              height: var(--grid-item-height)
              background-color: var(--color-green)
            entries:
              - text_key: M
                inlinecss:
                  color: var(--color-purple)
              - text_key: N
                inlinecss:
                  color: var(--color-white)
              - text_key: O
                inlinecss:
                  color: var(--color-green)
              - text_key: P
                inlinecss:
                  color: var(--color-yellow)
              - text_key: Q
                inlinecss:
                  color: var(--color-orange)
              - text_key: R
                inlinecss:
                  color: var(--color-cyan)
  - name: page07
    start_spacing_slotname: cut-out-right-side-guide-04
    start_spacing_inlinecss:
      transform: rotate(180deg)
    inlinecss:
      transform: rotate(180deg)
    columns:
      - comment: Left column
        inlinecss:
          width: 55mm
        rows:
          - comment: At top left
            type: letters-grid
            inlinecss:
              --grid-item-width: 55mm
              --grid-item-height: 62mm
              height: var(--grid-item-height)
              background-color: var(--color-yellow)
            entries:
              - text_key: S
                inlinecss:
                  color: var(--color-purple)
              - text_key: T
                inlinecss:
                  color: var(--color-white)
              - text_key: U
                inlinecss:
                  color: var(--color-green)
              - text_key: V
                inlinecss:
                  color: var(--color-yellow)
              - text_key: W
                inlinecss:
                  color: var(--color-orange)
              - text_key: X
                inlinecss:
                  color: var(--color-cyan)
          - comment: spacing
            inlinecss:
              flex-grow: 1
          - comment: At center left
            type: letters-grid
            inlinecss:
              --grid-item-width: 55mm
              --grid-item-height: 62mm
              height: var(--grid-item-height)
              background-color: var(--color-orange)
            entries:
              - text_key: Y
                inlinecss:
                  color: var(--color-purple)
              - text_key: Z
                inlinecss:
                  color: var(--color-white)
              - text_key: _one
                inlinecss:
                  color: var(--color-green)
              - text_key: _two
                inlinecss:
                  color: var(--color-yellow)
              - text_key: _three
                inlinecss:
                  color: var(--color-orange)
              - text_key: _four
                inlinecss:
                  color: var(--color-cyan)
          - comment: spacing
            inlinecss:
              flex-grow: 1
          - comment: At bottom left
            type: letters-grid
            inlinecss:
              --grid-item-width: 55mm
              --grid-item-height: 62mm
              height: var(--grid-item-height)
              background-color: var(--color-cyan)
            entries:
              - text_key: _five
                inlinecss:
                  color: var(--color-purple)
              - text_key: _six
                inlinecss:
                  color: var(--color-white)
              - text_key: _seven
                inlinecss:
                  color: var(--color-green)
              - text_key: _eight
                inlinecss:
                  color: var(--color-yellow)
              - text_key: _nine
                inlinecss:
                  color: var(--color-orange)
              - text_key: HOME
                inlinecss:
                  color: var(--color-cyan)
                  font-size: 18pt
      - comment: Center
        inlinecss:
          width: 76mm
        rows:
          - comment: Guide at center
            type: custom
            slotname: cut-out-center-guide
            inlinecss:
              flex-grow: 1
              transform: rotate(180deg)
      - comment: Right column
        inlinecss:
          width: 55mm
        rows:
          - comment: At top right
            type: letters-grid
            inlinecss:
              --grid-item-width: 55mm
              --grid-item-height: 62mm
              height: var(--grid-item-height)
              background-color: var(--color-purple)
            entries:
              - text_key: A
                inlinecss:
                  color: var(--color-purple)
              - text_key: B
                inlinecss:
                  color: var(--color-white)
              - text_key: C
                inlinecss:
                  color: var(--color-green)
              - text_key: D
                inlinecss:
                  color: var(--color-yellow)
              - text_key: E
                inlinecss:
                  color: var(--color-orange)
              - text_key: F
                inlinecss:
                  color: var(--color-cyan)
          - comment: spacing
            inlinecss:
              flex-grow: 1
          - comment: At center right
            type: letters-grid
            inlinecss:
              --grid-item-width: 55mm
              --grid-item-height: 62mm
              height: var(--grid-item-height)
              background-color: var(--color-white)
              border: 1px solid var(--color-black)
            entries:
              - text_key: G
                inlinecss:
                  color: var(--color-purple)
              - text_key: H
                inlinecss:
                  color: var(--color-white)
              - text_key: I
                inlinecss:
                  color: var(--color-green)
              - text_key: J
                inlinecss:
                  color: var(--color-yellow)
              - text_key: K
                inlinecss:
                  color: var(--color-orange)
              - text_key: L
                inlinecss:
                  color: var(--color-cyan)
          - comment: spacing
            inlinecss:
              flex-grow: 1
          - comment: At bottom right
            type: letters-grid
            inlinecss:
              --grid-item-width: 55mm
              --grid-item-height: 62mm
              height: var(--grid-item-height)
              background-color: var(--color-green)
            entries:
              - text_key: M
                inlinecss:
                  color: var(--color-purple)
              - text_key: N
                inlinecss:
                  color: var(--color-white)
              - text_key: O
                inlinecss:
                  color: var(--color-green)
              - text_key: P
                inlinecss:
                  color: var(--color-yellow)
              - text_key: Q
                inlinecss:
                  color: var(--color-orange)
              - text_key: R
                inlinecss:
                  color: var(--color-cyan)
  - name: page08
    comment: no cut out
    columns:
      - inlinecss:
          width: 57mm
        rows:
          - comment: At top left
            type: coloured-table
            rowheight: 12mm
            rows:
              - comment: empty
              - comment: empty
              - comment: empty
              - text_key: HOME
            inlinecss:
              --grid-item-width: 57mm
              --grid-item-height: 94mm
              height: var(--grid-item-height)
          - comment: At center left
            type: coloured-circle
            colour: yellow
            inlinecss:
              flex-grow: 1
          - comment: At bottom left
            type: coloured-table
            rowheight: 12mm
            rows:
              - comment: empty
              - comment: empty
              - comment: empty
              - text_key: SPELL
            inlinecss:
              --grid-item-width: 57mm
              --grid-item-height: 94mm
              height: var(--grid-item-height)
      - inlinecss:
          width: 72mm
        rows:
          - comment: At top center
            type: coloured-circle
            colour: cyan
            inlinecss:
              flex-grow: 1
          - comment: space in middle
            inlinecss:
              width: var(--cut-out-center-guide-width)
              height: var(--cut-out-center-guide-height)
          - comment: At bottom center
            type: coloured-circle
            colour: green
            inlinecss:
              flex-grow: 1
      - inlinecss:
          width: 57mm
        rows:
          - comment: At top right
            type: coloured-table
            rowheight: 12mm
            inlinecss:
              --grid-item-width: 57mm
              --grid-item-height: 94mm
              height: var(--grid-item-height)
          - comment: At center right
            type: coloured-circle
            colour: purple
            inlinecss:
              flex-grow: 1
          - comment: At bottom right
            type: coloured-table
            rowheight: 12mm
            inlinecss:
              --grid-item-width: 57mm
              --grid-item-height: 94mm
              height: var(--grid-item-height)
  - name: page09
    start_spacing_slotname: cut-out-right-side-guide-05
    start_spacing_inlinecss:
      transform: rotate(180deg)
    inlinecss:
      transform: rotate(180deg)
    columns:
      - inlinecss:
          width: 57mm
        rows:
          - comment: At top left
            type: coloured-table
            rowheight: 12mm
            rows:
              - comment: empty
              - comment: empty
              - comment: empty
              - text_key: HOME
            inlinecss:
              --grid-item-width: 57mm
              --grid-item-height: 94mm
              height: var(--grid-item-height)
          - comment: At center left
            type: coloured-circle
            colour: yellow
            inlinecss:
              flex-grow: 1
          - comment: At bottom left
            type: coloured-table
            rowheight: 12mm
            rows:
              - comment: empty
              - comment: empty
              - comment: empty
              - text_key: SPELL
            inlinecss:
              --grid-item-width: 57mm
              --grid-item-height: 94mm
              height: var(--grid-item-height)
      - inlinecss:
          width: 72mm
        rows:
          - comment: At top center
            type: coloured-circle
            colour: green
            inlinecss:
              flex-grow: 1
          - comment: Guide at center
            type: custom
            slotname: cut-out-center-guide
            inlinecss:
              flex-grow: 1
              transform: rotate(180deg)
          - comment: At bottom center
            type: coloured-circle
            colour: cyan
            inlinecss:
              flex-grow: 1
      - inlinecss:
          width: 57mm
        rows:
          - comment: At top right
            type: coloured-table
            rowheight: 12mm
            inlinecss:
              --grid-item-width: 57mm
              --grid-item-height: 94mm
              height: var(--grid-item-height)
          - comment: At center right
            type: coloured-circle
            colour: purple
            inlinecss:
              flex-grow: 1
          - comment: At bottom right
            type: coloured-table
            rowheight: 12mm
            inlinecss:
              --grid-item-width: 57mm
              --grid-item-height: 94mm
              height: var(--grid-item-height)
  - name: page10
    comment: no cut out
    copyof: page08
  - name: page11
    copyof: page09
    start_spacing_slotname: cut-out-right-side-guide-06
  - name: page12
    comment: no cut out
    copyof: page08
  - name: page13
    copyof: page09
    start_spacing_slotname: cut-out-right-side-guide-07
  - name: page14
    comment: no cut out
    copyof: page08
  - name: page15
    copyof: page09
    start_spacing_slotname: cut-out-right-side-guide-08
  - name: page16
    comment: no cut out
    copyof: page08
  - name: page17
    copyof: page09
    start_spacing_slotname: cut-out-right-side-guide-09
  - name: page18
    comment: no cut out
    copyof: page08
  - name: page19
    copyof: page09
    start_spacing_slotname: cut-out-right-side-guide-10
  - name: page20
    comment: no cut out
    copyof: page08
  - name: page21
    copyof: page09
    start_spacing_slotname: cut-out-right-side-guide-11
  - name: page22
    comment: no cut out
    copyof: page08
  - name: page23
    copyof: page09
    start_spacing_slotname: cut-out-right-side-guide-12
  - name: page24
    comment: no cut out
    columns:
      - inlinecss:
          width: 57mm
        rows:
          - comment: At top left
            type: coloured-table02
            rowheight: 12mm
            overlay_slotname: table-overlay-01
            rows:
              - text_key: i_love_you
              - text_key: yes
                inlinecss:
                  margin-left: 14mm
              - text_key: no
                inlinecss:
                  margin-left: 30mm
              - text_key: CAR
                inlinecss:
                  margin-left: 43mm
            inlinecss:
              --grid-item-width: 57mm
              --grid-item-height: 94mm
              height: var(--grid-item-height)
          - comment: spacing
            inlinecss:
              flex-grow: 1
          - comment: At center left
            type: text-with-coloured-circle
            fixed: true
            colour: yellow
            text_slotname: training-page-description
            inlinecss:
              --grid-item-width: 57mm
              --grid-item-height: 94mm
              height: var(--grid-item-height)
          - comment: spacing
            inlinecss:
              flex-grow: 1
          - comment: At bottom left
            type: coloured-table02
            rowheight: 12mm
            rows:
              - text_key: COMFORT
              - text_key: TOILET
              - text_key: DRINKS
              - text_key: SPELL
            inlinecss:
              --grid-item-width: 57mm
              --grid-item-height: 94mm
              height: var(--grid-item-height)
      - inlinecss:
          width: 72mm
        rows:
          - comment: At top center
            type: coloured-circle
            colour: cyan
            inlinecss:
              flex-grow: 1
          - comment: space in middle
            inlinecss:
              width: var(--cut-out-center-guide-width)
              height: var(--cut-out-center-guide-height)
          - comment: At bottom center
            type: coloured-circle
            colour: green
            inlinecss:
              flex-grow: 1
      - inlinecss:
          width: 57mm
        rows:
          - comment: At top right
            type: coloured-table02
            rowheight: 12mm
            rows:
              - text_key: im_too_hot
              - text_key: im_too_cold
              - text_key: cup_of_tea
              - text_key: cup_of_coffee
            inlinecss:
              --grid-item-width: 57mm
              --grid-item-height: 94mm
              height: var(--grid-item-height)
          - comment: spacing
            inlinecss:
              flex-grow: 1
          - comment: At center right
            type: text-with-coloured-circle
            colour: purple
            text_key: TRAINING_PAGE
            text_inlinecss:
              font-size: 18pt
            text_at_top: true
          - comment: spacing
            inlinecss:
              flex-grow: 1
          - comment: At bottom right
            type: coloured-table02
            rowheight: 12mm
            rows:
              - text_key: BED
              - text_key: CLOTHING
              - text_key: BATHTIME
              - text_key: MEALS
            inlinecss:
              --grid-item-width: 57mm
              --grid-item-height: 94mm
              height: var(--grid-item-height)
  - name: page25
    start_spacing_slotname: cut-out-right-side-guide-13
    start_spacing_inlinecss:
      transform: rotate(180deg)
    inlinecss:
      transform: rotate(180deg)
    columns:
      - inlinecss:
          width: 57mm
        rows:
          - comment: At bottom right
            type: coloured-table02
            rowheight: 12mm
            rows:
              - text_key: COMFORT
              - text_key: TOILET
              - text_key: DRINKS
              - text_key: SPELL
            inlinecss:
              --grid-item-width: 57mm
              --grid-item-height: 94mm
              height: var(--grid-item-height)
          - comment: spacing
            inlinecss:
              flex-grow: 1
          - comment: At center right
            type: text-with-coloured-circle
            fixed: true
            colour: yellow
            text_slotname: training-page-description
            inlinecss:
              --grid-item-width: 57mm
              --grid-item-height: 94mm
              height: var(--grid-item-height)
          - comment: spacing
            inlinecss:
              flex-grow: 1
          - comment: At top right
            type: coloured-table02
            overlay_slotname: table-overlay-02
            rowheight: 12mm
            rows:
              - text_key: i_love_you
              - text_key: yes
                inlinecss:
                  margin-right: 14mm
              - text_key: no
                inlinecss:
                  margin-right: 30mm
              - text_key: CAR
                inlinecss:
                  margin-right: 43mm
            inlinecss:
              --grid-item-width: 57mm
              --grid-item-height: 94mm
              height: var(--grid-item-height)
      - inlinecss:
          width: 72mm
        rows:
          - comment: At bottom center
            type: coloured-circle
            colour: green
            inlinecss:
              flex-grow: 1
          - comment: Guide at center
            type: custom
            slotname: cut-out-center-guide
            inlinecss:
              flex-grow: 1
              transform: rotate(180deg)
          - comment: At top center
            type: coloured-circle
            colour: cyan
            inlinecss:
              flex-grow: 1
      - inlinecss:
          width: 57mm
        rows:
          - comment: At left bottom
            type: coloured-table02
            rowheight: 12mm
            rows:
              - text_key: BED
              - text_key: CLOTHING
              - text_key: BATHTIME
              - text_key: MEALS
            inlinecss:
              --grid-item-width: 57mm
              --grid-item-height: 94mm
              height: var(--grid-item-height)
          - comment: spacing
            inlinecss:
              flex-grow: 1
          - comment: At center left
            type: text-with-coloured-circle
            colour: purple
            text_key: TRAINING_PAGE
            text_inlinecss:
              font-size: 18pt
            text_at_top: true
          - comment: spacing
            inlinecss:
              flex-grow: 1
          - comment: At top left
            type: coloured-table02
            rowheight: 12mm
            rows:
              - text_key: im_too_hot
              - text_key: im_too_cold
              - text_key: cup_of_tea
              - text_key: cup_of_coffee
            inlinecss:
              --grid-item-width: 57mm
              --grid-item-height: 94mm
              height: var(--grid-item-height)

---
::: slot redheart-img
<img style="width: var(--img-width); height: var(--img-width);" :src="$withBase('/speakbook/shapes/redheart.svg')" />
:::
::: slot smileyface-img
<img style="width: var(--img-width); height: var(--img-width);" :src="$withBase('/speakbook/shapes/smileyface.svg')" />
:::
::: slot last-page-heading
<div class="float-left" style="width: 40mm; height: 37mm; shape-outside: polygon(0 0, 40mm 0, 10mm 100%, 0 100%);"></div>
<h2 class="my-2"> Parmaklarla heceleme sayfası </h2>
<p class="my-2">
Eğer ellerinizi kullanabiliyorsanız, bu sayfa sizin için. 
Parmağınızla harfleri teker teker göstererek kelimeleri veya sözcük gruplarını heceleyebilirsiniz. 
Sıklıkla kullanılan kelimeler boş kutuların içerisine yazılabilir. 
ANA SAYFA kelimesine işaret ederek, konuşma partnerinize ana kitabı kullanarak ve gözlerinizle iletişime geçmek istediğinizi belirtebilirsiniz. </p>
:::
::: slot training-page-description
<p class="fsize-3">
Eğitim sayfasındaki basit teknikleri öğrendikten sonra, bu kitapta bulunan boş sayfaları kullanarak kendi sayfalarınızı yaratabilirsiniz. 
</p>
:::
::: slot table-overlay-01
<div class="abs-at-top-left" style="top: 0.5mm; left: 0.5mm; width: 44mm; height: 44mm;">
  <img class="abs-fill-parent" :src="$withBase('/speakbook/shapes/table-overlay-01.svg')" />
  <div class="abs-at-center bold" style="transform: translate(calc(-50% - 8mm), calc(-50% - 8mm)) rotate(-45deg); color: white;text-align: center;font-size: 18pt;width: 35mm;line-height: 1;">{{ $page.frontmatter.text.training_page }}</div>
</div>
:::

::: slot table-overlay-02
<img class="abs-at-bottom-left rotate-180" style="bottom: 0.5mm; left: 0.5mm; width: 44mm; height: 44mm;" :src="$withBase('/speakbook/shapes/table-overlay-02.svg')" />
:::

::: slot shape-square-2x-img
<img style="width: var(--img-width); height: var(--img-width);" :src="$withBase('/speakbook/shapes/square-2x.svg')" />
:::
::: slot shape-heart-2x-img
<img style="width: var(--img-width); height: var(--img-width);" :src="$withBase('/speakbook/shapes/heart-2x.svg')" />
:::
::: slot shape-circle-2x-img
<img style="width: var(--img-width); height: var(--img-width);" :src="$withBase('/speakbook/shapes/circle-2x.svg')" />
:::
::: slot shape-triangle-2x-img
<img style="width: var(--img-width); height: var(--img-width);" :src="$withBase('/speakbook/shapes/triangle-2x.svg')" />
:::
::: slot shape-square-1x-img
<img style="width: var(--img-width); height: var(--img-width);" :src="$withBase('/speakbook/shapes/square-1x.svg')" />
:::
::: slot shape-heart-1x-img
<img style="width: var(--img-width); height: var(--img-width);" :src="$withBase('/speakbook/shapes/heart-1x.svg')" />
:::
::: slot shape-circle-1x-img
<img style="width: var(--img-width); height: var(--img-width);" :src="$withBase('/speakbook/shapes/circle-1x.svg')" />
:::
::: slot shape-triangle-1x-img
<img style="width: var(--img-width); height: var(--img-width);" :src="$withBase('/speakbook/shapes/triangle-1x.svg')" />
:::
::: slot star-16p-bkg
<img class="fill-width fill-height" :src="$withBase('/speakbook/shapes/star-16p.svg')" />
:::
::: slot cut-out-center-guide
<div class="pos-rel flex-h justify-content-center" style="width: var(--cut-out-center-guide-width); height: var(--cut-out-center-guide-height);">
  <img class="abs-fill-parent" :src="$withBase('/speakbook/shapes/cut-out-center-guide.svg')" />
  <div class="wmode-vertical-lr rotate-180 fsize-10 v-oneline-fsize-10 bold grey-color text-center">
    {{ $page.frontmatter.text.cut_out_this_part }}
  </div>
</div>
:::
::: slot cut-out-right-side-guide-01
<div class="flex-h height-100ph grey-color">
  <img style="width: 44.5mm; height: 287.2mm;" :src="$withBase('/speakbook/shapes/cut-out-right-side-guide.svg')" />
  <div class="flex-v mx-auto fsize-8 v-oneline-fsize-8 bold">
    <div v-for="i in 2" class="wmode-vertical-lr rotate-180 flex-grow-1 text-center">
      {{ $page.frontmatter.text.cut_out_this_part }}
    </div>
  </div>
</div>
:::
::: slot cut-out-right-side-guide-02
<CutOutSideGuide textlen="2" :text="$page.frontmatter.text.cut_out_this_part">
  <img class="abs-at-center-left" :src="$withBase('/speakbook/shapes/cut-out-right-side-guide-02.svg')" />
</CutOutSideGuide>
:::
::: slot cut-out-right-side-guide-03
<CutOutSideGuide textlen="2" :text="$page.frontmatter.text.cut_out_this_part">
  <img class="abs-at-center-left" :src="$withBase('/speakbook/shapes/cut-out-right-side-guide-03.svg')" />
  <div class="white-color wmode-vertical-lr rotate-180 fsize-8 bold flex-v items-align-center justify-content-center" style="position: absolute; top: 2mm; left: 0mm; width: 10mm; height: 28mm;">{{ $page.frontmatter.text.HOME }}</div>
</CutOutSideGuide>
:::
::: slot cut-out-right-side-guide-04
<CutOutSideGuide textlen="2" :text="$page.frontmatter.text.cut_out_this_part" textstyle="padding-top: 30mm; box-sizing: border-box;">
  <img class="abs-at-center-left" :src="$withBase('/speakbook/shapes/cut-out-right-side-guide-04.svg')" />
  <div class="red-color wmode-vertical-lr rotate-180 fsize-8 bold flex-v items-align-center justify-content-center" style="position: absolute; top: 30.5mm; left: 0mm; width: 10mm; height: 28mm;">{{ $page.frontmatter.text.SPELL }}</div>
</CutOutSideGuide>
:::
::: slot cut-out-right-side-guide-05
<CutOutSideGuide textlen="1" :text="$page.frontmatter.text.cut_out_this_part" textstyle="padding-top: 90mm; box-sizing: border-box;">
  <img class="abs-at-center-left" :src="$withBase('/speakbook/shapes/cut-out-right-side-guide-05.svg')" />
</CutOutSideGuide>
:::
::: slot cut-out-right-side-guide-06
<CutOutSideGuide textlen="1" :text="$page.frontmatter.text.cut_out_this_part" textstyle="padding-top: 90mm; box-sizing: border-box;">
  <img class="abs-at-center-left" :src="$withBase('/speakbook/shapes/cut-out-right-side-guide-06.svg')" />
</CutOutSideGuide>
:::
::: slot cut-out-right-side-guide-07
<CutOutSideGuide textlen="2" :text="$page.frontmatter.text.cut_out_this_part">
  <img class="abs-at-center-left" :src="$withBase('/speakbook/shapes/cut-out-right-side-guide-07.svg')" />
</CutOutSideGuide>
:::
::: slot cut-out-right-side-guide-08
<CutOutSideGuide textlen="2" :text="$page.frontmatter.text.cut_out_this_part" textstyle="padding-top: 10mm; box-sizing: border-box;">
  <img class="abs-at-center-left" :src="$withBase('/speakbook/shapes/cut-out-right-side-guide-08.svg')" />
</CutOutSideGuide>
:::
::: slot cut-out-right-side-guide-09
<CutOutSideGuide textlen="1" :text="$page.frontmatter.text.cut_out_this_part" textstyle="padding-bottom: 80mm; box-sizing: border-box;">
  <img class="abs-at-center-left" :src="$withBase('/speakbook/shapes/cut-out-right-side-guide-09.svg')" />
</CutOutSideGuide>
:::
::: slot cut-out-right-side-guide-10
<CutOutSideGuide textlen="1" :text="$page.frontmatter.text.cut_out_this_part" textstyle="padding-bottom: 90mm; box-sizing: border-box;">
  <img class="abs-at-center-left" :src="$withBase('/speakbook/shapes/cut-out-right-side-guide-10.svg')" />
</CutOutSideGuide>
:::
::: slot cut-out-right-side-guide-11
<CutOutSideGuide textlen="1" :text="$page.frontmatter.text.cut_out_this_part">
  <img class="abs-at-center-left" :src="$withBase('/speakbook/shapes/cut-out-right-side-guide-11.svg')" />
</CutOutSideGuide>
:::
::: slot cut-out-right-side-guide-12
<CutOutSideGuide textlen="1" :text="$page.frontmatter.text.cut_out_this_part">
  <img class="abs-at-center-left" :src="$withBase('/speakbook/shapes/cut-out-right-side-guide-12.svg')" />
</CutOutSideGuide>
:::
::: slot cut-out-right-side-guide-13
<CutOutSideGuide textlen="2" :text="$page.frontmatter.text.cut_out_this_part">
  <img class="abs-at-bottom-left" :src="$withBase('/speakbook/shapes/cut-out-right-side-guide-13.svg')" />
</CutOutSideGuide>
:::
::: slot cover-footer
<div class="flex-h items-align-center lheight-1_5x" style="width: calc(var(--page-width) - 60mm);">
  <p class="cover-footer-text">
    <span class="fsize-8 bold"> sözel olmayan iletişim sistemi </span><br>
    <span class="red-color fsize-8 bold">acecent.re/speakbook</span><br>
    <span class="fsize-4"> Konuşmakitabı 5. baskı © 2011 Patrick Joyce,  2020 Ace Centre, Kuhunyushwe ngu-Ersin Sinay</span>
  </p>
  <div class="flex-grow-1"></div>
  <img style="width: 30mm;height: 30mm;" :src="$withBase('/speakbook/images/PublishedByAce.svg')" />
</div>
:::

::: slot inst-01-flt-right-content
<div class="abs-fill-parent flex-h" style="align-items: flex-end;">
  <div class="flex-grow-1"></div>
  <div class="flex-v">
    <img class="m-1" style="width: 58.5mm; height: 79.7mm; box-sizing: border-box;" :src="$withBase('/speakbook/images/01.png')"  />
    <div class="m-1 p-1 flex-grow-1 flt-box" style="width: 57.5mm; min-height: 79.7mm; box-sizing: border-box;">
      <h3 class="my-1 fsize-5">Konuşmakitabı üzerine nasıl yazılır? </h3>
      <p class="my-2 fsize-4_5">
Konuşma kitabına yazdıklarınız kişisel ihtiyaçlarınıza bağlı olacaktır, ancak ne yazarsanız yazın, herhangi bir çift sayfa yayılımının her bir yüzünün üzerinde aynı metnin olması ve bunların birbirinin ayna görüntüsü olması önemlidir- yukarıdaki örnekteki gibi. Siz ve eşiniz farklı bir dilde mi konuşuyorsunuz? Sorun değil - her iki tarafa da farklı bir dil yazın.</p>
    </div>
  </div>
</div>
:::
::: slot inst-01-content
Konuşmakitabı, konuşamayan ve ellerini veya kollarını kullanmada zorluk çeken, ancak gözlerinin kullanımını koruyan insanlar için sözel olmayan bir iletişim aracıdır. Bu basım, okuma ve yazma bilen kişiler içindir. Okuma-yazma bilmeyen kişiler için,  yabancı dil baskıları ve cep sürümü için, şu adresi ziyaret edin:
<b>acecent.re/speakbook</b></p>
<h2 class="fsize-6">Kullanma talimatları</h2>
<p> Başlamak için ihtiyacınız olan şeyler, konuşma kitabı; siyah, kalıcı olmayan bir kalem, silme bezi ve konuşma partneri.</p>
<p>
Siz ve konuşma partneriniz birbinizden yaklaşık 1 metre uzak olacak şekilde karşılıklı oturun. Görme yetinize bağlı olarak, bu mesafeyi azaltmayı veya artırmayı yararlı bulabilirsiniz. Kitabın arka kapağının içindeki eğitim sayfasını açın. Bu, temel tekniği öğrenmenize yardımcı olmak için zaten doldurulmuştur. Uzmanlaştığınızda, sağlanan boş sayfaları kullanarak kendi sayfalarınızı yazabilirsiniz. Kitabı kendi üzerine katlayın ve aranızda tutun, böylece ikiniz de bir 'eğitim sayfasına' bakıyor olacaksınız ve birbirinizin gözlerini ortadaki boş alandan görebileceksiniz. Sonra sayfada bulunan ihtimallerden hangisi hakkında iletişime geçmek istediğinize karar verin. Karar verdiğinizde, partnerinize başlamaya hazır olduğunuzu belirtin. Bunu konuşma partnerinize bakıp göz kırparak, gözlerini açıp kapatarak belirtebilirsiniz ya da kendinizin belirlediği başka bir ifade ile belirtebilisiniz. Daha sonra istediğiniz mesaja bir saniye kadar bakın, ardından mesajın yanındaki küçük sembolle aynı büyük simgeye bakın. Konuşma partneriniz daha sonra göz hareketlerinizi takip ederek ne demek istediğiniz öğrenir - örneğin tahtanın sol üst tarafına ve ardından büyük üçgene baktığınızı görebilir, bu yüzden “bir fincan çay!” demek istemeniz gerektiğini bilir. Seçim yaptıktan sonra konuşma partneriniz bu seçimi sözel olarak yüksek ses söyle ve siz de bunu göz kırparak veya daha önceden ayarladığınız bir ifade ile onaylarınız. 
</ P>
<p> Bu konuşma kitabını kullanmak için temel tekniktir. Şimdi kitaptaki diğer sayfaları nasıl kullanacağınızı öğrenmelisiniz, çünkü konuşma kitabının gerçek dehası, kendi seçtiğiniz yüzlerce cümleye, istediğiniz zaman değiştirebileceğiniz ifadelere kolayca erişebilmenizde yatmaktadır. Tek ihtiyacınız olan sadece nemli bir bez ve kaleminiz. </p>
:::

::: slot inst-02-flt-right-label
<div class="pos-rel fill-height fill-width">
  <img class="abs-fill-parent" :src="$withBase('/speakbook/shapes/inst-02-right-label-bkg.svg')" />
  <div class="fsize-8 abs-at-center" style="transform: translate(calc(-50% + 5mm), calc(-50% - 5mm)) rotate(45deg); color: white;width: 42mm;text-align: center;">{{ $page.frontmatter.text.instructions }}</div>
</div>
:::
::: slot inst-02-flt-left-content
<div class="flex-h" style="padding: 3mm;">
  <div class="flex-grow-1 flex-v">
    <img class="m-1" style="width: 57.5mm; height: 79.7mm; box-sizing: border-box;" :src="$withBase('/speakbook/images/02.png')"  />
    <img class="m-1" style="width: 57.5mm; height: 79.7mm; box-sizing: border-box;" :src="$withBase('/speakbook/images/03.png')"  />
  </div>
  <Content slot-key="cut-out-center-guide" />
</div>
:::
::: slot inst-02-content
<p> Konuşma kitabının her sayfasında kendi metninizi yazabileceğiniz 14 veya 15 boş bölüm bulunur. Kullanıcının farklı sayfalar arasında hareket edebilmesi için, "ana sayfa" sayfasını oluşturduk. Bu kitabın ön tarafında bulunur ve sayfanın kenarında siyah bir “ANA SAYFA” sekmesi ile işaretlenmiştir. Buradaki amaç, kitabın en başında bulunan bu sayfada en çok kullandığınız 7 ifadeyi yazmanız ve böylelikle kolaylıkla bu ifadelere istediğiniz anda ulaşabilmeniz. 
Ayrıca, boş olan sekiz şeritin birinde diğer 8 boş çift sayfaya bağlantı kurabilirsiniz. Bunlar hayatınızın daha derinlemesine ifadeler gerektiren parçaları olmalı, örneğin banyo veya araba ile dışarı çıkmak gibi.  Sol tarafta “ANA SAYFA” sayfası için olası bir örnek bulabilirsiniz. Kalın harflerle yazılan 8 kelime, kitabın başka yerlerindeki çift sayfalara olan bağlantıları ifade eder. Yapmanız gereken boş bir sayfa bulmak ve örneğin kenar sekmesine “YATAK” yazmak, daha sonra varolan şeritlere uyumadan önce rutininizle en çok alakalı 14 ifadeyi yazmanızdır. Ardından kitabınız dolana kadar diğer 7 bağlantı için bu işlemi tekrarlayın. Bir hata yaparsanız veya bir cümleyi değiştirmek isterseniz, nemli bir bezle silin ve tekrar başlayın. </p>
<p> Konuşma kitabını kullanmak için partnerinize iletişim kurmak istediğinizi belirtirsiniz. Konuşma partneriniz konuşma kitabının “ANA SAYFA” sayfasına açar ve örneğin siz “YATAK” kelimesini ifade edersiniz. Konuşma partneriniz daha sonra “YATAK” sayfasına geçer ve siz bu sayfadaki kelime ve sözcük grupları ile iletişime geçebilirsiniz ör: yatağa gitmek istiyorum gibi. Her sayfada “ANA SAYFA” ve “HECELEME” ifadeleri bulunmaktadır. “ANA SAYFA” sekmesi her zaman “ANA SAYFA” sayfasına geri dönebilmeniz içindir. “HECELEME” sayfası, kitabın başka bir yerinde görünmeyen kelime ve sözcük gruplarını heceleyerek iafde etmenize olanak tanır. Bir farkla diğer sayfalara benzer şekilde çalışır. Bu sayfada, üzerinde 6 renkli harf veya rakam bulunan 6 renkli blok vardır. Bu sayfada harfler ve 1'den 9'a kadar sayılar bulunmaktadır. (sıfır için O harfini kullanabilirsiniz). İletişim kurmak istediğiniz harfe bir saniye kadar bakın, ardından seçtiğiniz harfle aynı renkteki renkli bloğa bakın. Konuşma partneriniz gözlerinizi takip edip; örneğin sol üst bloğa ve ardından sağ üst bloğa (yeşil olan) baktığınızı görür ve “C” harfiniz ifade ettiğinizi anlar. Konuşma partneriniz onaylamak için yüksek sesle “C” der ve siz de bunu daha önce belirlediğiniz onaylama sinyal ile onayladıktan sonra bir sonraki harfe geçebilirsiniz. Konuşma partneriniz, mümkün olduğunda süreci hızlandırmak için kelimenin geri kalanını tahmin eder. </ P>
<p> Konuşmakitabı içerisinde seçtiğiniz 119 cümle için yer var. Bu yeterli değilse veya belirli bir bölümde 14'ten fazla ifadeye ihtiyacınız varsa, her satıra bir tane siyah kalem, biri kırmızı olmak üzere iki kelime öbeği yazarak kapasitesini iki katına çıkarabilirsiniz. Normal bir şekilde siyah olarak yazılmış cümleyi gözlerinizle ifade ederek, büyük sembole bakıp kırmızı olana gözlerinizi kırparak aynı kutudaki kırmızı cümleyi ifade etmek istediğinizi belirtebilirsiniz </p>
:::

::: slot last-page-content
<div style="width: 10mm;"></div>
<div class="flex-v block-holder b10x">
  <Content slot-key="last-page-heading" />
  <div class="flex-v mt-2"> <!-- split between letters keys and others -->
    <div class="flex-h">
      <div class="flex-v block-holder b3x">
        <div class="block b0x flex-grow-1" style="margin-left: 8mm;"></div>
        <div class="block b3x"></div>
        <div class="block b3x"></div>
        <div class="block b3x"></div>
        <div class="block b3x"></div>
        <div class="block b3x"></div>
        <div class="flex-h flex-wrap">
          <div class="block">{{ $page.frontmatter.text._GBP }}</div>
          <div class="block">{{ $page.frontmatter.text._USD }}</div>
          <div class="block">{{ $page.frontmatter.text._percent }}</div>
          <div class="block">{{ $page.frontmatter.text._plus }}</div>
          <div class="block">{{ $page.frontmatter.text._minus }}</div>
          <div class="block">{{ $page.frontmatter.text._slash }}</div>
          <div class="block">{{ $page.frontmatter.text._X }}</div>
          <div class="block">{{ $page.frontmatter.text._equal }}</div>
          <div class="block">{{ $page.frontmatter.text._question_mark }}</div>
        </div>
        <div class="block b3x white-color black-bkg">{{ $page.frontmatter.text.HOME }}</div>
        <div class="block b3x yellow-bkg" style="font-size: 18pt;">{{ $page.frontmatter.text.THANK_YOU }}</div>
      </div>
      <div class="flex-v block-holder b4x">
        <div class="block b4x">
        </div>
        <div class="flex-grow-1"></div>
      </div>
      <div class="flex-v block-holder b3x">
        <div class="block b3x"></div>
        <div class="block b3x"></div>
        <div class="block b3x"></div>
        <div class="block b3x"></div>
        <div class="block b3x"></div>
        <div class="block b3x"></div>
        <div class="block b3x"></div>
        <div class="flex-h flex-wrap">
          <div class="block pink-bkg">{{ $page.frontmatter.text._one }}</div>
          <div class="block pink-bkg">{{ $page.frontmatter.text._two }}</div>
          <div class="block pink-bkg">{{ $page.frontmatter.text._three }}</div>
          <div class="block pink-bkg">{{ $page.frontmatter.text._four }}</div>
          <div class="block pink-bkg">{{ $page.frontmatter.text._five }}</div>
          <div class="block pink-bkg">{{ $page.frontmatter.text._six }}</div>
          <div class="block pink-bkg">{{ $page.frontmatter.text._seven }}</div>
          <div class="block pink-bkg">{{ $page.frontmatter.text._eight }}</div>
          <div class="block pink-bkg">{{ $page.frontmatter.text._nine }}</div>
          <Content class="block" slot-key="redheart-img" />
          <div class="block pink-bkg">{{ $page.frontmatter.text._zero }}</div>
          <Content class="block" slot-key="smileyface-img" />
        </div>
      </div>
    </div>
    <div class="flex-h flex-wrap">
      <div class="block cyan-bkg">{{ $page.frontmatter.text.Q }}</div>
      <div class="block cyan-bkg">{{ $page.frontmatter.text.W }}</div>
      <div class="block cyan-bkg">{{ $page.frontmatter.text.E }}</div>
      <div class="block cyan-bkg">{{ $page.frontmatter.text.R }}</div>
      <div class="block cyan-bkg">{{ $page.frontmatter.text.T }}</div>
      <div class="block cyan-bkg">{{ $page.frontmatter.text.Y }}</div>
      <div class="block cyan-bkg">{{ $page.frontmatter.text.U }}</div>
      <div class="block cyan-bkg">{{ $page.frontmatter.text.I }}</div>
      <div class="block cyan-bkg">{{ $page.frontmatter.text.O }}</div>
      <div class="block cyan-bkg">{{ $page.frontmatter.text.P }}</div>
      <div class="block cyan-bkg">{{ $page.frontmatter.text.A }}</div>
      <div class="block cyan-bkg">{{ $page.frontmatter.text.S }}</div>
      <div class="block cyan-bkg">{{ $page.frontmatter.text.D }}</div>
      <div class="block cyan-bkg">{{ $page.frontmatter.text.F }}</div>
      <div class="block cyan-bkg">{{ $page.frontmatter.text.G }}</div>
      <div class="block cyan-bkg">{{ $page.frontmatter.text.H }}</div>
      <div class="block cyan-bkg">{{ $page.frontmatter.text.J }}</div>
      <div class="block cyan-bkg">{{ $page.frontmatter.text.K }}</div>
      <div class="block cyan-bkg">{{ $page.frontmatter.text.L }}</div>
      <div class="block cyan-bkg">{{ $page.frontmatter.text._atsign }}</div>
      <div class="block cyan-bkg">{{ $page.frontmatter.text.Z }}</div>
      <div class="block cyan-bkg">{{ $page.frontmatter.text.X }}</div>
      <div class="block cyan-bkg">{{ $page.frontmatter.text.C }}</div>
      <div class="block b1_5x yellow-bkg">{{ $page.frontmatter.text.YES }}</div>
      <div class="block cyan-bkg">{{ $page.frontmatter.text.V }}</div>
      <div class="block b1_5x yellow-bkg">{{ $page.frontmatter.text.NO }}</div>
      <div class="block cyan-bkg">{{ $page.frontmatter.text.B }}</div>
      <div class="block cyan-bkg">{{ $page.frontmatter.text.N }}</div>
      <div class="block cyan-bkg">{{ $page.frontmatter.text.M }}</div>
    </div>
  </div>
</div>
:::
