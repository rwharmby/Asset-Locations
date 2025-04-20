# Asset-Locations
List of asset location with in the terminal 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Medical Asset Locations</title>
  <style>
    body { font-family: sans-serif; padding: 20px; background: #f9f9f9; color: #333; }
    h1 { color: #5a2a83; }
    select, input { padding: 8px; margin: 10px 0; width: 100%; max-width: 400px; }
    .item { padding: 10px; border-bottom: 1px solid #ccc; }
    .area { font-weight: bold; }
    .location { color: gray; }
  </style>
</head>
<body>
  <h1>Medical Asset Locations</h1>
  <select id="category" onchange="renderList()">
    <option>Medical Screens</option>
    <option>Defibrillators</option>
    <option>Lifts</option>
    <option>Travelators</option>
    <option>Escalators</option>
  </select>
  <input type="text" id="search" placeholder="Search..." oninput="renderList()" />

  <div id="list"></div>

  <script>
    const data = {
      'Medical Screens': [
        { area: 'Terminal 3 Landside', descriptor: 'Zone B by Lifts to South Exit', location: '202A' },
        { area: 'Terminal 3 Landside', descriptor: 'Zone D Adjacent to Baggage X-ray', location: '202B' }
      ],
      'Defibrillators': [
        { area: 'Terminal 3 Landside', descriptor: 'Arrivals baggage hall (next to left luggage)', location: 'D1' },
        { area: 'Terminal 3 Landside', descriptor: 'Arrivals link corridor', location: 'D2' }
      ],
      'Lifts': [
        { area: 'Terminal 3 Landside', descriptor: 'Check-in hall', location: 'L1' },
        { area: 'Terminal 3 Landside', descriptor: 'Central forecourt', location: 'L2
