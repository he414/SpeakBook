---
layout: SpeakBook
classic_edition: true
text:
  ring_bind_edge: Reliez en classeur à spirales
  cut_out_this_part: Découpez cette partie.
  SPEAKBOOK: SPEAKBOOK
  classic: classic
  EDITION: VERSION
  color_blind: Adapté pour les
  friendly: daltoniens
  instructions: instructions
  HOME_PAGE: ACCUEIL
  SPELL: EPELER
  HOME: ACCUEIL
  THANK_YOU: MERCI
  A: A
  B: B
  C: C
  D: D
  E: E
  F: F
  G: G
  H: H
  I: I
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
  W: W
  X: X
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
  im_too_hot: J’ai trop chaud
  im_too_cold: J’ai trop froid
  cup_of_tea: Verre d’eau!
  cup_of_coffee: Tasse de café!
  i_love_you: Je t’aime
  yes: oui
  no: non
  CAR: Voiture
  BED: COUCHER
  CLOTHING: VETEMENTS
  BATHTIME: DOUCHE
  MEALS: REPAS
  COMFORT: INCONFORT
  TOILET: WC
  DRINKS: BOISSONS
  TRAINING_PAGE: Page d’essai
  training_page: Page d’essai
  _GBP: €
  _USD: $
  _percent: "%"
  _plus: +
  _minus: "-"
  _slash: /
  _X: X
  _equal: =
  _question_mark: "?"
  _atsign: "@"
  YES: OUI
  NO: NON
  edition_nth: 5e
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
<h2 class="my-2">Page pour épeler en utilisant les doigts.</h2>
<p class="my-2">
Si vous avez encore l'usage de vos mains, cette page est pour vous. Vous pouvez épe-ler des mots ou des phrases à votre partenaire en les montrant du doigt. Les mots fré-quemment utilisés peuvent être écrits dans les cases vides. Quand vous voulez revenir au livre principal pour communiquer, attirez l'attention sur <strong class="bold">„ ACCUEIL‟*</strong> .
</p>
:::
::: slot training-page-description
<p class="fsize-3">
Lorsque vous avez appris la technique de base en utilisant cette page d'essai, vous pouvez écrire vos propres pages.
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
    <span class="fsize-8 bold">Outil de communication non-verbale</span><br>
    <span class="red-color fsize-8 bold">acecent.re/speakbook</span><br>
    <span class="fsize-4">Speakbook 4ème version © 2011 Patrick Joyce, 2020 Ace Centre traduit en français par Myrande Robin et Jill Shepperd</span>
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
      <h3 class="my-1 fsize-5">Comment écrire sur Speakbook</h3>
      <p class="my-2 fsize-4_5">En fait, ce que vous écrirez sur Speakbook dépendra de vos besoins particuliers. Peu importe ce que vous écrivez, il est important que chaque côté d'une double page possède le même texte, et que chaque page soit une image miroir de l'autre - comme dans l'exemple ci-dessus. Si vous et votre partenaire parlez des langues différentes, il suffit d'écrire une langue différente sur chaque côté.</p>
    </div>
  </div>
</div>
:::
::: slot inst-01-content
<div class="p-1 text-center">
  <SpeakBookTextFourColorBkg class="speakbook-title fsize-10 p-1 bold" :text="$page.frontmatter.text.SPEAKBOOK"></SpeakBookTextFourColorBkg>
</div>
<p>Le Speakbook est un outil de communication non-verbale pour les personnes qui ne peuvent pas parler et qui ont des difficultés à utiliser leurs mains ou les bras, mais qui conservent l'usage de leurs yeux. Cette version est destinée aux personnes qui savent lire et épeler. Pour les versions pour les non-lecteurs, les versions en langue étrangère, et l'édition de poche, allez sur le site <b>acecent.re/speakbook</b></p>
<h2 class="fsize-6">Mode d'emploi.</h2>
<p>Vous aurez besoin du Speakbook, un marqueur noir effaçable, un chiffon pour effacer et un interlocuteur.</p>
<p>
Vous vous asseyez, face à face avec votre interlocuteur, à environ un mètre de distance. En fonction de votre vision, diminuez ou augmentez la distance. Ouvrez le Speakbook à la page d'essai, à l'intérieur de la couverture arrière. La page est déjà remplie pour vous aider à apprendre les bases. Lorsque vous aurez compris le fonctionnement, écrivez vos propres pages, en utilisant les blancs. Pliez le livre sur lui-même et tenez-le entre vous. Vous êtes chacun face à une page d’essai, et vous voyez les yeux de l'autre à travers le trou. Choisissez sur la page ce que vous allez communiquer à votre interlocuteur. Lorsque vous avez décidé, indiquez à votre partenaire que vous êtes prêt à commencer, en clignant des yeux par exemple. Regardez le message que vous avez choisi pendant une seconde ou deux, puis le cercle de la même couleur que la bande sur laquelle le message est écrit. Votre partenaire suit maintenant vos mouvements oculaires - par exemple, il voit que vous avez regardé le côté supérieur gauche du tableau suivi par le cercle bleu, donc il sait que vous voulez dire "un verre d'eau". Il dit alors, '"un verre d'eau" à haute voix, et vous le confirmez avec un clignement d'oeil, ou un autre signal choisi à l'avance.
</p>
<p>Ceci est la méthode de base pour utiliser le Speakbook. Maintenant il faut apprendre à utiliser les autres pages, parce que le vrai génie de Speakbook réside dans sa capacité à vous donner un accès facile à des centaines de phrases de votre choix, des phrases que vous pouvez changer à tout moment, avec seulement un chiffon humide et d'un coup de stylo.</p>
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
<p>Chaque page du Speakbook a 14 ou 15 sections vierges sur laquelle vous écrivez vos propres textes. Afin que l'utilisateur puisse se déplacer entre les différentes pages, nous avons créé la page <b>"ACCUEIL"</b>. Elle se trouve au début et est indiquée par un onglet noir en bordure de page. Ecrivez les 7 expressions que vous employez le plus souvent sur cette page, car vous commencerez toujours par cette page <b>"ACCUEIL"</b>. Sur 8 des bandes vides, écrivez des liens vers les 8 autres doubles pages vierges. Ces liens doivent correspondre à des moments répresentatifs de votre vie les plus importants, tels que les repas, l'heure du bain, ou sortir chercher du pain.</p>
<p>A gauche vous trouvez un exemple d'une mise en page possible pour la page <b>"ACCUEIL"</b>. Les 8 mots en majuscules gras sont des liens vers des doubles pages du livre. Sur une page vierge, écrivez, par exemple, <b>"LIT"</b> sur l'onglet, puis, sur les bandes, écrivez les 14 phrases correspondant le plus à votre routine du coucher. Ensuite, répétez ce processus pour les 7 autres liens, jusqu'à ce que votre Speakbook soit rempli. Si vous faites une erreur, ou si vous voulez changer une phrase, effacez avec un chiffon humide et recommencez!</p>
<p>Pour utiliser le Speakbook, indiquez à votre partenaire que vous souhaitez communiquer. Votre partenaire ouvre le Speakbook à la page <b>"ACCUEIL"</b> et vous montrez du regard par exemple, <b>"LIT"</b>. Votre partenaire se tourne alors vers la page <b>"LIT"</b> et vous pouvez alors lui communiquer la suite "Je veux me coucher" - ou autre chose. <b>"ACCUEIL"</b> et <b>"EPELER"</b> sont pré-remplis sur chaque page. <b>"ACCUEIL"</b> vous permet de toujours revenir à la page <b>"ACCUEIL"</b> (vous voulez peut-être un "VERRE D'EAU!" quand vous vous couchez). La page <b>"EPELER"</b> vous permet d'épeler des mots individuels et les expressions qui n'apparaissent pas dans le livre. Il fonctionne de façon similaire aux autres pages, mais avec une différence. Sur cette page il y a 6 blocs de couleur, chacun marqué avec des lettres colorées ou des chiffres. Vous avez tout l'alphabet, plus les chiffres 1-9 (pour zéro utilisez la lettre O). Regardez la lettre que vous souhaitez indiquer pendant une seconde ou deux, suivi du bloc coloré de la même couleur que votre lettre choisie. Votre partenaire suit vos yeux, voit par exemple que vous avez regardé le bloc supérieur gauche suivi du bloc en haut à droite (vert), et sait que vous avez choisi <b>"C"</b>. Votre partenaire dit <b>"C"</b> à haute voix pour confirmer, et vous passez à la prochaine lettre. Votre partenaire peut deviner le reste du mot, si possible, pour accélérer le processus<br> Le Speakbook a de la place pour 119 phrases de votre choix. Si cela ne suffit pas, ou si vous avez besoin de plus de 14 phrases dans une section particulière, vous pouvez doubler sa capacité en écrivant deux phrases sur chaque ligne, une en noir, une en rouge. Vous choisissez une phrase en noir de façon normale, une en rouge en clignant des yeux quand vous regardez le grand symbole.</p>
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
