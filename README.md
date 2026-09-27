# SENTRA — Smart Safety & Emergency Monitoring (Prototype)

Competition prototype for schools and factories. **All sensor data, AI results and security indicators are simulated.**
No hardware, backend or emergency services are connected.

## Run
Open `index.html` in a modern browser (Chrome, Edge, Firefox), or serve the folder:

    npx serve .        # or: python -m http.server 8080

Demo login: `admin@sentra.demo` / `Sentra@2026`

## Structure
    index.html          App shell + all page skeletons
    css/style.css       Theme tokens (light/dark), layout, components, responsive rules
    js/utils.js         DOM/format/math helpers, icons, sparklines, storage
    js/data.js          Mock configuration: sensors, zones, maps, scenarios, devices, seed history
    js/state.js         Central state object + Store (pub/sub + selectors)
    js/simulation.js    MockDataSource (readings) + Rules (status, risk, alarm hardware)
    js/ai.js            Simulated sensor-fusion classifier + evacuation routing
    js/charts.js        Dependency-free canvas charts (theme aware)
    js/ui.js            Rendering for chrome, views, map, camera feeds, modals
    js/app.js           Boot, auth gate, routing, events, scenario orchestration
    assets/             Logo and favicon
