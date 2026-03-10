# TrustArc Banner Override Notes

## Why this fixes your issues

1. **Desktop CTA too low**: The modal uses a 3-row grid (`header / scrollable body / footer`) instead of relying on legacy fixed/min heights that push the action area downward.
2. **White background covering copy on narrower desktop**: Only the footer keeps a white background and top border; the body is an independent scroll region, preventing overlap artifacts.
3. **Mobile overflow beyond viewport width**: The overlay uses viewport-aware padding and modal width is capped at `100%` with safe-area handling.

## Integration checklist

- Load `trustarc_banner_override.css` after TrustArc default styles.
- Keep only selectors that match your environment. If your tenant emits different IDs/classes, map these selectors:
  - Overlay: `#truste-consent-track` / `.truste_box_overlay`
  - Modal: `#truste-consent-content` / `.truste_box`
  - Message: `#truste-consent-text` / `.truste-message`
  - Footer buttons wrapper: `#truste-consent-buttons` / `.truste_buttons`
- Remove any older overrides that set fixed heights on banner containers.

## Optional hardening

If TrustArc injects inline styles with high priority, keep `!important` as shown. If your environment allows, reduce `!important` usage after verifying cascade order.
