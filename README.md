# Website

<!Doctype>
<html>
<body>
<style>



img {
    float: left;
}
h1{
   float: left;
   font-family: algerian;
   font-size: 50
   }
</style>

<img src="https://www.2b1stconsulting.com/wp-content/uploads/2012/11/Sinopec_Key_Facts_and_Figures_in_brief1.png" width="150" height="180" />
<h1 align="center">Sinopic Petrol Pump</h1>
<style>
ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    overflow: hidden;
    background-color: #333;
}

li {
    float: left;
}

li a {
    display: block;
    color: white;
    text-align: center;
    padding: 12px 30px;
    text-decoration: none;
}

li a:hover:not(.active) {
    background-color: #111;
}

.active {
    background-color: #4CAF50;
}
</style>
</head>
<body>
<br>
<br><br><br><br><br><br>
<ul>
  <li><a class="active" href="#home">Home</a></li>
  <li><a href="file:///C:/Users/Hemant%20Sah/Desktop/Notepad/about.html">About US</a></li>
  <li><a href="file:///C:/Users/Hemant%20Sah/Desktop/Notepad/Contact%20Us.html">Contact</a></li>
  <form>
  <li> <input type="text" name="search" placeholder="Search..">
</form> </li>

</ul>
</p>
<style> 
input[type=text] {
    width: 130px;
    box-sizing: border-box;
    border: 2px solid #ccc;
    border-radius: 4px;
    font-size: 16px;
    background-color: white;
    background-image: url('searchicon.png');
    background-position: 10px 10px; 
    background-repeat: no-repeat;
    padding: 12px 20px 12px 40px;
    -webkit-transition: width 0.4s ease-in-out;
    transition: width 0.4s ease-in-out;
}
    <meta name="viewport" content="initial-scale=1.0, user-scalable=no">
    <meta charset="utf-8">
    <title>Waypoints in directions</title>
    <style>
      #right-panel {
        font-family: 'Roboto','sans-serif';
        line-height: 30px;
        padding-left: 10px;
      }

      #right-panel select, #right-panel input {
        font-size: 15px;
      }

      #right-panel select {
        width: 100%;
      }

      #right-panel i {
        font-size: 12px;
      }
      html, body {
        height: 100%;
        margin: 0;
        padding: 0;
      }
      #map {
        height: 50%;
        float: left;
        width: 70%;
        height: 50%;
      }
      #right-panel {
        margin: 20px;
        border-width: 2px;
        width: 20%;
        height: 400px;
        float: left;
        text-align: left;
        padding-top: 0;
      }
      #directions-panel {
        margin-top: 10px;
        background-color: #FFEE77;
        padding: 10px;
        overflow: scroll;
        height: 174px;
      }
    </style>
  </head>
  <body>
    <div id="map"></div>
    <div id="right-panel">
    <div>
    <b>Start:</b>
    <select id="start">
      <option value="Hyderabad">Hyderbad</option>
      <option value="Vijayawada">Vijayawada</option>
      <option value="Vizag">Vizag</option>
    </select>
    <br>
    <b>Waypoints:</b> <br>
    <i>(Ctrl+Click or Cmd+Click for multiple selection)</i> <br>
    <select multiple id="waypoints">
      <option value="nalgonda">Nalgonda</option>
      <option value="miralaguda">miralaguda</option>
      <option value="eluru">eluru</option>
      <option value="rajahmundry">rajahmundry</option>
      <option value="rajavommangi">rajavommangi</option>
    </select>
    <br>
    <b>End:</b>
    <select id="end">
      <option value="Hyderabad">Hyderbad</option>
      <option value="Vijayawada">Vijayawada</option>
      <option value="Vizag">Vizagoption>
     </select>
    <br>
      <input type="submit" id="submit">
    </div>
    <div id="directions-panel"></div>
    </div>
    <script>
      function initMap() {
        var directionsService = new google.maps.DirectionsService;
        var directionsDisplay = new google.maps.DirectionsRenderer;
        var map = new google.maps.Map(document.getElementById('map'), {
          zoom: 6,
          center: {lat: 16.592830, lng: 80.836012}
        });
        directionsDisplay.setMap(map);

        document.getElementById('submit').addEventListener('click', function() {
          calculateAndDisplayRoute(directionsService, directionsDisplay);
        });
      }

      function calculateAndDisplayRoute(directionsService, directionsDisplay) {
        var waypts = [];
        var checkboxArray = document.getElementById('waypoints');
        for (var i = 0; i < checkboxArray.length; i++) {
          if (checkboxArray.options[i].selected) {
            waypts.push({
              location: checkboxArray[i].value,
              stopover: true
            });
          }
        }

        directionsService.route({
          origin: document.getElementById('start').value,
          destination: document.getElementById('end').value,
          waypoints: waypts,
          optimizeWaypoints: true,
          travelMode: 'DRIVING'
        }, function(response, status) {
          if (status === 'OK') {
            directionsDisplay.setDirections(response);
            var route = response.routes[0];
            var summaryPanel = document.getElementById('directions-panel');
            summaryPanel.innerHTML = '';
            // For each route, display summary information.
            for (var i = 0; i < route.legs.length; i++) {
              var routeSegment = i + 1;
              summaryPanel.innerHTML += '<b>Route Segment: ' + routeSegment +
                  '</b><br>';
              summaryPanel.innerHTML += route.legs[i].start_address + ' to ';
              summaryPanel.innerHTML += route.legs[i].end_address + '<br>';
              summaryPanel.innerHTML += route.legs[i].distance.text + '<br><br>';
            }
          } else {
            window.alert('Directions request failed due to ' + status);
          }
        });
      }
    </script>
    <script async defer
    src="https://maps.googleapis.com/maps/api/js?key=AIzaSyAsoiP3jgf2wiOoxLNaBLVYJ8xGEa2-290&callback=initMap">
    </script
	
<!-- saved from url=(0061)file:///C:/Users/SUKRUT(BLACK)/Desktop/sukrut/calculator.html -->
<html><head><meta http-equiv="Content-Type" content="text/html; charset=windows-1252"><script language="javascript">
                function multiplyNumbers()
                {
                        var a = 12.56;
                        var b = parseInt(document.getElementById("value2").value);
                        var c = parseInt(document.getElementById("value3").value);
                        var ansD = document.getElementById("answer");
                        ansD.value = 12.56*b;
                    var ansE = document.getElementById("answer1");
                        ansE.value = 12.56*b/c;  

                    
                }
</script>
      
  </head>
  <body>
       
  <p1> <font size="5" color="black" align="center">Please put distance between the two points. </font></p1><font size="5" color="black" align="center"> 
= <input type="text" id="value2" name="value2" value="0">

        Volume of pipeline between selected points = <input type="text" id="answer" name="answer" value=""> 
Cubickilometers.
<font size="5" color="black" align="center">Please put number of robots  
= <input type="text" id="value3" name="value3" value="2">
<input type="button" name="Sumbit" value="Here we go" onclick="javascript:multiplyNumbers()"><br>
Number of hours required= <input type="text" id="answer1" name="answer1" value=""> 
Cubickilometers.


</font></font>

</body></html>
	
