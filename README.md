# AISwitch

  Website Switcher - Airplane Dashboard

  OVERVIEW:
  This HTML page serves as a comprehensive dashboard for smart plug energy optimization based on real-time weather data.
  It features automatic and manual geolocation, dynamic graph plotting using Plotly, plug configuration, schedule optimization,
  and automated webhook execution to switch smart plugs ON/OFF.

  KEY FEATURES:
  1. Layout & Styling:
     - Uses Bootstrap 4 for layout and responsiveness.
     - Orbitron font for a cockpit-inspired aesthetic.
     - Custom dark theme styling for a modern look.

  2. Geolocation:
     - Attempts automatic location detection.
     - Option for manual city/village input if geolocation fails or user prefers manual control.

  3. Weather Integration:
     - Fetches weather data from Open-Meteo API.
     - Uses UV index and wind speed to compute a renewable energy score.

  4. Plug Management:
     - Users can add/delete multiple smart plugs.
     - Each plug has configurable on hours, total hours, and kWh usage.
     - Webhooks for ON/OFF control (testable via button).
     - Plug status updates live every minute.

  5. Visualization:
     - Plots wind, UV, and renewable energy data in Plotly.
     - Superimposes plug schedules (uniform and optimized) on the same graph.
     - Graph is responsive and allows range selection (6h, 12h, 1d, all).

  6. Schedule Optimization:
     - Two schedule modes: User Planned and Optimized (based on renewable quality).
     - Plug operation adapts to forecast changes while respecting desired on-time per cycle.

  7. State Management:
     - Settings (location, slider, plug configs) can be saved/loaded using localStorage.

  8. Automatic Refresh:
     - Weather data and plug schedules update hourly.
     - A visible countdown timer shows time left until the next update.

  9. Plug Control:
     - The page evaluates the current time against the schedule.
     - Fires webhook ON/OFF only if plug state changes.
     - Ensures each plug completes its required ON time even if forecast changes.

  10. Accessibility:
     - Fully mobile-responsive layout.
     - Clear labels, small text hints, and tooltips.

  INSTRUCTIONS:
  - Customize plug settings, enter location, and choose a scheduling strategy.
  - Adjust the energy slider to influence optimization.
  - Save/load preferences using the buttons at the top.
  - Monitor schedule execution and plug state live via graph and plug panel.
