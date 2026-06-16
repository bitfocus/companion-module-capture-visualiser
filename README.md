# companion-module-capture-visualiser

Bitfocus Companion module for **Capture Visualiser** OSC control.

This version targets **Companion module API 2.0** for Companion **4.3+**.

---

## Setup

1. In Companion, add **Capture.se → Capture Visualiser**.
2. Set **Target IP** to the machine running Capture Visualiser.
3. Set **OSC Port** to the Capture OSC port, default `4004`.

If Capture is running on the same machine as Companion, use the machine's LAN IP address rather than `127.0.0.1`.

---

## Actions

| Action | Description |
|---|---|
| Ping Capture | Sends `/ping` |
| Refresh catalogs | Requests available camera catalogs |
| Get live view status | Requests current live view status |
| Set Ambient Lighting | Sets ambient lighting level as a percentage |
| Set Fill Lighting | Sets fill lighting level as a percentage |
| Set Hue Clamp | Sets hue clamp level as a percentage |
| Set Bloom | Sets bloom level as a percentage |
| Set Exposure Adjustment | Sets exposure adjustment from `-3EV` to `+3EV` |
| Set White Balance | Sets white balance from `2500K` to `10000K` |
| Set Automatic Exposure | Turns automatic exposure on or off |
| Set Laser Flicker | Turns laser flicker effect on or off |
| Change Camera Position | Recalls a catalog camera position with optional transition timing, dampening, and curvature |

---

## Feedbacks

| Feedback | Condition |
|---|---|
| Any live view active | Active when Capture reports a live view index |
| Specific view live | Active when the selected view index is live |

---

## Variables

| Variable | Content |
|---|---|
| `$(capture:product_name)` | Capture product name |
| `$(capture:product_version)` | Capture product version |
| `$(capture:catalog_count)` | Number of discovered catalogs |
| `$(capture:live_view_index)` | Current live view index |
| `$(capture:camera_x)` / `camera_y` / `camera_z` | Current camera position |
| `$(capture:focus_x)` / `focus_y` / `focus_z` | Current focus position |
| `$(capture:catalog_N_name)` | Dynamic catalog name |
| `$(capture:catalog_N_pos_M_name)` | Dynamic catalog position name |

---

## Presets

| Category | Contents |
|---|---|
| Camera Positions | Dynamic camera position buttons generated from Capture catalogs |
| Lighting | Ambient, fill, hue, bloom, exposure, laser flicker, and white balance presets |
| System | Ping, get status, and refresh catalogs |
