SOUTHPORT FIRE DEPARTMENT TV DASHBOARD

FILES
- index.html — the complete dashboard.

HOW TO RUN
1. Put index.html on the hallway TV computer.
2. Open it in Chrome or Edge.
3. Press F11 for full-screen.
4. Keep the computer connected to the internet.

For the most dependable setup, serve the folder instead of opening the file directly:
- Mac/Linux: open Terminal in the folder and run: python3 -m http.server 8080
- Windows: run: py -m http.server 8080
Then open: http://localhost:8080

DATA SOURCES
- National Weather Service API: current observations, hourly forecast, daily high/low, and alerts.
- NOAA CO-OPS: Southport tide predictions, station 8659084.
- NC State Climate Office / NC Forest Service-supported fire danger map.
- Brunswick County Fire Marshal burn-ban page.

IMPORTANT BURN-BAN SETTING
The dashboard has BURN_BAN_ACTIVE = true because Brunswick County's official page showed an active burn-ban notice when this version was created.
When the ban is officially lifted, open index.html in a text editor and change:
const BURN_BAN_ACTIVE = true;
to:
const BURN_BAN_ACTIVE = false;

The dashboard's colored “Local Readiness Indicator” is calculated from humidity, wind, and rain probability. It is not the official NC Forest Service adjective rating.

NOAA/NWS SCROLLING TICKER
The updated version includes a continuous bottom ticker that rotates:
- Active NWS warnings, watches, advisories and special weather statements
- The detailed Southport forecast
- The AMZ252 marine forecast from Cape Fear to Little River Inlet out 20 NM
- NOAA Weather Radio information
The ticker changes color automatically for warnings, watches and advisories.
