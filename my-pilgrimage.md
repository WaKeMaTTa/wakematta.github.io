---
layout: page
title: My Pilgrimage
---
## My Pilgrimage

Allow me to share with you all the CGMJCI congregations around the world that I’ve had the honor of attending.

So far, I have visited 17 churches across four countries: France, Switzerland, Germany, and Italy.

<div id="map" style="height: 500px;"></div>

. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

<script>
  const points = [
    {
      location_name: "Marseille, France",
      coordinates: [43.292163, 5.3734908],
      visit_card_url: "https://direcciones.idmji.org/en/iglesia/697/",
    },
    {
      location_name: "Avignon, France (CLOSED)",
      coordinates: [43.9263999, 4.8436042],
      visit_card_url: "https://direcciones.idmji.org/en/iglesia/1146/",
    },
    {
      location_name: "Paris (Pantin), France",
      coordinates: [48.8974317, 2.40503],
      visit_card_url: "https://direcciones.idmji.org/en/iglesia/589/",
    },
    {
      location_name: "Lyon, France",
      coordinates: [45.7498111, 4.8282579],
      visit_card_url: "https://direcciones.idmji.org/en/iglesia/970/",
    },
    {
      location_name: "Nice, France",
      coordinates: [43.7003848, 7.2829292],
      visit_card_url: "https://direcciones.idmji.org/en/iglesia/846/",
    },
    {
      location_name: "Paris 14th (Montparnasse), France",
      coordinates: [48.8273987, 2.3209477],
      visit_card_url: "https://direcciones.idmji.org/en/iglesia/1062/",
    },
    {
      location_name: "Beaucaire, France",
      coordinates: [43.8236389, 4.6266716],
      visit_card_url: "https://direcciones.idmji.org/en/iglesia/841/",
    },
    {
      location_name: "Geneva (Carouge), Switzerland",
      coordinates: [46.1799519, 6.1422544],
      visit_card_url: "https://direcciones.idmji.org/en/iglesia/403/",
    },
    {
      location_name: "Lausanne, Switzerland",
      coordinates: [46.5404222, 6.6308944],
      visit_card_url: "https://direcciones.idmji.org/en/iglesia/653/",
    },
    {
      location_name: "Neuchâtel (Peseux), Switzerland",
      coordinates: [46.9851423, 6.8972302],
      visit_card_url: "https://direcciones.idmji.org/en/iglesia/400/",
    },
    {
      location_name: "Bern, Switzerland",
      coordinates: [46.9466099, 7.4401543],
      visit_card_url: "https://direcciones.idmji.org/en/iglesia/718/",
    },
    {
      location_name: "Zürich, Switzerland",
      coordinates: [47.3862163, 8.5022607],
      visit_card_url: "https://direcciones.idmji.org/en/iglesia/719/",
    },
    {
      location_name: "München, Germany",
      coordinates: [48.1404777, 11.5235582],
      visit_card_url: "https://direcciones.idmji.org/en/iglesia/335/",
    },
    {
      location_name: "Dornbirn, Austria",
      coordinates: [47.3992929, 9.7358132],
      visit_card_url: "https://direcciones.idmji.org/en/iglesia/1172/",
    },
    {
      location_name: "Lugano (Lamone), Switzerland",
      coordinates: [46.0387765, 8.9276274],
      visit_card_url: "https://direcciones.idmji.org/en/iglesia/727/",
    },
    {
      location_name: "Milano, Italy",
      coordinates: [45.524364, 9.1931905],
      visit_card_url: "https://direcciones.idmji.org/en/iglesia/51/",
    },
    {
      location_name: "Torino, Italy",
      coordinates: [45.0481003, 7.67399],
      visit_card_url: "https://direcciones.idmji.org/en/iglesia/683/",
    },
  ]


  function waitForLeaflet(callback) {
    if (typeof L !== 'undefined') {
      callback();
    } else {
      setTimeout(() => waitForLeaflet(callback), 100);
    }
  }

  waitForLeaflet(() => {
    var map = L.map('map').setView([46.1665, 6.7248], 5);

    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
      attribution: '&copy; OpenStreetMap contributors'
    }).addTo(map);

    points.forEach(point => {
      const marker = L.marker(point.coordinates).addTo(map);
      marker.bindPopup(
        `<strong>${point.location_name}</strong><br><small><a href="${point.visit_card_url}" target="_blank">Visit card</a></small>`
      );
    });
  });
</script>
