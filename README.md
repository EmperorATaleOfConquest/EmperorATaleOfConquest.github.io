# EmperorATaleOfConquest.github.io
<!DOCTYPE html>
<html = style="height: 100%;">
  <head>
    <title>DnD World Map</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="scripts/leaflet.css">
    <script src="scripts/leaflet.js"></script>
  </head>
  
  <body style="height: 100%;margin: 0;">
    <div id="map" style="width: 100%; height: 100%; background: #000000;"></div>
    <script type="text/javascript">
  //Creating the Map
    var map = L.map('map').setView([0, 0], 0);
    L.tileLayer('map/{z}/{x}/{y}.png', {
      continuousWorld: false,
      noWrap: true,  
      minZoom: 0,
      maxZoom: 10,
    }).addTo(map);
  //Coordinate Finder
    var marker = L.marker([0, 0], {
      draggable: true,
    }).addTo(map);
    marker.bindPopup('LatLng Marker').openPopup();
    marker.on('dragend', function(e) {
      marker.getPopup().setContent(marker.getLatLng().toString()).openOn(map);
    });
  //Markers
    </script>
  </body>
</html>
