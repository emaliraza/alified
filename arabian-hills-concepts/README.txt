ARABIAN HILLS DEVELOPERS — WEBSITE DESIGN CONCEPTS
Crafting Distinctive Living & Commercial Spaces
====================================================================
MOCKUP — FOR DESIGN SELECTION ONLY


WHAT'S IN THIS FOLDER
--------------------------------------------------------------------
  index.html      Launcher. Shows the 3 concepts side by side, with
                  colour swatches, typography and a comparison table.
  concept1.html   Concept 1 — The Heritage Atelier (classic luxury)
  concept2.html   Concept 2 — The Contemporary Edge (modern minimal)
  concept3.html   Concept 3 — The Cinematic Journey (immersive 3D)
  README.txt      This file.

Each concept is ONE self-contained HTML file. There is no build step,
no npm and nothing to install.


HOW TO OPEN
--------------------------------------------------------------------
1. Keep the four .html files together in the same folder. They link
   to each other.
2. Double-click index.html. It opens in your default browser.
3. Click "View Concept" on any card, or press 1, 2 or 3.

Use an up-to-date Chrome, Edge, Safari or Firefox.

You need an internet connection for the full experience. Fonts
(Google Fonts), photography (Unsplash) and the motion libraries
(Three.js, GSAP + ScrollTrigger, Lenis and Tailwind) all load from
public CDNs. Offline, every page still renders: it falls back to
system fonts, designed gradient and line-art artwork in place of
photos, and static versions of the 3D scenes.


HOW TO PRESENT
--------------------------------------------------------------------
- Go full-screen: F11 (Windows) or Ctrl+Cmd+F (Mac).
- Keyboard shortcuts work on every page:
      1 / 2 / 3  jump to that concept
      0          back to the overview (index.html)
- Each concept has a floating badge at the top-right (for example
  "Concept 1/3 — The Heritage Atelier") and a switcher just below it
  (Overview · 01 · 02 · 03). On phones the badge sits in the header;
  tap it to show the switcher.
- Suggested order: open index.html, then walk through 1 → 2 → 3, and
  finish back on the comparison table to decide.
- Concept 3 is a scroll-driven film. Scroll slowly with a mouse wheel
  or trackpad and pause at each chapter. The Journey bar at the
  bottom (Site → Tower → Lobby → Units → Contact) shows progress; you
  can click any milestone to fly there.
- On Concept 3 you can force a mode for demonstration:
      concept3.html?static=1   shows the mobile/static fallback
      concept3.html?webgl=1    forces the live 3D (e.g. on a tablet)
- To show the mobile layouts, narrow the browser window or use the
  browser's device toolbar (F12, then the phone icon).


WHAT EACH CONCEPT EMPHASISES
--------------------------------------------------------------------
CONCEPT 1 — THE HERITAGE ATELIER  (Classic timeless luxury)
  Feeling:    Established, trustworthy, heritage. A London/Dubai
              property brochure come to life.
  Palette:    Ivory #F7F3EC · Bronze Gold #B08D57 · Espresso #2B2118
              · Warm Sand #D9C7A7
  Type:       Cormorant Garamond (display, italic accents) + Jost
  Layout:     Symmetrical, centred and editorial. The logo sits
              between a split navigation. Large numbered sections
              (01–05) are separated by thin gold rules. Features an
              arched image triptych, refined bordered service cards
              and a staggered project grid.
  Motion:     Slow Ken Burns on the hero, gentle parallax, fade-up
              reveals and gold underline sweeps on buttons.
  Signature:  A vertical gold scroll-progress rail on the left edge,
              with clickable section markers.
  Best for:   Conveying trust, heritage and stability to investors,
              families and institutions.

CONCEPT 2 — THE CONTEMPORARY EDGE  (Modern minimalist)
  Feeling:    Bold, spacious and design-forward, like a leading
              architecture practice.
  Palette:    Charcoal #141414 · Off-White #F2EFE9 · Champagne
              #C9A961 · Cool Grey #8A8A8A
  Type:       Space Grotesk (oversized display) + Inter
  Layout:     Asymmetric 12-column grid with lots of negative space.
              Section labels stay sticky as you scroll, and dark and
              light bands alternate. Services are full-width rows
              that fill with gold on hover. Projects sit in a
              horizontal scroll-snap gallery that you can drag.
  Motion:     Text slides up from behind masks. A gold 3D wireframe
              tower (Three.js) draws itself, rotates slowly and reacts
              to the mouse. Lenis provides smooth scrolling. Images
              shift from greyscale to colour on hover. Live
              Dubai/Lahore clocks add a small detail.
  Signature:  A custom gold-dot cursor that expands on interactive
              elements with contextual labels (View, Drag, Enquire).
              It is hidden on touch devices.
  Best for:   Positioning Arabian Hills as a design-led,
              forward-thinking developer.

CONCEPT 3 — THE CINEMATIC JOURNEY  (Immersive scroll-driven 3D)
  Feeling:    An Apple product launch meets a luxury property film.
              The "wow" option.
  Palette:    Midnight Navy #0A1628 · Liquid Gold #D4AF37 · Soft Sand
              #E8DCC4 · Deep Teal #1A3A4A
  Type:       Cinzel (regal display, gold gradient) + Manrope
  Experience:
              - On load, a stylised office tower rises from a glowing
                grid, with a gold "construction" scan line.
              - Scrolling flies the camera from an aerial view of the
                site, around the tower and through the lobby doors.
                Inside are gold columns, light shafts and a rotating
                ring sculpture. The camera then rises past lit units
                to the crown and ends on a wide skyline shot.
              - Chapter panels pin and fade in at each milestone.
              - Service cards float and drift in, and tilt in 3D on
                hover.
              - Each project card has a live 3D building thumbnail.
                Click it to open a detail panel.
              - Statistics count up as they come into view.
              - Atmosphere comes from dust motes, traffic light
                streams, stars and gold light bloom.
  Signature:  The Journey bar: Site → Tower → Lobby → Units → Contact.
  Fallback:   Phones, reduced-motion settings and devices without
              WebGL get a static cinematic version. It keeps the
              same content and adds a photographic hero with parallax
              and drifting gold dust.
  Best for:   Flagship launches and campaign moments that need
              maximum impact.


TECHNICAL NOTES (for the development team)
--------------------------------------------------------------------
- Each page's design system is hand-written CSS at the top of the
  file, using custom properties (tokens). This keeps every page
  intact even if a CDN fails.
- Tailwind (Play CDN 3.4.16) is loaded as an optional utility layer.
  Preflight is disabled and the brand colours and fonts are
  registered, so you can extend it with utilities straight away.
- Library versions:
      Three.js r128, GSAP 3.12.5 + ScrollTrigger (cdnjs),
      Lenis 1.1.13 (jsDelivr).
  For production, move to the current Three.js with ES modules and
  self-host the libraries.
- Graceful degradation:
      - Scroll reveals, counters, menus, forms and the review chrome
        use IntersectionObserver and plain JavaScript.
      - GSAP and Lenis only add enhancements on top.
      - If Three.js or WebGL is unavailable, Concept 2 draws its
        tower as an SVG and Concept 3 switches to static mode.
      - Each photo tries a backup image once, then shows designed
        CSS artwork with a caption.
- Performance:
      - Animations use transform and opacity only.
      - 3D renders pause when off-screen.
      - Concept 3 lowers its pixel ratio automatically if frames
        drop, and phones get the static version.
- Accessibility: semantic landmarks, a skip link, labelled forms,
  keyboard-operable galleries, menus, modal and cards. Contrast is
  checked and prefers-reduced-motion is respected.
- The code is lightly commented by section so the chosen concept can
  be extended into the full site.


PLACEHOLDER CONTENT
--------------------------------------------------------------------
- All photography is placeholder imagery from Unsplash. Replace it
  with real project renders and photos.
- The three projects (The Horizon Towers, Al Noor Residences, Hills
  Business Park) are illustrative. So are the office addresses, phone
  numbers (+971 4 000 0000, +92 42 0000 0000), the email address
  (info@arabianhills.co), the testimonial and the statistics.
- The contact forms are mock-ups. They show a confirmation and send
  nothing.


AFTER SELECTION — SUGGESTED NEXT STEPS
--------------------------------------------------------------------
1. Confirm the direction, plus any elements to borrow from the other
   concepts (for example, Concept 3's Journey bar on Concept 1).
2. Gather brand assets (final logo, real renders, project data), then
   finalise the sitemap: Home, About, Services, Projects (with
   detail pages), Investors, Careers, Contact.
3. Produce high-fidelity designs for the inner pages and mobile.
4. Build on a CMS so the team can manage projects and enquiries,
   with forms connected to the CRM or sales inbox.
