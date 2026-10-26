# BusMate requested UI updates

- Added a shared `/users` route that opens the correct Student or Faculty dashboard based on the authenticated session. Both login success responses now route to `/users`; legacy `/student` and `/faculty` paths remain compatible.
- `/driver` now shows a dedicated driver login page when no driver session exists. The page links to driver registration, and successful registration returns to `/driver` for login.
- Student and Faculty dashboard sections open as a single full-page view. The other dashboard cards are hidden until the user presses **Back to Dashboard**.
- Updated live-map tracking marker to use the supplied tracking-pin image, increased its size, added a clearer blue GPS trail, and made the marker popup show the latest location and coordinates.
- Existing admin login/dashboard and underlying API/data workflows were left in place.

Run with the existing setup: install `requirements.txt`, then start `python app.py`.

## Follow-up dashboard refinements (2026-10-26)
- Added `/user` as an alias for the shared `/users` dashboard route. Signed-in students and faculty are routed to their respective dashboard; a direct unauthenticated `/user` visit opens the student dashboard instead of the login page.
- Removed the extra manual “View All Bus Routes” and “View Today's Return Buses” buttons from student/faculty dashboards. Opening either box now loads the route/return-bus list automatically.
- Improved the Back to Dashboard button contrast, size, hover state, and keyboard-focus visibility.
