Personal Toolbox
A browser-based collection of practical PDF, image, text, developer, and generator tools.
Personal Toolbox is 100% client-side: files are processed in the user's browser and no file-processing backend is required.
Features
PDF Tools
Merge PDFs
Split / Extract PDF pages
Images to PDF
Rotate PDF pages
Add watermark
Reduce PDF size
Add page numbers
PDF to images
Organize PDF pages
PDF information
Scan documents with a phone camera
Image Tools
Crop images
Resize images
Rotate / flip
JPG / PNG / WebP conversion
Image compression
Image information / metadata
DPI and print-size calculations
Remove image metadata
Text Tools
Word counter and case tools
Scratchpad
Diff checker
Markdown previewer
Developer Tools
JSON formatter
Base64 encoder / decoder
URL encoder / decoder
Hash generator
Unix timestamp converter
Color converter
Generators
QR code generator
Password generator
Lorem Ipsum generator
Privacy
Files selected for PDF and image operations are processed locally in the browser. No server-side file-processing API is required.
The application uses browser APIs and JavaScript libraries. Some libraries are loaded from CDNs, so an internet connection may be required when the page first loads them.
Technology
HTML5
CSS3
JavaScript
pdf-lib
PDF.js
JSZip
QRCode.js
Running locally
Most tools can be used by opening index.html directly.
For the live camera scanner, browsers normally require a secure context such as HTTPS or localhost. When using a local file:// page on Android, use the built-in Use Camera / Gallery fallback.
Deploying to Render
This is a static site and does not require a build command.
Use these Render settings:
Setting
Value
Service Type
Static Site
Repository
sdfprwz/Personel-toolbox
Branch
main
Root Directory
Leave blank
Build Command
Leave blank
Publish Directory
.
Environment Variables
None required
The repository should contain:
Personel-toolbox/
├── index.html
└── README.md
Render will serve index.html at the root of the site.
Because the deployed site uses HTTPS, the live camera feature can request camera permission from supported browsers.
Camera scanner
The scanner supports:
Live camera preview when browser permissions allow it
Android Camera / Gallery fallback
Multiple scanned pages
Page thumbnails
A4, Letter, or automatic page sizing
High, Balanced, and Small PDF quality
Creating one PDF from multiple captured pages
Camera access still depends on the browser and device permissions.
Multiple-file workflow
Multi-file tools support adding files sequentially:
Select the first file.
Tap + Add another file.
Select another file.
Repeat as required.
Run the operation.
This is useful for PDF merging, image conversion, image resizing, and other batch operations.
Performance
All processing happens in the browser, so memory usage depends on the user's device.
For very large PDFs or high-resolution images:
Process smaller batches.
Avoid unnecessarily high image resolutions.
Use smaller quality settings when appropriate.
Close memory-heavy browser tabs on mobile.
Project structure
The project is intentionally simple:
Personel-toolbox/
├── index.html
└── README.md
The application is a single-page client-side application and requires no backend server.
Deployment
The project can be hosted on any service that serves static HTML, including Render Static Sites and GitHub Pages.
No Node.js server or backend API is required.
