# Lab 4 — Reflection

 `flex: 1 1 280px`

- 1 (grow): card can expand to fill leftover space, equally with siblings.
- 1 (shrink): card can shrink below 280px if the container is too narrow.
- 280px (basis): starting width before grow/shrink is applied.

Math: 900px container − 40px (2 gaps × 20px) = 860px available.
3 × 280px = 840px basis total. Leftover = 20px, split 3 ways ≈ 6.7px each.
Each card ends up ≈ 286–287px wide.

 Equal height cards + button at the bottom

- `.pricing-table` has `align-items: stretch`, so every `.plan` card is forced to match the height of the tallest card in the row.
- Each `.plan` is itself `display: flex; flex-direction: column`, so its content stacks vertically — leaving empty space at the bottom of shorter cards.
- `margin-top: auto` on `.btn` absorbs that leftover space, pushing the button to the bottom of its card no matter how much content is above it.

 Mobile-first vs. `max-width`

Mobile-first means writing base styles for the smallest screen with no media query, then using `min-width` queries to add layout as space increases. This matches how most Malawian users experience the site first, since mobile traffic dominates.

Using `max-width` instead would mean designing for desktop first, then subtracting/overriding features for smaller screens — mobile becomes an afterthought correction rather than the primary target, and mobile devices still have to parse the desktop rules before the override kicks in.

  Float's limitation vs. Flexbox

Float can align one image beside text, but it can't natively give multiple columns equal height or evenly distributed spacing — floated elements don't share an alignment system. Flexbox solves this directly with `align-items` and `justify-content`.

