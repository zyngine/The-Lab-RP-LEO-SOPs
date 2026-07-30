# Branding

## What changed

    mkdocs.yml                  logo, favicon, custom palette
    docs/assets/logo.png        the flask mark
    docs/assets/favicon.png     browser tab
    docs/stylesheets/extra.css  the actual brand hex

## Why a stylesheet rather than a named colour

Material ships named palettes — `cyan`, `indigo` and so on — and they
get close but never exact. Setting `primary: custom` and defining the
variables in `extra.css` means the header, links, headings and every
component that reads the primary colour all pick up the real values from
the logo, rather than each needing its own override later.

## The choices worth knowing about

The dark background carries a **green cast** rather than being neutral
grey, so the header does not look bolted onto a stock theme.

The header is the **dark panel colour with an acid green underline**,
not a slab of cyan. A saturated bar across the top of a long procedural
document is tiring to read under, and it lets the logo carry the colour
instead.

**Links are acid green**, because Material's default blue disappears
against a dark background.

**H2 headings are cyan**, which makes scanning a long SOP for the
section you need considerably faster.

## Applying the same to the player rulebook

Copy `docs/stylesheets/extra.css` and `docs/assets/` across, then make
the same three edits to that repo's `mkdocs.yml`: add `logo` and
`favicon` under `theme`, change both `primary` and `accent` to `custom`,
and add the `extra_css` block. The two sites will then match exactly.
