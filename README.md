# VIC1 dual-surface interactive relighting viewer
This deploys as a static page to Vercel: upload `index.html` alone at the repository root.
No additional image asset folder is required: both surfaces' albedo and normal textures are embedded.
Surface A: RTI_5; Surface B: RTI_1. These labels refer to source datasets, not proven anatomical faces.
Default: ?side=RTI_5
Second surface: ?side=RTI_1
The user can also use the two buttons to switch datasets.
This is normal-map based interactive surface relighting rather than full PTM/RTI polynomial reconstruction.
The TIFF originals were not modified; 2560x1706 WebP previews are embedded.
To update: replace old index.html in the vic1-rti-viewer GitHub repository, commit, and wait for Vercel's deployment.
The VIC1 OBJ main site's config.js may keep rtiViewerUrl: 'https://vic1-rti-viewer.vercel.app/'.
