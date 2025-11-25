---
layout: simple-page
title: Contact
permalink: /contact
menu: contact

---


<div class="col-1-of-3" markdown=1>

For enquiries please contact:

*vibekenordmarkhansen @ gmail.com*

Imperial College South Kensington campus is accessible on public transport
by the Picadilly, District and Circle lines. The nearest stations are South Kensington and Gloucester Road.

</div>

<div class="col-2-of-3">

  <div id="mapdiv" height="460"></div>
</div>

See the map below for the building locations for the symposium.

<img src="/assets/img/campus-map.png" width="94%"/>


<script src="https://www.openlayers.org/api/OpenLayers.js"></script>
<script>
  map = new OpenLayers.Map("mapdiv");
  map.addLayer(new OpenLayers.Layer.OSM());

  var lonLat = new OpenLayers.LonLat( -0.178973, 51.498889 )
        .transform(
          new OpenLayers.Projection("EPSG:4326"), // transform from WGS 1984
          map.getProjectionObject() // to Spherical Mercator Projection
        );

  var zoom=16;

  var markers = new OpenLayers.Layer.Markers( "Markers" );
  map.addLayer(markers);

  markers.addMarker(new OpenLayers.Marker(lonLat));

  map.setCenter (lonLat, zoom);
</script>
