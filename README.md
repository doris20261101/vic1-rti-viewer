# VIC1 two-sided RTI viewer
Deploy `index.html` alone to the existing GitHub repository powering https://vic1-rti-viewer.vercel.app/.
- Outboard Surface: RTI_5, `?side=RTI_5`
- Inboard Surface: RTI_2, `?side=RTI_2`
- RTI_1 has been removed. No MP4 animations.
- Both normal and albedo images are embedded in `index.html`.
- The labels indicate user-provided orientation, not inferred from the images.

# Optional matching 3D hotspot site
The second ZIP contains an updated `index.html` plus `config.js` for the 3D OBJ main site.
In Curator tools, select the hotspot's correct RTI in the 'Default media' menu. 
Place the Inboard hotspot on the internal degraded region of the 3D OBJ, and the Outboard hotspot at the surface coating.
Actual 3D positions cannot be determined from the 2D image alone.
After saving, Copy hotspot JSON and paste it into config.js hotspots array.
Existing previously saved hotspots require reselecting/remaking if their saved media values were different.
