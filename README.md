# AppNova-arishafatima-uzmayaseen
# CampusFind

A lost & found mobile app for University of Lahore students. Report lost or found items with your exact GPS location, browse everything reported on campus, and see which items are closest to you.

Built for **AppNova**.

## Team

| | |
|---|---|
| App name | CampusFind |

| Member | SAP ID |
|---|---|
| Arisha Fatima| 70147272 |
| Uzma Yaseen| 70146302|

## Tech stack

- **Language:** Java + XML (Android Studio)
- **UI:** Material Design 3, light yellow theme
- **Database:** SQLite (local, via `SQLiteOpenHelper`)
- **Authentication:** Own users table; passwords stored as salted SHA-256 hashes, never plain text
- **Session:** `SharedPreferences`
- **Location:** Android `LocationManager` (no API keys needed)
- **Min SDK:** 26 (Android 8.0)s

## Features completed (F1 - F12)

**Level 1 - Core**
- F1: Custom launcher icon and app name
- F2: Separate Login and Register screens with validation
- F3: Bottom navigation (Home, Nearby, Report, Profile) and Profile tab with team info and Logout
- F4: Home list with the 6 starter items, newest first
- F5: Item details screen

**Level 2 - Standard**
- F6: Report form (Lost/Found) with validation
- F7: "Use my current location" fills latitude and longitude (5 decimals)
- F8: Items saved in the local database and shown at the top of Home immediately
- F9: Session stays after restart; Logout returns to Login

**Level 3 - Advanced**
- F10: Open the item's location in the Maps app
- F11: Nearby tab sorted by distance (metres below 1 km, otherwise km)
- F12: Lost/Found filter on Home and "Mark as Returned" for your own items

## How to run

1. Clone the repository:
   ```
   git clone https://github.com/your-username/AppNova-EntryID-TeamName.git
   ```
2. Open the project folder in Android Studio and wait for Gradle sync to finish.
3. Run on an emulator or a real phone (Android 8.0 or higher).
4. Allow the location permission when asked.
   - Emulator: set a location in Extended controls > Location (for example 31.38955, 74.24070).
5. Register an account, then log in.

An APK is included in the repository root.

## Screenshots

| Login | Home | Report | Nearby | Details |
|---|---|---|---|---|
| _add_ | _add_ | _add_ | _add_ | _add_ |

## Project structure

```
app/src/main/java/com/campusfind/app/
  LoginActivity, RegisterActivity   - authentication screens
  MainActivity                      - bottom navigation
  HomeFragment, NearbyFragment,
  ReportFragment, ProfileFragment   - the four tabs
  DetailActivity                    - item details
  DbHelper                          - SQLite (users + items)
  LocationHelper                    - GPS
  Session                           - logged-in user
```
