# Goblin Node — Full Changelog

All changes are listed in reverse chronological order, grouped by release branch.
For consumer-facing release notes see the dated files alongside this one.

---

## v1.6.0 -- Sep 7, 2026

### New Features

- **Float16 HDR and OpenEXR [Pro]** -- Preserve brighter color and finer tonal detail through core color, math, channel, and sampling nodes, then export half-float OpenEXR textures.
- **Image Sample Node [Pro]** -- Look up an image through a UV texture, with repeat, clamp, or mirror addressing plus nearest or bilinear filtering.
- **Advanced Animation Export [Pro]** -- Export graph animation as image sequences, sprite atlases, or animated GIFs with palette and dithering controls.
- **Richer 3D Material Preview** -- Add bloom, chromatic aberration, FXAA, self-reflections, and self-shadowing to material inspection.
- **Smarter Quick Add** -- Add favorites, recent-use suggestions, keyboard navigation, and touch placement for faster graph construction.

### Improvements

- **Fluid Animation Playback** -- Cached preview frames, timeline stepping, and seamless loops make animated textures easier to inspect.
- **More Confident Exporting** -- Palettized PNG previews, output inspection, palette-asset support, and direct single-file downloads refine the export workflow.
- **Reliable Local Work** -- Durable graph history and recovery protect projects during interrupted persistence.
- **Responsive Workspace** -- Preview, node-drag, selection, toolbar, alignment, and touch interactions are more dependable.

### Bug Fixes

- **High-Precision Accuracy** -- Preserved float16 metadata and corrected HSB, curves, atlas, Tile Generator, and palettize behavior.
- **Stable Animation and Export** -- Fixed cached playback, live FPS, graph timing, GIF encoding, GPU parity, and animation filenames.
- **Preview and Interaction Reliability** -- Corrected pinned previews, transform and paint alignment, fullscreen controls, compact-zoom sizing, node dragging, selection, and toolbar overlap.
- **Safe Project Persistence** -- Prevented stalled saves and fallback autosave data loss.

## v1.5.0 -- Aug 27, 2026

### New Features

- **Animation Workflows** -- Add a Time node and animation preview controls for frame-based texture creation and inspection.
- **Material Graph Import** -- Generate connected material graphs from loose images and ZIP archives, with media sources available from the editor insert menu.
- **Color and Math Tools** -- Add Separate HSB, Combine HSB, Channel Swizzle, and per-pixel Math operations for more direct channel and image manipulation.
- **Texture Placement Controls** -- Extend Tile Generator with symmetry and size modes, and let image nodes inherit tiling settings from the graph.
- **Preview and Export Workspace** -- Use viewport transform gizmos, graph-input controls in Output preview, and export-time bit-depth settings in a responsive export workspace.

### Improvements

- **Responsive Graph Editing** -- Graph panning, zooming, dragging, marquee selection, edge rendering, and paint handoff are coalesced and isolated so large graphs stay responsive.
- **Workspace Navigation** -- Editor tabs persist across Home, Projects, and Assets, while the catalog receives clearer glass styling, compact actions, and responsive mobile layout.
- **Graph Organization** -- Add a draggable, resizable minimap with selected-node previews, configurable interaction quality, foldable alignment tools, and clearer render-status feedback.
- **Deterministic Variation** -- Set a seed per renderable node, with graph instances deriving stable child seeds for controlled procedural variation.
- **Touch and Mobile Controls** -- Use a free-pan hand tool, preview pinch/orbit gestures, persistent finger-drawing preference, mobile density settings, and controls sized for localized labels.

### Bug Fixes

- **Rendering Parity** -- Corrected CPU/GPU transform orientation, resolution-independent transform and emboss controls, procedural noise artifacts, curves alpha handling, and native 16-bit RGBA compositing.
- **Graph Type and Routing Accuracy** -- Fixed Math image/scalar type inference, channel-aware noodle colors, parameter-edge inheritance, graph-input visuals, node defaults, and exposed-parameter reset behavior.
- **Preview Reliability** -- Fixed stale selected previews, pinned output slots, tab-switch regeneration, transform gizmo visibility, render timing refresh, paused-state indicators, and floating preview toggles.
- **Input and Selection Reliability** -- Restored node dragging, marquee selection, empty-canvas deselection, Quick Add gesture boundaries, Apple Pencil targets, preview history gestures, and touch pinch/orbit continuity.
- **Catalog and Platform Stability** -- Prevented unwanted save prompts, corrected compact mobile actions, preserved empty frame titles, and made iOS Appflow dependency retrieval more reliable.

## v1.4.0 -- Aug 18, 2026

### New Features

- **Complete Native 16-bit Color Pipeline [Pro]** -- Native high-precision grayscale, RGB, and RGBA data now flows through generators, filters, transforms, warps, subgraphs, atlases, paint, and PNG/TIFF export.
- **Vector Warp [Pro]** -- Added color-vector-map distortion with DirectX and OpenGL orientation options.
- **Precision Numeric Editing** -- Added typed numeric drafts, explicit step controls, and touch/stylus-safe precision scrubbing.
- **Interior Box 3D Preview** -- Added an inward-facing box model for inspecting materials in an enclosed environment.

### Improvements

- **Render Controls** -- Improved inherited render-scale and bit-depth settings, fullscreen controls, and node metadata reporting.
- **Mobile Editing** -- Added compact header navigation and improved input, dropdown, and preview-panel behavior on smaller touch devices.
- **Home Workspace** -- Added a particle field, canvas grid effect, and localized rotating hero copy.

### Bug Fixes

- **Rendering Accuracy** -- Preserved native precision through color adjustments, blurs, transforms, warps, flood fill, atlas operations, and subgraphs.
- **Editor Reliability** -- Fixed stale bit-depth badges, exposed parameter actions after duplication, narrow inspector controls, long renders, and pinned preview behavior.
- **Touch and Platform Stability** -- Recovered interrupted iOS gestures and improved Apple Pencil dropdown interactions, graph package pickers, local project fallback, and web build database setup.

## v1.3.1 -- Aug 10, 2026

### New Features

- **Flexible Render Settings** -- Set a node output relative to its input, the graph, or an exact resolution, with bit-depth settings ready for higher-fidelity workflows.
- **Expanded Flood Fill Toolkit** -- New Flood Fill to Index, BBox Size, Grayscale Color, and split luminance/color controls enable more precise regional masks.
- **New Texture Tools** -- Added Auto Crop, Normal Combine, Tile Safe Transform, and GPU-accelerated FXAA.

### Improvements

- **Graph Control** -- Compact selection actions, editable/reorderable graph input ports, and fullscreen project settings improve complex-graph editing.
- **Pro Access** -- Newly released Pro nodes are gated consistently.

### Bug Fixes

- **Accurate Sampling** -- Mismatched node resolutions use pixel-exact resampling, and Flood Fill samples its color input per region.
- **Editor Reliability** -- Stabilized render metadata, pinned previews, disabled-node passthrough, preview controls, and Dot insertion.
- **Mobile and GPU Polish** -- Controls respect the Dynamic Island and GPU Emboss orientation matches the expected preview.

## v1.3.0 -- Aug 3, 2026

### New Features

- **Precision Paint Grid** -- Axis, straight, smooth, and absolute snapping modes guide paint strokes with more control.
- **Continuous Grid Paths** -- Paint paths move through grid intersections while preserving intentional diagonal turns.

### Improvements

- **Quad Transform Controls** -- Transform controls live in the Selected preview and align with texture bounds.
- **Minimap Navigation** -- A tap recenters the graph after pointer release.

### Bug Fixes

- **Quick Add** -- New nodes mount and refresh their handle bounds before edges connect.
- **GPU Transforms** -- Removed a diagonal seam from quad transforms.
- **Editor Reliability** -- Improved warp resolution updates, Apple Pencil curve taps, catalog navigation, and preview-node interactions.

## v1.2.9 -- Jul 31, 2026

### New Features

- **Preview Nodes** -- Visual node presentation with texture-output cards directly in the graph and detailed controls in the Selected preview.

### Improvements

- **Catalog Performance** -- Thumbnails decode on demand and nonessential editor asset loading is deferred.
- **Preview Performance** -- Preview-node thumbnails are isolated from GPU rendering; inactive preview and material resources are released sooner.
- **Render Worker Scope** -- Workers receive only graph dependencies needed for the active render.

### Bug Fixes

- **Touch Controls** -- Detached preview control works reliably on touch devices.
- **3D Preview UVs** -- Corrected plane and cube-cap UV orientation.
- **Preview Stability** -- Stabilized the inspector portal and sanitized preview-node worker data.
- **Memory Management** -- Bounded editor history and render buffers; fixed resource cleanup for disabled GPU acceleration and inactive material slots.

## v1.2.8 — Jul 30, 2026

### New Features

- **Expanded Paint Tools** — Collapsible paint preview tools, expanded brush controls, compositing options, and live tiled strokes across the viewport.
- **Texture Bounds Frame** — Toggleable color-coded frame around texture bounds with color picker in settings.
- **Preview Filtering Toggle** — Independent 2D preview filtering control decoupled from zoom level.
- **Cache Status Badge** — Node headers now show cache status badge (Database/RotateCcw icons) with distinct GPU/cache icons.
- **Replace Node Button** — Contextual button to replace a node inline from the selection bar.
- **Marquee Threshold** — 8px minimum rect size guard prevents stale micro-drag selection rects.

### Improvements

- **Editor Tabs** — Tabbed editor navigation replacing project return flow, with drag reordering.
- **Nested Catalog** — Graph and asset browser rebuilt as a nested catalog with custom collections, colors, drag-to-organise, trash lifecycle, and persistence.
- **Detachable Preview** — Preview panel can be popped out to a separate window, with fullscreen mode and pinned controls. Works on iOS and Android.
- **Contextual Action Bar** — Horizontal action bar above node/edge selections with fit view, disable/expose, docs, insert node, and delete actions.
- **Edge Quick-Insert** — Green plus button on selected edges to insert nodes inline via quick-add with marquee selection support.
- **Dilate/Erode Mask [Pro]** — New node for mask dilation and erosion with GPU acceleration under Color Channels.
- **Progressive Rendering** — Main-thread fallback now yields between nodes to keep UI responsive.
- **Export Graph Package** — Export button available directly from the output panel.
- **Material Socket Auto-Rename** — Outputs panel supports automatic material socket renaming.
- **Render Diagnostics** — Exposed renderer memory estimates and WebGL tracking in resource monitor.
- **High Bit Depth Gating** — 16/16f/32f modes disabled unless node opts in via `NODE_HIGH_BIT_DEPTH_CAPABLE`.
- **Preview Filtering** — Nearest/pixelated filtering activates at previewZoom threshold for intuitive zoom-to-pixel behaviour.
- **Tile Button** — Renamed to Tiling On/Off with emerald/amber colour states.
- **Autosave Stability** — Autosave interval no longer resets on every node/edge edit (ref-based handle), crash-safe and edit-version aware.
- **Fullscreen Preview** — Minimize button replaces hide button when in fullscreen mode.
- **Paint Tools** — Collapsible preview tools, expanded brush controls, compositing, settings preserved across node swaps.
- **Catalog Navigation** — Refined navigation with persisted collection colors and deliberate browsing experience.
- **Cache Performance** — Persisted nodeHashMemo; reordered cache check to skip hash for dirty-based cache hit.
- **Paint Performance** — Reduced brush point density with incremental texture flushes during stroke.
- **i18n** — Added disable_cache/enable_cache keys to all 8 locales.

### Bug Fixes

- **React Flow removeChild Crash** — Removed imperative DOM cleanup of React Flow's selection nodes, fixing `NotFoundError` in `UserSelection`/`ViewportPortal`.
- **iOS WebView** — JS Heap lines now hidden when unavailable in WKWebView.
- **iPad WebKit** — Sanitized node/edge data before worker `postMessage` to prevent `DataCloneError`.
- **Paint Worker Crash** — Prevented `document.createElement` call in web worker by using `this.createCanvas()`.
- **PaintOverlay Tiling** — Fixed tilingX/tilingY fallback to legacy tiling boolean.
- **Paint Brush Wrapping** — Brush footprints now wrap correctly across tiled edges.
- **Paint Stroke Alignment** — Fixed preview alignment and resolution across committed strokes.
- **Stylus Pressure** — Preserved pressure sensitivity across committed paint strokes.
- **Texture Bounds Frame** — Anchored to preview texture, kept to original tile in tiled preview.
- **SVG Anti-Aliasing** — Removed `backdrop-blur` from `SelectionContextBar` to prevent WebKit SVG anti-aliasing loss.
- **Marquee Selection** — Added 8px minimum rect size guard to prevent micro-drag stale selection rects.
- **Preview Filtering** — Uses previewZoom threshold instead of effectiveScale for 2D filtering.
- **Fullscreen Preview** — Replaced hide button with exit fullscreen button in fullscreen mode.
- **Detached Preview** — Preserved detached window after fullscreen, kept visible when panel hidden.
- **Blur Mode** — Restored with separate scale control.
- **Context Bar** — Reordered buttons, tailored actions for frame/dot utility nodes, positioned from noodle sockets for multi-edge selections, kept constant-size in graph space.
- **Tutorial Stability** — Graph preset rendering stabilized; tutorial stops when leaving the project.
- **Autosave Crash Safety** — Hardened against memory pressure, stabilized interval via ref-based handle.
- **Mobile Graph Rendering** — Hardened against memory pressure, always collect render metrics with memory diagnostics.
- **Dilate Erode** — Categorized under Color Channels, GPU badge fixed.
- **Cache Badge** — Fixed toggle icon and state display with translation issues.
- **Edge Plus Button** — Locked to graph space using viewport transform, reverted to simple edge midpoint for marquee selection.

## v1.2.7 — Jul 22, 2026

### New Features

- **Paint Node** — Full paint system with soft brush, eraser, opacity, pressure size/opacity, clear layer, and native color picker.
- **Shape Extrude [Pro]** — CPU + GPU 3D mesh extrusion with analytical ray-shape intersection.
- **Atlas Pack & Atlas Split [Pro]** — Texture atlas packing and splitting with correct scaling.
- **Graph Minimap** — Color-coded viewport minimap with minimize button in zoom stack.
- **System Fonts** — Text node supports both Google Fonts and system fonts.

### Improvements

- **Node Color System** — Unified accent colors across graph, minimap, and UI (single source of truth).
- **Graph Node Headers** — Changed to red for faster visual identification.
- **Soft Brush & Pressure** — On Paint node now supports soft brush modes and pressure sensitivity.
- **Release Workflow** — Prebuild checks run automatically before tagging; release artifacts organised into per-version folders with templates.

### Bug Fixes

- **Emboss** — Direction corrected.
- **Tile Generator** — Color map mapping fixed.
- **Cylinder Texture** — Stretching fixed.
- **Minimap Colors** — Frame node minimap colours now match graph view.
- **Paint Node** — Stroke alignment, double rendering, and reordered controls fixed.
- **Premium Tagging** — Shape extrude, atlas pack, and atlas split correctly marked as [Pro].
- **Atlas Accent** — Pack and Split nodes use correct accent colour (mix node accent).
- **Transaction Safety** — Read/write transactions now correctly await `tx.oncomplete`.
- **Font Loading** — Text node correctly includes both Google Fonts and system fonts.

## v1.2.6 — Jul 21, 2026

### New Features

- **Shape Node** — Added hemisphere, cone, and capsule shapes (capsule uses soft gradient falloff with configurable capsule length).
- **Blend Node** — 8 new blend modes: Color Dodge, Color Burn, Linear Burn, Vivid Light, Linear Light, Hard Mix, Exclusion, Divide.
- **Clone Stamp** — New node for texture repair and duplication (CPU + GPU).
- **6 New [Pro] Nodes** — Simplex Noise, Gabor Noise, Crystal Noise, BnW Spots, Swirl, Spherize.

### Improvements

- **Coordinates Transform** — from/to mapping corrected (cartesian↔polar now works as labeled).
- **Swirl node** — added directional control (CW/CCW) and refined intensity ranges.
- **Capsule shape** — sizeX/sizeY now properly stretch/squish the shape.

### Bug Fixes

- **Voronoi** — Fixed missing maxSeed declaration causing runtime errors.
- **Noodle snapping** — Sort by nearest socket instead of nearest empty; reduced snap distance.
- **Normal Map** — Orientation corrected.
- **Transform** — Tiling mode now interacts correctly with repetitions.
- **Image node** — Always outputs graph canvas dimensions.
- **Capsule** — Changed from hard-edged to smooth gradient falloff.
- Various UI fixes (layout thrashing, missing useCallback, Perlin label sync, tailwind token compat).

---

## v1.2.5 — May 27, 2026

### New Features

- **New Languages** — Full support for Japanese, Korean, and Simplified Chinese.
- **Noodle Navigation** — Added a new section for node and noodle connections.
- **Per-Node Bit Depth** — Added a new per-node bit depth setting with dropdowns and badges.
- **Node Previews** — You can now preview noodles directly in the node preview panel.

### Improvements

- **GPU Acceleration** — Added GPU processing for Curves, Quad Transform, Threshold, Grayscale, Invert, Quantize, Height Blend, Solid, Autolevels, Palettize, and many more.
- **Blend Modes** — Added Add Sub, Pin Light, Hard Light, Color, Hue, Saturation, and Luminosity blend modes.
- **Improved Aesthetics** — Enhanced node and noodle connections with better accent colors and icons.

### Bug Fixes

- **Graph Editor UX** — Fixed numerous issues with selected noodle/node UX and prevented nodes from deselecting on save.
- **Localization Formatting** — Fixed translation key typos and missing translation strings across dozens of nodes.
- **Preview Panel UX** — Context action buttons are now properly left-aligned, and graph output ports now start collapsed instead of expanded.

---

## v1.2.4 — May 20, 2026

### New Features

- **4 New Languages** — Spanish (ES), German (DE), French (FR), and Brazilian Portuguese (PT-BR) are now fully supported. Switch languages from User Settings.
- **First-Launch Tutorial** — A guided interactive walkthrough for new users covering the core graph workflow step by step.
- **GPU Median: Channel-Aware Shaders** — Dynamic shader generation now detects input channel count at runtime; a lighter grayscale variant is used for single-channel inputs, reducing GPU load significantly.

### Improvements

- **Memory-Aware Rendering** — The texture engine now proactively enforces its cache budget before each node render, preventing memory spikes that could stall large graphs.
- **Unsaved-Changes Modal** — Dialog height now adapts to longer localised action labels, keeping the UI clean across all languages.
- **Localisation Infrastructure** — Added translation parity verification script, text-length truncation guidelines, and roadmap language-to-region mapping.

### Bug Fixes

- **GPU: Median Context Loss** — Fixed context loss on large Median filter operations; added recovery cooldowns to prevent cascading GPU failures on iPad.
- **UI: Nested Modal Width** — Fixed a Radix UI scroll-lock side-effect that caused the graph/assets modal to shrink in width after nested dialog interactions.
- **Editor: ImageNode Sluggishness** — Eliminated redundant re-renders caused by the Image node presence in the graph.
- **i18n: Missing Output-Node Keys** — Resolved absent parameter translation keys causing untranslated strings in localised builds.
- **UTF-8 BOM** — Removed BOM from `package.json` and the release-note generation script output.

---

## v1.2.3 — May 18, 2026

### Improvements
- **Per-Output Render Scales**: Added per-output render scale sliders to the export panel.
- **Smarter Previews**: Preview upstream sources and actual dimensions when passthrough nodes are selected.
- **Performance**: Debounced preview dimension estimates and decoupled them from the nodes array.

### Bug Fixes
- **Editor Loops**: Fixed bugs causing the entire graph to unnecessarily rebuild on selection change.
- **Rendering Loops**: Guarded render dimension resolution against cycle loops from `dot` portals.
- **WebGL Stability**: Queued background render requests to prevent WebGL stalls on iOS.

---

## v1.2.2 — May 16, 2026

### New Features

- **5 Nodes Now Free** — Dot, Frame, Comment, Normal Map, and Ambient Occlusion are now available on the Free plan, giving free-tier users access to essential utility and analysis tools.
- **Selection-Aware Fold/Unfold** — The Minimize/Expand buttons in the toolbar now operate only on selected nodes when a selection exists; with no selection, all nodes are affected as before.
- **Copy-Paste Preserves Connections** — Internal noodle connections between selected nodes are now restored automatically after a copy-paste or duplication.
- **Workflow Integrity Gates** — Pasting or duplicating selections containing Pro nodes now triggers an upgrade prompt to protect graph integrity.

### Improvements

- **Export Panel Cleanup** — The Export Outputs dialog has been reorganized with collapsible sections for a cleaner, less cluttered experience.
- **Node Badge Icons** — GPU and CPU mode indicators on node headers now use icons (⚡ / chip) instead of text labels.
- **Image Crop Precision** — Image node crop controls now use a normalized coordinate system for more predictable behavior across resolutions.

### Bug Fixes

- **Normal Map Parity** — CPU rendering path now matches GPU and OpenGL-standard gradient orientation for Normal Map.
- **Export Seed Accuracy** — Exports now correctly apply the graph's global seed, ensuring previews and exported files match.
- **Preview Tab Persistence** — Saving a graph no longer resets the active preview tab (Selected / Output / 3D).
- **Quick Menu Node Placement** — Fixed node coordinate calculation when creating nodes via the quick-add menu.
- **Engine Stability** — Resolved a variable shadowing bug in the texture engine that caused zero-intensity blurs and transform offsets under certain render scale configurations.
- **Render Performance** — Organizational node moves no longer trigger unnecessary graph re-renders.
- **Image Node Drag** — Prevented the browser's native drag from interfering with image node thumbnail interactions during canvas movement.

---

## v1.2.1 — May 14, 2026


### New Features

- **Massive GPU Expansion** — GPU acceleration is now available for Blend, HSL, Mirror, Normal Map, Flood Fill, Levels, Curvature, Sharpen, and many more, significantly speeding up texture generation.
- **Dynamic Project Thumbnails** — Configure your project thumbnails to update automatically from any node output or 3D preview.
- **Precision Image Controls** — The Image node now supports built-in cropping and offsetting, perfect for precise asset placement.
- **Per-Node Render Scaling** — Fine-tune performance and quality with individual render scale controls on all rendering nodes.
- **4-Mode Directional Tiling** — New tiling options (None, Horizontal, Vertical, Both) for granular control over texture repetition.
- **Foldable Output Node Ports** — Reorder and fold output ports for better organization of final assets.

### Improvements

- **Foldable Preview Sections** — Tidy workspace with collapsible headers in the selection and output panels.
- **Smart Node Placement** — Added intelligent collision detection to prevent nodes from stacking during creation.
- **Automatic Frame Color Rotation** — Frame colors now automatically rotate their hue for easier visual grouping.
- **Modern Defaults** — GPU acceleration and glassmorphism headers are now enabled by default.
- **Memory & Performance Optimizations** — Significant optimizations for large graphs, including memoization and multi-heuristic node scoring.

### Bug Fixes

- **Apple Pencil Stability** — Resolved a critical WebKit issue causing 'missed clicks' when using a stylus on iPad.
- **Database Resilience** — Added an automated reconnection loop to handle IndexedDB termination in Safari/WebKit.
- **Render Corrections** — Fixed artifacts in Flood Fill and Median nodes; corrected non-linear ramps in gradients.
- **iOS Display Quality** — Resolved image aliasing on iPad when zooming in/out of the 2D preview.
- **UI & Schema Fixes** — Restored missing GPU badges, fixed project thumbnail persistence, and resolved multiple layout shifts.

---

## v1.2.0 — May 5, 2026

### New Features

- **3D Preview System** — A completely new real-time PBR 3D viewport with environment lighting, physical material slots (Normal, Height, Roughness, Metalness, AO), and real-time mesh displacement.
- **Splatter Circular Node** — New generator for creating complex circular distributions and patterns.
- **Math Node** — Perform complex float and integer calculations directly in your graph. Supports dynamic data types and real-time evaluation.
- **GPU-accelerated node rendering (experimental)** — Massive performance boosts for Warp, Distance, Noise, Box Blur, Blur HQ, and Slope Blur.
- **HDRI Environment Suite** — 6 new high-quality environment presets from Poly Haven with a new high-fidelity "Studio" default.
- **Quick Math contextual actions** — Rapidly create and connect nodes using keyboard shortcuts and contextual menus.
- **3D Preview statistics** — Real-time vertex and triangle counts added to the 3D viewport.
- **Wireframe & Shadow toggles** — Inspect mesh topology and lighting directly in the 3D preview.
- **Environment light intensity** — Dedicated slider to control the brightness of environment maps.
- **Texture filtering & Mipmaps** — Improved texture rendering quality with configurable filtering and mipmap generation.
- **Multi-Directional Warp node** — New node that applies distortion from multiple directions simultaneously.
- **Non-Uniform Blur node** — Blur with independent horizontal and vertical radius control.
- **Tiling toggle on warp nodes** — Warp, Directional Warp, Multi-Directional Warp, and Distance nodes now have per-node tiling toggle buttons.
- **Adaptive Quality Governor** — Automatic resolution scaling to keep the editor responsive on all devices (mobile/desktop).
- **Resource Monitoring Panel** — Real-time tracking of RAM and VRAM usage directly in the toolbar.

### Improvements

- **Improved Slope Blur** — Reworked Slope Blur using an iterative warp chain for professional-grade results.
- **Foldable preview panels** — Selection, Output, and 3D panels are now collapsible for a cleaner workspace.
- **Enhanced noodle workflow** — Better contextual actions, smarter node snapping, and improved UX efficiency.
- **Zoom range extended** — minimum zoom-out lowered to 0.01 for both 2D and 3D preview.
- **Angle widgets reoriented** — matching industry-standard conventions.
- **Local web build configuration stabilised** — (`dev:web`, `build:web:release`).
- **Node library filters** — added to library panel, quick-add menu, and Node Reference dialog.

### Bug Fixes

- **iOS Stability** — Resolved critical pointer capture crashes affecting iOS and Capacitor builds.
- **3D Rendering fixes** — Resolved shading artifacts and fixed shown environment not matching rotation values.
- **Node logic corrections** — Fixed Blend and Math nodes from incorrectly passing the wrong input on disable.
- **Edge Detect Scaling** — Fixed resolution-dependent scaling issues for the Edge Detect algorithm.
- **Fixed inconsistent zoom scaling** — resolved issues between single-tile and infinite-tiling preview modes.
- **Fixed blur node artefacts** — corrected incorrect tiling at certain radii.
- **Fixed Node Reference dialog** — now opens the correct node on first interaction.

---

## patch1 — Development Phase 2026

### Progress

- **Graph instances** — Initial work on referencing and embedding other graphs as reusable instances.
- **Pro plan / monetization** — RevenueCat-backed entitlement system setup.
- **Graph package import/export** — Initial `.gnproj` / `.gnpack` format development.
- **Expose parameters on nodes** — Core logic for marking node parameters as graph inputs.
- **Batch export** — Basic implementation of "Export All Outputs".

### Improvements

- Graph load normalises legacy node types: `output→graphOutput`, `group→frame`, `bevel-with-emboss-fields→emboss`.
- Node library panel defaults utility categories to collapsed.
- Preview panel interactions smoothed.
- Improved tablet and touch support across the editor.

### Bug Fixes

- Fixed multiple edge cases in graph package import (dependency ID remapping, asset source map).
- Fixed premium node gate not applying correctly on graph package import.

---

## main — January 2026

### New Features

- **Tile Generator node** [Pro] — Generate seamless repeating tile patterns with blend mode, variance, and luminosity offset controls.
- **Directional Warp node** [Pro] — Warp a texture along a direction driven by a separate intensity input.
- **Levels node** — Contrast and brightness input/output level adjustment.
- **Auto Levels node** — Automatic contrast normalisation.
- **Gradient Map node** — Remap grayscale values to a configurable colour gradient.
- **HSL Adjustment node** — Hue, Saturation, and Lightness adjustment.
- **Bevel / Emboss node** [Pro] — Create shaded bevel and emboss effects from height data.
- **Ambient Occlusion node** [Pro] — Fast horizon-based AO from a heightmap.
- **Highpass node** [Pro] — Extract high-frequency detail from a texture.
- **Normal Map node** [Pro] — Generate a normal map from a height input.
- **Distance node** [Pro] — Per-pixel distance field generation.
- **Edge Detect node** [Pro] — Detect and highlight edges with adjustable width and roundness.
- **Mirror node** — Mirror texture horizontally and/or vertically.
- **Slope Blur node** [Pro] — Blur directed by a slope/angle map.
- **Flood Fill nodes** [Pro] — Flood Fill, Flood Fill to Random Grayscale, Flood Fill to Gradient.
- **Directional Blur node** [Pro] — Blur along a direction.
- **Radial Blur node** [Pro] — Blur radiating from a centre point.
- **Median node** [Pro] — Median filter for noise reduction.
- **Curvature node** [Pro] — Extract surface curvature from height.
- **Quad Transform node** [Pro] — Four-corner perspective warp.
- **Trapezoid Transform node** [Pro] — Perspective trapezoid transformation.
- **Quick Tile node** [Pro] — One-step tiling with seam blending.
- **Coordinates Transform node** [Pro] — Low-level UV coordinate remapping.
- **Palette Extract / Palettize nodes** [Pro] — Extract and quantise colour palettes.
- **Histogram Range / Scan / Select nodes** [Pro] — Histogram-based level operations.
- **Fractal Noise node** [Pro] — Multi-octave fractal noise generator.
- **Gradient (Dynamic) node** [Pro] — Programmable multi-stop gradient generator.
- **Value / Bool / Int / Enum / Vec2 nodes** [Pro] — Constant value provider nodes.
- **Dot node** [Pro] — Wire organiser node.
- **Frame / Comment nodes** [Pro] — Visual grouping and annotation nodes.
- **Text node** — Render text as a texture with custom font, size, and colour.
- **Voronoi node** — Voronoi cell pattern generator.
- **Curves node** — Tone curve adjustment with draggable control points.
- **Threshold node** — Binary split at a configurable value.
- **Warp node** — Distort a texture using a separate warp map.
- **Kaleidoscope node** — Kaleidoscope symmetry effect.
- **Skew node** — Skew transformation.
- **Switch / Multi Switch nodes** — Select between multiple inputs.
- **Combine / Separate RGBA and Alpha nodes** — Channel splitting and merging.
- **Height Blend / Average Blend nodes** [Pro] — Height-aware and simple average blending.
- **Copy/paste nodes and subgraphs** — Copy, paste, and duplicate selections within the editor.
- **Node minimise** — Collapse a node to hide its body and save canvas space.
- **Image upload node** — Use any image file as a texture source.

### Improvements

- Node library organised into collapsible categories with search.
- Transform node: offset uses normalised 0–1 range; tiling works as repetition count; scale property added.
- Perlin noise improved for seamless tiling.
- Blur: Gaussian and box blur fixed; only executes when radius > 0; wraps edges correctly; does not affect alpha channel.
- Graph zoom limits expanded for large graphs.
- Node sliders and input controls improved for tablet/touch.
- Curves node: scrollable control points, persistent scrollbar, touch support.
- Only connected output buffers are allocated (performance).

### Bug Fixes

- Fixed blend node mask not applying correctly.
- Fixed highpass node outputting incorrect data.
- Fixed blur node alpha channel mutation.
- Fixed colour channel separation producing incorrect output.

---

## Foundation — December 2025

### New Features

- Initial node-based texture editor — React + Vite frontend, node graph editor via React Flow, Canvas 2D texture generation engine.
- Core nodes: Shape, Checker, Gradient, Solid Color, Perlin Noise, Blend, Transform.
- Project save/load via PostgreSQL-backed API.
- Node library panel with categories.
- Real-time preview for selected node and graph output.
- Color picker component.
- Reset functionality on all nodes.
- Multiple blend modes.

---

_Updated: 2026-08-27. Version: v1.5.0._
_See `docs/releases/workflow.md` for how to maintain this file._
