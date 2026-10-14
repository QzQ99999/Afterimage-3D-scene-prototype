# Frozen V1 snapshot

The user froze this version as **Afterimage 3D scene prototype V1** on 2026-10-14.

- Do not edit, replace, regenerate, rename, delete, or update `Afterimage 3D scene prototype V1.html` without the user's explicit confirmation of the specific change.
- Requests to inspect, run, preview, copy, back up, or upload this version do not authorize content changes.
- Preserve the HTML bytes and verify them against `SHA256SUMS.txt` before copying or uploading.
- Do not remove the local read-only attribute or change the checksum manifest or these instructions to bypass the freeze.
- The original `Afterimage 3D scene prototype.html` is also frozen and must not be modified without the user's explicit confirmation.
- Keep this policy in force until the user explicitly approves a change.

## Reconfirmed frozen publication snapshot — 2026-10-14

The user explicitly requested saving and freezing the current version locally, prohibiting updates or changes to the source without their confirmation, and uploading this exact version to the existing GitHub repository and GitHub Pages. This authorization covers publishing the existing bytes only. Do not make source changes, silently update this frozen version, or publish a future revision without the user's explicit authorization for that action.

The frozen HTML SHA256 is `37f949f4210a5aa9194822c147845921e8b2c6576cdf140a3adcc65eae43535e` (85,325 bytes), including the red controllable sphere, follow camera and Sun Disc Size slider. The local source remains read-only and matches `SHA256SUMS.txt`. A byte-identical local snapshot, instructions and manifest are preserved in `backups/frozen-current-20261014-223938/`. The publication copies are the V1 HTML path and `docs/index.html`; preserve the original frozen V0 root HTML files.

## Current authorized sun disc size revision — 2026-10-14

The user explicitly requested a slider in the Sun group controlling the visible sun disc size. The Sun group now includes Disc Size (`sun-disc-size`), range 10–500%, step 1%, default 100% (the original disc profile), numeric output and individual Reset. The existing Reset All and collapsible group behavior include this new slider, bringing the total to 18 sliders.

The slider uses the previously reserved lightColor.w uniform component to scale only the visible disc profile. Existing sun direction, halo, illumination, shadow softness, fog, sphere movement, camera and all other controls remain unchanged. The 80-float uniform layout and six render passes are retained. JavaScript syntax and all five WGSL modules/six pipeline entries passed compilation; the new control was verified in the browser accessibility tree.

The preceding HTML, instructions and checksum are backed up under `backups/before-sun-disc-size-20261014-222943-764/`. Current HTML SHA256: `37f949f4210a5aa9194822c147845921e8b2c6576cdf140a3adcc65eae43535e`. The manifest matches and the HTML is read-only. This local change has not been uploaded to GitHub. The freeze remains in force for future changes.

## Previous authorized player sphere revision — 2026-10-14

The user explicitly requested a red sphere in front of the cube face indicated by the screenshot, at a distance of four cube edges, with a diameter of one quarter of the cube edge, WASD movement, and a sphere-centered follow camera retaining free orbit/zoom and the original initial viewing angles.

The indicated face is +Z. Cube edge remains 1.82, sphere radius is 0.2275, and the ground-resting initial center is [0, 0.2275, 8.19], measuring four edges from the +Z face to the sphere center. Initial camera yaw 0.70, pitch 0.29, radius 10.8 and FOV remain unchanged; its pivot and eye follow the sphere. WASD uses camera-relative horizontal motion at 2.73 world units/second, equal diagonal speed, cube collision/sliding, and clears held keys on blur/tab hiding. Existing drag, touch orbit/pinch, wheel and arrow-key controls remain. The camera lifts over the cube if its orbit would enter the geometry.

The sphere participates in primary rays, cube reflections, sunlight/fog visibility and fog-scaled contact shadows. Motion-aware sphere reprojection and local lighting-history rejection avoid stale sphere/shadow/reflection history; stopping restarts the existing stationary 96-sample coverage accumulation. All 17 sliders, five groups, boundary control, six render passes and previous defaults are preserved. A short WASD/drag/scroll hint is shown.

The prior HTML, instructions and checksum are backed up in `backups/before-player-ball-20261014-215907-555/`. Current HTML SHA256 is `becde5b8d1880371587ac16dbc88e943e25aa3b2cc8813397b4c2b222640fd34`. The checksum manifest matches and the HTML is read-only. Native GPU shader/render checks, JS movement/camera/collision/scheduling and slider regressions, and browser WASD/orbit/zoom checks passed. Reports are in `verification/20261014-player/`. This revision is local; the previously published GitHub snapshot was not changed. All freeze rules remain in force for further changes.

## Previous authorized zoom stability and boundary revision — 2026-10-14

After reverting the previous broad fog stability repair, the user explicitly requested a targeted fix for image shimmer around the cube when zoomed out, plus a slider in Environment controlling the ground/sky boundary distance from the cube. The existing boundary must remain both the default and nearest position.

The current revision adds `Boundary Distance` (`environment-boundary`): minimum/default 55, maximum 275, step 1, with numeric output, individual Reset and Reset All support. It moves the cube-centered radial ground-to-sky transition outward using `smoothstep(distance-45, distance, radius)`, preserving its original width and exact default trace appearance. The Environment group now contains four sliders; all five groups and 17 sliders fully expand.

The targeted stability repair averages stationary subpixel coverage without rejecting samples that alternate between cube and ground, starts a clean accumulation once the camera stops, and fades the geometry-dependent spatial filter as stationary coverage converges. Motion reprojection retains geometry validation. Dynamic resolution adapts during interaction and stays fixed during static convergence; the page sleeps after 96 samples. The original fog integration, cloud-gap shaft pattern, density, reflection sampling, sand detail, six-pass pipeline, geometry and all previous control defaults are retained. The earlier deterministic fog raymarch repair was not restored.

The preceding HTML, instructions and checksum are backed up under `backups/before-zoom-boundary-20261014-212407-985/`. Current HTML SHA256: `bc545a2ea25206c024c6dff86fe0cb8871274013b109e78dee6924375895f054`. The manifest matches, and the HTML is read-only. Native GPU comparisons, JavaScript control/scheduling tests, zoomed-out browser rendering, boundary movement and Reset checks passed. Reports and screenshots are under `verification/20261014-zoom-boundary/`. Local previews are synchronized. All freeze rules and explicit authorization requirements for future changes and GitHub uploads remain in force.

## Previous authorized controls revision — 2026-10-14

The user explicitly requested this local V1 revision: fog-only saturation and brightness; removal of cloud-mask shadows from the ground; three Sun X/Y/Z sliders; Tyndall Shaft Size, Shaft Density and Shaft Opacity controls (zero opacity removes directional scattering while retaining ordinary fog); five fully expandable groups (Sun, Fog, Tyndall, Light and Environment); a global Collapse All / Expand All button above Reset All at the right; independent hue/brightness/saturation controls for direct light and sky; and object/contact shadows that weaken as fog density rises.

This revision is based on the restored GitHub V1 snapshot below. It retains the original irregular cloud-gap shaft profile at default size/density, with Size scaling the pattern and Density controlling gap coverage. Fog grading applies only to volume-scattered radiance, the sky has independent color uniforms, and cloud masks no longer modulate direct surface lighting. All 16 sliders retain numerical outputs and individual Reset buttons. Groups have natural content height; only the overall panel scrolls. The original cube, camera and six-stage render pipeline are preserved.

The previous HTML, instructions and checksum are saved byte-for-byte under `backups/before-requested-controls-20261014-203754-972/`. The revised HTML SHA256 is `b508f43e6c9b6870afbb315930c60d4d74744c6000e1e0873c038714773dc31f`; `SHA256SUMS.txt` matches and the HTML is read-only. Native GPU checks, JavaScript behavior checks and browser rendering/layout checks passed. This authorization covers the listed local changes only; the freeze and explicit authorization requirement for future changes or GitHub uploads remain in force.

## Previous saved snapshot — 2026-10-14

The user explicitly authorized replacing the entire local V1 HTML with `C:/Users/31202/AppData/Local/Temp/afterimage-github-shafts/github-v1.html`, the original GitHub V1 snapshot. This full-file replacement supersedes the local revisions described below. The current file is byte-identical to that source (SHA256 `43b7a7437ab8145f2e87da3b9e5de548beb92b676b269d0bc33128c70775f6d4`). The former local HTML, instructions and checksum were preserved under `backups/before-github-replacement-20261014-202550-085/`. Do not reapply earlier local features unless the user asks. The current HTML is read-only, the checksum manifest matches it, and the original non-V1 source and GitHub repository were not changed.

## Earlier approved local revisions — 2026-10-14

The user explicitly approved adding a red sphere in front of the cube, WASD movement, and a sphere-centered follow camera with free orbit and zoom. The subsequent approved adjustment enlarges that sphere 3x and the cube 2x and increases the initial spacing to match the supplied reference. These changes are saved in the local V1 HTML and reflected in `SHA256SUMS.txt`.

The user subsequently approved doubling the initial ball-to-cube spacing from 7.5 to 15 world units along the ground plane, preserving all object sizes and controls.

The user also approved changing the scene saturation and brightness sliders to affect fog only, and adding a Tyndall Effect slider for directional volumetric scattering. The user then clarified that this slider must control shaft size and spatial density instead of brightness, and requested removal of the large cloud-shadow bands on the ground. That revision used a combined shaft pattern frequency control; the pattern affects fog only, while direct surface lighting retains object shadows without the cloud mask.

The latest approved revision replaces the solar orbit slider with Sun X/Y/Z controls, separates Shaft Size and Shaft Density, and adds independent hue/brightness/saturation controls for Light and Environment (sky). All 15 sliders are arranged vertically within five native collapsible groups: Sun, Fog, Tyndall, Light, and Environment. Numerical values, individual Reset buttons, English labels, the Sun Disc toggle, and Reset All are retained. Shaft Size changes the radius of fixed candidate beams; Shaft Density changes how many candidates are enabled. Existing object sizes, initial spacing, movement, camera controls, and the six-stage render pipeline are preserved.

The user subsequently reported a browser WGSL compile error. The authorized repair adds explicit parentheses around the multiplied hash inputs before bitwise XOR, as required by the browser's WGSL parser; this does not change the intended calculations or controls.

The user requested fully expanded groups. Group bodies now use their natural content height without internal scroll areas; only the overall control panel scrolls when all expanded groups exceed the available viewport height. Native expand/collapse behavior is retained.

The user approved dynamic light shafts, a Shaft Opacity slider (0 hides all directional shaft scattering while retaining ordinary fog), attenuation along the light propagation path, weaker object/contact shadows as fog density increases, and removal of distant fog grain. This revision has 16 sliders. It uses continuous source-distance attenuation, stable near-dense volume integration, filtered distant shaft detail, and short animation history. Rendering continues while visible shafts animate, pauses when the page is hidden, and returns to static convergence when the effect is hidden. The six rendering passes and the existing dynamic-resolution budget are retained.

The user clarified that dynamic shafts must stay in place rather than drift. Each candidate shaft now has its own random phase and period, with newly randomized fade-in, hold, and fade-out durations each cycle. Distant unresolved shafts use their mean lifecycle coverage to preserve the fog noise fix. A Collapse All / Expand All button sits above Reset All at the right; it controls all five groups, follows individual group changes, and preserves slider values. These explicitly authorized local changes replace the earlier drifting pattern.

The user then explicitly requested restoring the shafts from two revisions earlier while retaining Shaft Opacity and everything else. The current shafts are fixed and continuously present again: both drift and random lifecycles are removed, the original candidate coverage is restored, and static convergence no longer schedules continuous animation. Shaft Opacity, the five groups and global expand/collapse button, distance attenuation, fog-dependent shadows, distant noise filtering, and the six-pass rendering pipeline remain intact.

The user subsequently requested the shafts from the actual GitHub online version, keeping everything else. The source was read from QzQ99999/Afterimage-3D-scene-prototype, main commit 7bbeaa43aa609e0d4fc47f07ee1098ad3d9fb62c, V1 HTML blob 149bdea7b6ead9a6b296fb4f0be3b0aedd6bee1a. The current shader restores that version's irregular cloud-gap projection and noise thresholds at default size/density, replacing the local candidate grid. Existing size and density controls adjust cloud-pattern scale and gap coverage; their tooltips reflect this. Opacity and distant filtering are retained. All other scene, surface lighting, fog, camera, UI and rendering code remains unchanged. This was a local revision only, not a GitHub write.

The user instructed that this revision must not be uploaded to GitHub yet. A later upload requires explicit authorization. All freeze rules above remain in force for further changes.
