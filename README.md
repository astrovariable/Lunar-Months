# The Four Lunar Months

An interactive animation that explains why the Moon has four different "month" lengths, even though there is only one Moon going around one orbit.

The answer depends on **what you measure one complete orbit against**:

| Month | Measured against | Mean length |
|---|---|---|
| **Draconic** | the Moon's nodes (where its orbit crosses Earth's orbital plane) | 27.212 days |
| **Sidereal** | the distant stars | 27.322 days |
| **Anomalistic** | the perigee (the Moon's closest point to Earth) | 27.555 days |
| **Synodic** | the Sun (New Moon to New Moon) | 29.531 days |

The tool is a single HTML file. There is nothing to install and no build step. Everything runs in the browser.

**Live version:** `https://<your-username>.github.io/<repo-name>/` *(replace with the real link)*

---

## Contents

- [What the tool shows](#what-the-tool-shows)
- [Terms used in this tool](#terms-used-in-this-tool)
- [How to use it](#how-to-use-it)
- [Things to try](#things-to-try)
- [Using it in a class or talk](#using-it-in-a-class-or-talk)
- [Running it on your computer](#running-it-on-your-computer)
- [Putting it on GitHub Pages](#putting-it-on-github-pages)
- [How the animation works](#how-the-animation-works)
- [Accuracy and limitations](#accuracy-and-limitations)
- [Files in this repository](#files-in-this-repository)
- [Credits](#credits)
- [Licence](#licence)

---

## What the tool shows

The page has three tabs. Each one runs an animation over 66 days (a little more than two months) and then starts again.

### Tab 1 – Synodic vs Sidereal

A top-down view of the Sun, Earth's orbit, and the Moon's orbit around Earth.

- A **gold line** through Earth always points in the same direction in space, towards a distant star. When the Moon comes back to this line, one **sidereal month** (27.32 days) is complete.
- An **orange line** always points from Earth to the Sun. Because Earth moves about 27° along its own orbit during one sidereal month, this line turns. The Moon needs about two more days to catch up with it. When it does, it is New Moon again, and one **synodic month** (29.53 days) is complete.
- The Moon is drawn with its sunlit half facing the Sun.
- A gold ring flashes on the gold line at each sidereal completion. An orange ring flashes on the orange line at each synodic completion.
- A counter at the top shows how many sidereal and synodic months have passed.

### Tab 2 – Anomalistic

A view of the Moon's elliptical orbit, with Earth at one focus.

- The **perigee** (red, closest point) and **apogee** (blue, farthest point) are marked.
- The long axis of the ellipse slowly turns in the same direction the Moon moves. This is called **apsidal precession**. Because the perigee keeps moving ahead, the Moon takes longer than a sidereal month to get back to it: 27.55 days. This is the **anomalistic month**.
- The Moon's speed changes along the orbit: faster near perigee, slower near apogee. This follows Kepler's second law.
- A grey trail shows where the Moon was during the last 10 days.
- A red ring flashes at each perigee return. Each new ring appears slightly further round than the last; that shift is the precession.

### Tab 3 – Draconic

A tilted 3D view of the Moon's orbit and the ecliptic plane (the plane of Earth's orbit around the Sun, drawn as a green disc).

- The Moon's orbit is tilted to this plane, so it crosses it at two points called **nodes**: the **ascending node** (☊, green), where the Moon goes from below the plane to above it, and the **descending node** (☋, orange).
- The line joining the nodes slowly turns *opposite* to the Moon's motion. This is called **nodal regression**. Because the node comes back to meet the Moon, the Moon reaches it sooner than a sidereal month: 27.21 days. This is the **draconic month**.
- A dashed line drops from the Moon to the plane, and a label says whether the Moon is above or below the plane.
- The part of the orbit behind the plane is drawn fainter, so the 3D shape is easier to see.
- A green ring flashes at each return to the ascending node.

### Below each animation

- **Event chips** on the canvas list each completion (for example, "synodic ×1 (New Moon) — 29.53 d") for a few days after it happens.
- An **explanation panel** describes what the current tab is showing.
- The **footer** lists the four month lengths in order and the Saros relation.

---

## Terms used in this tool

| Term | Meaning |
|---|---|
| **Orbit** | The path of one body around another. |
| **Sidereal month** | Time for the Moon to go once around Earth relative to the distant stars. |
| **Synodic month** | Time from one New Moon to the next (or Full Moon to Full Moon). This is the month of the Moon's phases, and the one most calendars use. |
| **Anomalistic month** | Time for the Moon to go from perigee back to perigee. |
| **Draconic month** | Time for the Moon to go from one node back to the same node. Also called the nodical month. The name comes from an old idea of a dragon swallowing the Sun or Moon during eclipses. |
| **Tropical month** | Time for the Moon to return to the same position measured from the March equinox point. It is only about 7 seconds shorter than the sidereal month. |
| **New Moon** | The phase when the Moon lies between Earth and the Sun, so its sunlit side faces away from us. |
| **Ellipse** | A stretched circle. The Moon's orbit is an ellipse, with Earth at one of two special inner points called foci (singular: focus). |
| **Eccentricity (e)** | A number that tells how stretched an ellipse is. 0 is a perfect circle; values closer to 1 are more stretched. The Moon's orbit has e ≈ 0.055. |
| **Perigee** | The point in the Moon's orbit closest to Earth. |
| **Apogee** | The point in the Moon's orbit farthest from Earth. |
| **Line of apsides** | The line joining perigee and apogee (the long axis of the ellipse). |
| **Precession** | A slow turning of an orbit's orientation, or of a spinning body's axis, over time. |
| **Prograde** | In the same direction as the Moon's motion. |
| **Retrograde** | In the opposite direction to the Moon's motion. |
| **Ecliptic** | The plane of Earth's orbit around the Sun. Seen from Earth, it is the path the Sun appears to follow across the sky over a year. |
| **Inclination (i)** | The tilt of the Moon's orbit relative to the ecliptic, about 5.15°. |
| **Node** | One of the two points where the Moon's orbit crosses the ecliptic. |
| **Nodal regression** | The slow backward turning of the line of nodes, one full turn in about 18.6 years. |
| **Kepler's equation** | The equation that tells where a body is along an elliptical orbit at a given time. |
| **Saros** | A cycle of about 18 years 11 days after which a very similar eclipse happens again. It exists because 223 synodic, 242 draconic and 239 anomalistic months are all very nearly the same length of time. |
| **Supermoon** | Popular name for a Full Moon that happens near perigee, so the Moon looks slightly larger and brighter. |

---

## How to use it

1. Open `index.html` in a web browser. The first tab, **Synodic vs Sidereal**, starts playing.
2. **Choose a tab** at the top: *Synodic vs Sidereal*, *Anomalistic*, or *Draconic*.
3. **Play or pause** with the **Pause / Play** button, or press the **Space** bar.
4. **Move through time** by dragging the **Time** slider (0 to 66 days). The readout at the top right of the canvas shows the current day. You can also press the **←** and **→** arrow keys to step back or forward by one day.
5. **Change the speed** with the **Speed** slider, from 0.5 to 20 days per second. The default is 6 days per second.
6. **Change the geometry** (only in the *Anomalistic* and *Draconic* tabs) with the **Geometry** slider:
   - At the right end ("teaching", the default), the shape and the precession are exaggerated so they are easy to see.
   - At the left end ("real"), they use the Moon's true values.
   - The text under the slider shows the current eccentricity or inclination and the precession period, next to the real values.
7. **Watch for the rings and chips.** Each time a month completes, a ring flashes at the point where it completed and a chip appears on the canvas with the month count and the elapsed days.
8. **Read the explanation panel** below the controls for a short description of the current tab.

Note: the Space bar works only when no slider or button is selected. If it doesn't respond, click on an empty part of the page first.

---

## Things to try

- **The two-day gap.** In *Synodic vs Sidereal*, pause just after the gold ring appears at 27.32 days. See how far the Moon still is from the orange Sun line. Then play until the orange ring appears at 29.53 days.
- **The gap grows.** Let it run to the second completions: sidereal at 54.64 days and synodic at 59.06 days. The gap is now about 4.4 days.
- **Why this month is hard to notice.** In *Anomalistic*, slowly drag **Geometry** from "teaching" to "real". The ellipse becomes almost a circle and the perigee almost stops moving. The effect is real but small.
- **Perigee running ahead.** In *Anomalistic* (teaching geometry), pause at each red ring and note where the perigee is. Each ring is further round than the one before.
- **Node coming back to meet the Moon.** In *Draconic*, watch the ascending node move backwards between the green rings. Compare its first return (27.21 days) with the sidereal month (27.32 days).
- **Order of the months.** Using the chips, write down the day of the first completion in each tab and sort them. You should get draconic < sidereal < anomalistic < synodic.

---

## Using it in a class or talk

A suggested order for a 15–20 minute session:

1. **Start with the question.** Ask the audience: "How long does the Moon take to go around Earth?" Collect answers. Most people will say about 28, 29 or 30 days.
2. **Show Synodic vs Sidereal.** Pause at day 27.32 and ask why the Moon is not at New Moon yet. Let them work out that Earth has moved along its orbit. Play to day 29.53.
3. **Connect to phases and calendars.** Explain that the synodic month is the one we see as phases, and the one used by lunar calendars (such as the Hindu and Islamic calendars).
4. **Move to Anomalistic.** Start at "teaching" geometry. Show the perigee moving ahead, then slide to "real" to show how small the real effect is. Mention supermoons.
5. **Move to Draconic.** Explain nodes with the drop line (above or below the plane). Show the node moving backward. Explain that eclipses need a New or Full Moon near a node.
6. **Finish with the Saros.** Point to the footer: 223 synodic ≈ 242 draconic ≈ 239 anomalistic months. This is why eclipses repeat in cycles of about 18 years.

For a projector, set the browser to full screen (`F11` on most desktop browsers) and lower the speed to 2–3 days per second so the audience can follow.




## How the animation works

Time `d` is measured in days from the start of the animation. All month lengths are mean values:

```
sidereal month     = 27.321661 d
synodic month      = 29.530589 d
anomalistic month  = 27.554550 d
draconic month     = 27.212221 d
tropical month     = 27.321582 d   (quoted in the text, not animated)
sidereal year      = 365.256363 d
```

### Synodic vs Sidereal

1. Earth's angle around the Sun:
   ```
   Earth angle = 360° × d / sidereal year
   ```
2. The Moon's angle around Earth, measured against the fixed star direction, starting at New Moon (Moon between Earth and Sun):
   ```
   Moon angle = 180° + 360° × d / sidereal month
   ```
3. The **star line** keeps the same direction in space. The Moon returns to it every sidereal month.
4. The **Sun line** points from Earth to the Sun, so it turns at Earth's orbital rate. The Moon catches it again when it has gained one full turn on Earth, which gives:
   ```
   1 / synodic = 1 / sidereal − 1 / year
   ```
   Putting in the numbers gives 29.53 days. The animation does not force this value; it comes out of the two motions.

### Anomalistic

1. The ellipse has Earth at one focus. Its long axis turns forward (prograde) with period `P_aps`, so the perigee direction is:
   ```
   ω = 360° × d / P_aps
   ```
2. The **mean anomaly** `M` (the Moon's angle from perigee if it moved at constant speed) increases by one full turn every anomalistic month:
   ```
   M = 360° × d / anomalistic month
   ```
3. **Kepler's equation** is solved for the **eccentric anomaly** `E` (a helper angle), using 10 steps of Newton's method:
   ```
   M = E − e sin E
   ```
4. Distance from Earth and the **true anomaly** `ν` (the Moon's real angle from perigee):
   ```
   r = a (1 − e cos E)
   ν = 2 atan2( √(1+e) sin(E/2), √(1−e) cos(E/2) )
   ```
   where `a` is the size of the orbit on screen.
5. The Moon is drawn at angle `ν + ω` and distance `r` from Earth.

### Draconic

1. The Moon moves around a circle of radius `R`, tilted by inclination `i`. Its angle from the ascending node, the **argument of latitude** `u`, increases by one turn every draconic month:
   ```
   u = 360° × d / draconic month
   ```
2. The node line turns backward (retrograde) with period `P_node`:
   ```
   Ω = −360° × d / P_node
   ```
3. Position in 3D (the ecliptic is the x–y plane, z is height above it):
   ```
   x0 = R cos u
   y0 = R sin u cos i
   z  = R sin u sin i
   x  = x0 cos Ω − y0 sin Ω
   y  = x0 sin Ω + y0 cos Ω
   ```
4. The 3D scene is drawn on screen as if seen from 33° above the ecliptic plane. Orbit points below the plane (`z < 0`) are drawn first and fainter, then the plane, then the points above it.

### Geometry slider

The slider mixes between the real and teaching values:

| Quantity | Real | Teaching |
|---|---|---|
| Eccentricity | 0.0549 | 0.30 |
| Apsidal precession period | 3232.6 d (8.85 yr), prograde | 240 d |
| Inclination | 5.145° | 15° |
| Nodal regression period | 6798.4 d (18.6 yr), retrograde | 300 d |

Eccentricity and inclination are mixed directly. For the two periods, the slider mixes their *rates* (1 ÷ period) instead, so the motion changes smoothly as you drag.

### Rings and chips

- A completion ring is drawn for 3.2 days after each event, as an expanding ring that pulses twice and fades out.
- A chip is shown on the canvas for 6 days after each event.
- Both are worked out directly from the current day, not from the previous frame. So when you drag the Time slider backwards or forwards, the rings and chips are always correct for that day.

---

## Accuracy and limitations

- **Month lengths are real.** All four month lengths use true mean values. Completion days on the chips are exact to the value shown.
- **Sizes and distances are not to scale.** The Sun, Earth, Moon and orbit sizes are chosen so everything fits on the screen.
- **Mean values only.** Real individual months vary. For example, a single synodic month can be several hours shorter or longer than 29.53 days, because of the Moon's elliptical orbit and the Sun's pull. The animation shows only the averages.
- **Teaching geometry changes the implied sidereal month.** In the *Anomalistic* and *Draconic* tabs, the precession is sped up while the month length stays at its real value. At the "teaching" setting, this means the Moon's period relative to the stars in those two tabs is not 27.32 days (it works out to about 24.7 days in *Anomalistic* and about 29.9 days in *Draconic*). At the "real" setting it matches 27.32 days. This does not affect the month being demonstrated in each tab.
- **Circular orbits in two tabs.** *Synodic vs Sidereal* and *Draconic* use circular orbits. Only *Anomalistic* uses an ellipse.
- **Simplified Moon shading.** The Moon's lit half is drawn as seen from above the orbit, not as the phase seen from Earth.
- **Tropical month not animated.** It differs from the sidereal month by only about 7 seconds, which is too small to show.
- **Fixed time span.** The animation always covers 66 days and then restarts from day 0.

---

## Files in this repository

```
.
├── index.html   The complete tool: layout, styles and code in one file
└── README.md    This file
```

---

## Credits

- Created by **Pranshu Kurel**, AstroVariable.
- Mean lunar month lengths and orbital elements: standard published mean values (epoch J2000.0).
- Kepler's equation solver: standard Newton's method.
- Fonts: Fraunces, Inter and JetBrains Mono, via Google Fonts.

---

## Licence

The code in this repository is released under the licence in the [`LICENSE`](LICENSE) file.
