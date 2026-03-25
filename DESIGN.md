```markdown
# The Design System: Authentic Heat & Urban Grit

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"Street-Food Sophisticate."** 

This system captures the collision of a bustling Mexico City *taquería* and a legendary NYC corner slice shop. It rejects the sterile, "perfect" look of modern SaaS templates in favor of a high-contrast, editorial layout that feels lived-in yet premium. We break the "template" look through **Intentional Asymmetry**: large typography that bleeds off-grid, overlapping imagery that breaks container boundaries, and a rejection of traditional borders in favor of raw tonal shifts.

## 2. Color & Surface Theory
The palette is rooted in the heat of the oven and the vibrancy of street culture. We use depth to guide the eye, not lines.

### The Palette
- **Primary (The Heat):** `#af101a` (Primary) / `#d32f2f` (Container). Use this for high-energy actions and brand moments.
- **Secondary (The Glow):** `#785900` (Secondary) / `#fdc003` (Container). This warm gold mimics the perfect crust and ambient street lighting.
- **Neutral (The Canvas):** `#fcf9f8` (Surface) and `#1c1b1b` (On-Surface). A warm, "paper-stock" off-white provides a premium editorial feel compared to pure digital white.

### The "No-Line" Rule
**Explicit Instruction:** Do not use 1px solid borders to define sections. Layout boundaries must be achieved through:
1.  **Background Shifts:** Transitioning from `surface` to `surface-container-low`.
2.  **Negative Space:** Using the Spacing Scale (specifically `spacing-12` and `spacing-16`) to create "breathing" separation.

### Glass & Gradient Rule
To prevent the UI from feeling flat or "cheap," apply **Signature Textures**:
- **CTAs:** Use a subtle linear gradient from `primary` to `primary-container` at 135 degrees.
- **Floating Overlays:** Use `surface-container-lowest` with an 85% opacity and a `20px` backdrop-blur to create a "frosted glass" effect for navigation bars or snack-selection overlays.

## 3. Typography: Editorial Boldness
We pair the structural weight of a modern sans-serif with the character of a high-contrast display face.

*   **Display & Headlines (Epilogue):** This is our "Street Voice." Use `display-lg` and `headline-lg` for product names and hero statements. Encourage tight letter-spacing (-2%) and occasional italics to mimic the energy of hand-painted signage.
*   **Body & Titles (Plus Jakarta Sans):** Our "Modern Utility." This provides the NYC pizzeria efficiency. Use `body-lg` for descriptions to ensure high legibility against vibrant backgrounds.
*   **The Hierarchy:** Headlines should be significantly larger than body text (a 4:1 ratio) to create a clear, authoritative editorial hierarchy that feels like a premium food magazine.

## 4. Elevation & Depth
We eschew traditional material shadows for **Tonal Layering**.

*   **The Layering Principle:** Treat the UI as stacked sheets of parchment. 
    *   Base layer: `surface`
    *   Section layer: `surface-container-low`
    *   Actionable card: `surface-container-lowest`
*   **Ambient Shadows:** If a card must float (e.g., a "Cart" modal), use a shadow color tinted with the brand’s red: `rgba(175, 16, 26, 0.08)` with a `48px` blur and `0px` offset. This mimics natural light passing through a warm environment.
*   **The "Ghost Border" Fallback:** For input fields, use `outline-variant` at 20% opacity. Never use 100% opaque black or grey borders.

## 5. Components

### Buttons & Interaction
- **Primary Button:** Roundedness `md` (0.375rem). Background is the `primary` gradient. Typography is `title-sm` in `on-primary` (white), all-caps with 0.05em tracking.
- **Secondary Button:** `surface-container-highest` background with no border. A subtle "lift" on hover via `surface-bright`.
- **Chips:** Used for pizza toppings or dietary tags. Use `secondary-container` with `on-secondary-container` text. Roundedness `full`.

### Cards & Menu Items
- **The Forbid Rule:** No divider lines between menu items.
- **The Style:** Use `surface-container-low` for the card body. Use `spacing-4` padding. Imagery should "pop" out of the container using a negative margin-top to create a 3D overlapping effect.

### Input Fields
- **State:** Understated. Use a `surface-container-high` background with a `2px` bottom-only border in `primary` that activates only on focus. This mimics NYC subway signage and architectural lines.

### Featured Component: "The Slice Selector"
A specialized horizontal scroll component using `surface-container-lowest` cards. Each card uses a `xl` (0.75rem) corner radius on the top-left only, creating an asymmetrical, custom-designed feel.

## 6. Do’s and Don'ts

### Do:
- **Overlap Elements:** Let a pizza image overlap a headline. It creates "Street-Food Energy."
- **Use Color as Structure:** Use a full-bleed `primary-container` section to break up long scrolls of white text.
- **Respect the Spacing Scale:** Stick strictly to `8`, `12`, and `16` for vertical section rhythm.

### Don’t:
- **Don't use pure #000000 for text:** Use `on-surface` (#1c1b1b) to keep the editorial feel soft and readable.
- **Don't use standard shadows:** Avoid the "floating box" look. Use background tonal shifts first.
- **Don't center everything:** Use left-aligned typography for a "New York Times" editorial vibe, punctuated by large, centered imagery.

### Accessibility Note:
Ensure that `on-primary` text on `primary` backgrounds maintains a 4.5:1 contrast ratio. When using `secondary` (Gold), pair it only with `on-secondary-fixed` (Dark) for legibility.```