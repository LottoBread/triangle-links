# Triangle Links changelog

Newest first. This history starts with the Triangle Range prototype in s&box and follows the Unreal port through the supplied Mixamo animation update. Controls and test results belong to the revision where they were reported. Section dates use Pacific time. Archive links open local build files where available.

## Unreal Engine playtests

### 2026-11-25 — Mixamo golf and locomotion clips

- Replaced the interim walk and run cycles with the supplied Mixamo clips, retargeted in place to the golfer's rig.
- Added distinct drive, wedge chip, and putt poses. The trace controls the backswing, contact pose, and follow-through. Releasing a putt plays a brief downswing before the ball launches at contact.
- Replicated the selected club and stroke phase so observers see the corresponding animation. All players should use the same build.

### 2026-11-25 — Golfer locomotion

- Retargeted Mixamo walk and sprint motion to the golfer's existing skeleton. Reworked the arm swing and adjusted foot height for the golfer's proportions.
- Blended idle, walk, and sprint by movement speed, with a shared stride phase. Address and cart poses now blend with locomotion. The stroke trace still controls the swing pose directly.

### 2026-11-25 — Wind, ultrawide, and menu redesign

- Removed fixed-aspect framing from the menu and address cameras. Moved the stroke panel to the boundary between the center and right thirds, tightened the horizontal margins, and centered its text.
- Anchored the loft and aim guide to the ball in the 3D scene. The trace reads from the visible drawing surface, including with display scaling.
- First Light now has slow wind shifts and occasional gusts that affect airborne shots. Added a windsock at each tee and a wind readout below the minimap. The Moon has no wind.
- **Play solo** opens the same course picker used by multiplayer hosts. Added redesigned game menus and a tabbed customization screen with direct swatch selection and a live equipment preview.

[Windows Wind & Ultrawide Playtest ZIP](<E:/Unreal/Builds/TriangleLinks-Windows-Wind-Playtest-2026-11-25.zip>)


### 2026-11-25 — The Moon

- Added a second nine-hole course from Tranquility Base to Earthrise. Crater bowls and raised rims change how shots land and roll. The minimap outlines the craters, and illuminated markers identify tees and cups.
- The Moon uses 1.62 m/s² gravity and vacuum ball flight. Full-swing launch speeds are tuned for the lunar course. Jumps, carts, and impact dust also use the lower gravity.
- Added a star field with Earth above the horizon, regolith and scattered rocks, and hard sunlight with cool fill. A UFO crosses the course periodically.
- Choose **Play The Moon** in the main menu or select **The Moon** as the multiplayer lobby host.

[Windows Moon Playtest ZIP](<E:/Unreal/Builds/TriangleLinks-Windows-Moon-Playtest-2026-11-25.zip>)


### 2026-11-25 — Trophy Hall, menu showcase, and controls

- Added six locally saved achievements with a trophy for each in the Trophy Hall. The main menu shows a close-up of the golfer, cart, club, and ball with their equipped finishes. Earned trophies drop and tumble behind the golfer when the menu loads.
- The cinematic camera targets the rendered ball. At address, the golfer is framed on the left, the lightly blurred swing guide sits on the right, and the minimap stays in the upper right.
- Iron divots and wedge pitch marks lower the rendered turf and expose brown dirt. Walking and cart collision stay smooth. Grass sprays forward at about 60°, reaching knee height on a soft swing and about 1.25× golfer height on a hard swing.
- Added minimap zoom on `[` and `]` and a keybinding editor under **Escape → Settings**. Made HUD text bolder and switched the hole-out callout to scalable text.
- Verified the archive and rendered the packaged menu with all six trophies loaded. Full-round and live Steam multiplayer testing remained open.

[Windows Trophy Playtest ZIP](<E:/Unreal/Builds/TriangleLinks-Windows-Trophy-Playtest-2026-11-25.zip>)

### 2026-11-24 — Loft, tee order, and cinematic cameras

- At address, **W/S** shifts the ball in the stance to change loft. The launch arrow and readout reflect loft and terrain slope. Club memory persists between shots, with automatic putter selection on the green.
- Added iron divot stripes, green pitch marks for steep wedge landings, and grass spray on non-tee strikes. Added selectable tracer colors, fire, and rainbow.
- The host chooses stroke or match play. Lowest cumulative strokes tee first in stroke play, and the previous hole winner tees first in match play. Ties keep the existing order. The scorecard highlights each hole’s low score and the overall lead separately. Hole-out results appear for three seconds.
- Hold **C** to spectate another player’s ball and press **T** to switch your own shots between chase and a low, long-lens green camera. The ball marker reaches 100 m, points from the screen edge when needed, and disappears within 5 m.
- The package launched. Tee order, loft, and wedge impact were tested. Camera framing and effects still needed a visual multiplayer test.

[Windows Loft Playtest ZIP](<E:/Unreal/Builds/TriangleLinks-Windows-Loft-Playtest-2026-11-25.zip>)

### 2026-11-24 — Clubhouse, cosmetics, and audio

- Added ball color, separate club grip, shaft, and head finishes, plus cart paint options including pearlescent, chrome, and gold. The menu saves selections. Outfit, accessory, and other cart-part controls were placeholders.
- Imported driver, iron, wedge, and cup sounds, ambient birds, and chase-camera wind that responds to ball speed. Raised the cigarette and added a rising smoke trail and separate exhale cloud.
- Increased club power proportionally. A clean full-power driver reached 220 m in testing. Remembered the last club selection between swings.
- Slow putts drop into the cup under gravity. Faster balls can rebound against its wall or skip off the lip. The ball marker showed between 5 and 24 m, and the tracer ended at the rendered ball. Added jumping with **Space** on foot.
- Verified packaged launch, shot distances, and cup behavior. Added future course concepts for the Moon and an asteroid belt.

[Windows Clubhouse Playtest ZIP](<E:/Unreal/Builds/TriangleLinks-Windows-Clubhouse-Playtest-2026-11-24.zip>) · [Future course notes](<E:/Unreal/TriangleLinks/Future Courses.md>)

### 2026-11-24 — Lobby screen, scorecard, and course interactions

- Added a scenic main menu, separate Steam lobby screen with player list and invites, and a course picker. The host starts the round. First Light was the available course.
- **Tab** opens a horizontal multiplayer scorecard with Steam names and avatars. Nearby players have small name tags.
- Corrected remote aim and cart poses and smoothed the ball chase camera.
- Added air drag and slope-adjusted launch angles. Cup lip behavior lets fast putts pop out. Tree canopies and bushes slow the ball as it passes through them, and trunks block players and carts.
- Local two-client tests passed lobby transition, remote aim posing, and trunk collision. Steam invites were wired up, with two-account invite acceptance still open.

[Windows Lobby Playtest ZIP](<E:/Unreal/Builds/TriangleLinks-Windows-Lobby-Playtest-2026-11-24.zip>)

### 2026-11-24 — Multiplayer synchronization, carts, and consumables

- Fixed remote movement and turn/address synchronization. A two-client test confirmed both players could tee off in turn and the guest could see the host’s swing and tracer.
- Each player gets a cart with a passenger seat and tighter suspension. **E** boards or exits, **B** applies the parking brake, **Space** handbrakes, and **V** flips a tipped cart. The map shows carts and every player’s ball.
- Tree trunks deflect the ball. Shallow bounces lose more speed. One test shot traveled about 21 m after its first fairway bounce and 11 m in rough.
- **G** drinks and **H** smokes. Smoking is cosmetic. Drinking progressively affects the view, swings, putts, and steering.
- The package passed a local multiplayer join test. This revision still needed a two-machine Steam test.

[Windows Multiplayer Playtest ZIP](<E:/Unreal/Builds/TriangleLinks-Windows-Multiplayer-Playtest-2026-11-24.zip>)

### 2026-11-24 — Steam lobby integration

- Added Steam networking and lobby discovery for up to four players with the Spacewar test app ID `480`. Steam lobby joins use the in-game list.
- The host successfully advertised a First Light lobby. A subsequent player report confirmed the Steam lobby worked with a friend, and identified the multiplayer issues addressed by the next patch.

[Windows Steam Playtest ZIP](<E:/Unreal/Builds/TriangleLinks-Windows-Steam-Playtest-2026-11-24.zip>)

### 2026-11-24 — Cart and ball physics

- Corrected horizontal mouse look and turned the wheel axles inward. Carts coast off throttle, lean with the terrain, and can roll over.
- Increased tall grass density in the rough by about 73%.
- Made bounce depend on surface and impact angle, and let the ball lift off hill crests. Increased green resistance and differentiated fairway and rough. At the same test speed the ball rolled 24 m on the fairway and 12 m in rough.
- Verified the Windows package launched into First Light.

[Windows Physics Playtest ZIP](<E:/Unreal/Builds/TriangleLinks-Windows-Physics-Playtest-2026-11-24.zip>)

### 2026-11-24 — First standalone Windows playtest

- Packaged the game with the required Visual C++ runtime. Players could extract the ZIP and run `TriangleLinks.exe`.
- Verified the main menu, First Light with the new foliage and materials, and a registered putt.

[First Windows Playtest ZIP](<E:/Unreal/Builds/TriangleLinks-Windows-Playtest-2026-11-24.zip>)

### 2026-11-24 — Foliage and material pass

- Added dense pines and broadleaf trees around the course, with bushes and wind-animated tall grass in the rough. Planting adapts to each hole and leaves tees and greens clear.
- Added mowing stripes, blade texture, and turf relief. Updated bark, foliage, golfer, cart, flag, ball, and club materials.
- Played through to West Bend to check foliage updates and grounding.

[Editable foliage models](<E:/Unreal/TriangleLinks/Art/TriangleLinksFoliage.blend>)

### 2026-11-24 — Playable loop, menu, and direct IP multiplayer

- Adjusted mouse look and corrected cart driving direction, steering, and seating.
- Moved the swing guide to the right and stripped back the panel. Added a minimap aim guide, revised daylight and haze, and introduced a cool-white tapered ball trail.
- Fixed second-hole collision and verified the golfer stayed grounded after advancing to West Bend.
- Added a menu and direct IP hosting for up to four players. Local two-player tests verified joining, turn order, and shot replication. Cart driving was solo-only in this revision.

### 2026-11-23 — Unreal port and First Light preview

- Created a separate Unreal 5.9 project. The C++ port covered nine hole layouts, terrain, grass, tracing, club loft, flight, bounce, putting, and cup capture. The standalone simulation passed checks for nine cup drops, swing speed, loft, and out-of-bounds handling.
- Imported the textured golfer and skeleton and cart with four separate wheels. The First Light preview had sloped terrain, four grass zones, and tee and pin collision. Play subsequently possessed the textured, animated golfer.
- The editor preview and native gameplay were brought up in stages while the Windows C++ toolchain was being set up.

[Unreal project](<E:/Unreal/TriangleLinks/TriangleLinks.uproject>)

## s&box prototype

### 2026-11-23 — Bounce, putting break, and consumables

- Green and fairway can produce multiple shallow skips. Steep green landings lose most of their speed. Rough and deep rough cushion bounces without the old sudden speed cut.
- Putts start closer to their aimed line, with the slope’s effect building during rollout.
- **B** drank and **N** toggled a cosmetic cigar. Intoxication wore off over time and affected camera sway, swing input, putts, and cart steering. Drink and cigar state were included in multiplayer snapshots.
- In simulation, a shallow green shot bounced three times, and a steep green landing slowed to about 0.2 m/s. A second-player consumables test remained open.

### 2026-11-23 — Ball height on grass

- Aligned the rendered ball and its trail to the grass surface between terrain vertices, including other players’ balls.
- Checked resting height across four grass types, normal airborne height, and descent into the cup.

### 2026-11-23 — Cart seating and grass edges

- Moved the golfer to the steering-wheel side. Smoothed grass boundaries and added subtle visual thickness and exposed cut edges between layers. Rolling physics were unchanged in this pass.

### 2026-11-23 — Imported cart

- Integrated the supplied cart, separated all four wheels, and connected wheel rotation and steering. Adjusted the driver position for the new body. A simulated drive confirmed movement and wheel animation.

### 2026-11-23 — Golfer animation pass

- Lowered the hands at idle, evened out arm motion while walking, and reduced torso bend and twist at address and during the swing. Idle and address were checked in game.

### 2026-11-22 — Imported golfer

- Integrated the corrected textured golfer, connected her skeleton to the procedural animation, and adjusted orientation and address pose. Verified she rendered and posed on the course.
- The imported clothing, hair, and cap were part of a single mesh in this revision, so those parts could not be swapped individually.

### 2026-11-22 — Golfer and cart art development

- Introduced an editable cartoon golfer with a continuous skinned body, UVs, and a 24-bone rig. Revisions rounded the head, simplified the face, and added finger geometry.
- Built separate skinned body, polo, shorts, shoes, glove, and cap pieces for the prototype golfer. Verified cap removal and re-equipping in s&box. This was a separate asset from the later imported golfer.
- Explored a fresh character concept and two Blender drafts. Those drafts remained development work. Tested the supplied golfer’s rig, found problems in the first exports, and integrated the corrected export in the later import patch. Cart concept art went through several style passes before the supplied cart was integrated.

### 2026-11-22 — s&box friends playtest

- Added **Play Solo**, **Host Steam Friends Lobby**, and **Join Friends** for up to four players. **Tab** opened the shared nine-hole scorecard.
- Added toon-shaded pines and broadleaf trees, dense boundary woods, and tall grass. Putts got a close follow camera.
- Address preserved the direction you were already looking. **A/D** ramped from fine adjustments to 30° per second. The cart accelerated harder and reached about 122 km/h on the fairway in testing.
- A second local client verified the lobby and scorecard. The ZIP runs in the s&box editor.

[s&box dev playtest ZIP](<C:/Users/strin/Documents/S&box Projects/golf_tech_demo/Exports/Triangle Links - sbox dev playtest.zip>)

### 2026-11-22 — Cart movement and shot follow fixes

- Fixed forward and reverse movement from a stop, including at high frame rates. Restored camera follow through flight and rollout and prevented leftover trace input from canceling it.

### 2026-11-22 — Third-person controls and handbrake slide

- Added **E** as the shared interact key for ball and cart, with in-world prompts. Mouse look worked on foot and in the cart, and the wheel controlled zoom.
- Kept third person as the active view and made walking follow the camera heading. Corrected wheel spin and visual steering. **Space** while turning at speed could initiate a slide.

### 2026-11-22 — Driveable cart, toon models, and recessed cup

- Introduced a cartoon golfer and matching driveable cart with animated wheels. Added grass clippings at impact and a fading gold flight trail.
- Scaled the ball down to about 10.5 cm in this revision. Well-paced putts could roll over the lip and drop into the recessed cup, while fast putts could cross it.

### 2026-11-22 — Playable rough and four-player golf

- Differentiated fairway, playable rough, and deep boundary rough. White stakes marked out-of-bounds, with a one-stroke penalty and return to the previous lie.
- Added up-to-four-player friends lobbies. Everyone tees off once, then the furthest ball from the pin plays. Tested with a host and a second local client.
- Added a more articulated golfer, a visible remote swing, and attachment points for headwear, eyewear, mouth, torso, hands, and club.

### 2026-11-22 — Larger swing panel

- About doubled the drawing width and moved the panel to center-left, keeping the golfer and club visible on the right in shoulder view.

### 2026-11-22 — Full-screen HUD and trace-driven animation

- Switched to a full-screen course view with distance, lie, score, and a minimap. Swing and putt panels opened only at address.
- Bound the backswing and downswing to the player’s trace. Valid shots launched on impact. The shoulder camera chased the ball through flight and rollout.
- Gave clubs distinct launch angles, including 12° for the driver and 53° for the wedge in this revision.

### 2026-11-22 — Sloped terrain and surface-dependent roll

- Added bird’s-eye, over-the-shoulder, and overhead cameras, a golfer holding an animated club, and a separate short putting stroke.
- Added hills, sloped greens, mowing stripes, and surface-dependent roll. The green rolled fastest and rough slowed the ball most. Soft putts gained usable distance and drives could bounce and roll after landing.

### 2026-11-22 — 3D course and a separate putting meter

- Moved the nine-hole course into a 3D overhead view and added zoom. Full shots kept the triangle trace with visible flight and landing.
- Putting used a separate hold-and-release **Space** meter, with a distance marker for the cup. Tested putts that stopped short, dropped in, and rolled past.

### 2026-11-22 — Club cycling

- Added **Q/F** cycling through Driver, 3 Wood, 5 Iron, 9 Iron, Wedge, and Putter at address. The HUD showed club and estimated distance. The automatic short-range putter could be overridden.

### 2026-11-22 — Nine-hole Triangle Links course

- Added walking, sprinting, ball address, manual aim offsets, and an aim-at-pin reset. Hole advancement carried the score forward.
- Verified a drive, a putt, and the move to the second tee in the original overhead view.

### 2026-11-22 — Trace speed affects ball speed

- Measured the apex-to-impact downswing to determine ball speed, with a penalty for off-center contact. Added ball speed to the shot readout.
- Three centered test strokes with 0.6 s, 0.2 s, and 0.1 s downswings produced 22, 47, and 70 m/s respectively.

### 2026-11-22 — Triangle Range installation

- Installed the supplied Triangle Range demo into the Golf Tech Demo s&box project and preserved the existing project file. Verified that the swing and ball-flight panels rendered in Play mode.

