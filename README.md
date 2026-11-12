# Canyon Notes - Rally Maps

A mobile-first interactive map prototype for US-34 through Big Thompson Canyon, from Loveland to Estes Park.

## Current prototype
- Dark MapLibre map using OpenFreeMap tiles.
- Road route fetched at runtime from the public OSRM demo routing service.
- Experimental left/right corner detection based on route geometry, limited to the canyon stage.
- Bidirectional stage view: switch between Loveland → Estes and Estes → Loveland; corner order and left/right labels are recalculated for the selected direction.
- Canyon stage starts at the Dam Store pullout, snapped to the nearest point on the routed US-34 geometry. The current finish is the existing route endpoint.
- Numbered corner markers and a touch-friendly roadbook list.
- Tap a note or marker to zoom to that corner.
- Toggle corner markers and route line.
- Zoom, fit-route, and optional browser geolocation controls.
- Responsive layout designed primarily for phones.

## Important limitations
- This is a standalone companion map, not a plugin embedded inside the Google Maps app.
- The road route and basemap require an internet connection.
- The public OSRM and OpenFreeMap services are prototype dependencies, not guaranteed production infrastructure.
- Corner severity is a rough geometric estimate. It is not a verified rally pacenote, speed recommendation, or hazard assessment.
- The current model does not account for elevation, camber, sight lines, surface conditions, traffic, or hazards. Validate every note before relying on it.
- Do not interact with the map while driving. Have a passenger operate it, or inspect the route while stopped.

## Next steps
1. Verify the exact canyon finish boundary and confirm that the returned route follows the intended US-34 segment.
2. Improve corner detection using road curvature and radius rather than a single heading-change threshold.
3. Add elevation-aware context and editable notes.
4. Add a route editor and save validated routes.
5. Add live GPS progress only after the route and notes are validated.
