# The 'VegBot' R&D lab
<br>
To conveniently facilitate local off-site R&D  for the https://github.com/simplyEngineering , a small greenhouse 'lab' was constructed, based upon a <a href="https://www.quickcrop.co.uk/product/vegtrug-tomato-greenhouse"> 'VegTrug' Tomato greenhouse</a>. This structure has a small footprint, alowing it to be  unusually located within the cockpit of 'Lena Mary', my dry-docked Moody 40 sailing yacht stripped of its steering gear.
<br>
<br>
<table>
<tr>
	<th width="50%">The basic 'VegBot' frame.</th>
	<th>The 'VegBot' frame in the cockpit (looking aft).</th>
</tr>
<tr>
	<td><image src = "images/Vegtrug frame with cover.jpg"></td>
	<td><image src = "images/VegTrug%20in%20situ%20(cockpit).jpg"></td>
</tr>
</table><br><br>

<table>
	<tr>
		<th colspan="2">Air quality control in the VegBot</th>
	</tr>
	<tr>
		<td width="50%">Air conditions within the VegBot are regulated under the control of the ESP8266 Master module. Minimum temperature is established by a heater control loop which is activated whenever the actual temperature falls below the  setpoint temperature by a set margin (nominally 1 degree). Deactivation occurs whenever the actual temperature exceeds the setpoint temperature by more than the same set margin. <br><br>Should the actual temperature exceed the solar gain margin (nominally 3 degrees) even when the heater is off as would be the case under summer conditions, induction and extractor fans are activated to introduce colder ambient air from and exhaust warm air to the outside space under the VegBot. Irrespective of the temperature control status, the induction and exhaust fans are activated to ensure that the air in the VegBot is completely changed at least once every 4 minutes. </td>
		<td>Maintaining a uniform temperature throughout the VegBot is only posible if the enclosed air is continuously recirculated. The recirculation fan at the head of the reciculation pipe lifts heated air from below the centre shelf and pushes it out into the space above the top shelf. From here it cools and by gravitation moves back down into the lower regions of the VegBot.<br><br><image src="images/VegTrug%20prior%20to%20installation%20showing%20ventilation%20pipes.jpg"><br><b>Ventilation pipe (rear) and recirculation pipe (front).</b></td>
	</tr>
	<tr>
		<td><image src="images/inletCircFan.jpg"><br>Ambient air induction fan and recirculation fan atop the ventilation and recirculation pipes respectively.</td>
		<td><image src="images/ExtractorFan.jpg"><br>Extractor fan in base of VegBot.</td>
	</tr>
	<tr>
		<td><image src = "images/humidifierHeater.jpg" width = "100%"></td>
		<td><br>The heater  (right) is a 500W ceramic element PTC device which is both fast heating and safe to use in an enclosed environment. The humidifier (left) is a generic 2.8l domestic device.  Both are controlled via isolating relays from the Master module. </td>
	</tr>
</table>
<table>
	<tr><th colspan="2%">The VegBot Control Centre and Camera</th></tr>
	<tr><td><image src="images/controlCentreCameraTubes.jpg"><td width="50%">The Control Centre comprising (from bottom to top) with recirculating and ventilation pipes behind:
		<ul>
		<li>'Poweradd' backup battery.</li>
		<li>8-port USB power supply.</li>
		<li>Master module with transducer fan.</li>
		</ul>
		The backup battery is continuously charged from the USB power supply and maintains system functionality in the event of mains failure.
		<br><br>
		The 8-port 5V usb power supply delivers power to the Master module, transducer fan, Camera module and recirculation and ventilation fans.
		<br><br>
		The ESP8266 Master module (described above) is equipped with a fan which ensures that the transducers are continuously fed with ambient air, without which the control loops would suffer considerable lag and significant deviation from their setpoints.
		<br><br>
		The ESP32-CAM Camera module.
		</td></tr>
</table>
	<br><br>
<table>
	<tr><th colspan="2">The Camera Module</th></tr>
	<tr><td colspan="2"><image src="images/cameraModule.jpg"></td></tr>
	<tr><td><b>Seeing is believing!</b><br><br> To supplant the data acquisition an ESP32-cam module (upper right) acquires a 1600 x 1200 jpg image every 30 minutes.  Using its WiFi client capabilities it uploads it to a public file server for viewing.<br><br> Having no intrinsic USB serial port a generic FTDI interface (lower right) is included on the board for convenience. The circular component is a 0.22F supercapacitor without which this camera may 'brownout' the supply due to a high level of surge current during data acquisition. <br><br>The relay module(centre left) is used to switch power to a 20W LED batten luminaire during the acquisition cycle.</td><td width="75%"><image src = "images/vegcam1.jpg"><br>The uploaded camera image is overlayed with a data panel by means of an HTML iFrame, its data source being extracted from the SQL data server sourced from a WiFi local host or LoRa Receiver/Gateway module.</td></tr>
</table>
<br><br>
	
# This is an active project - watch this space for further material<br>
	
### Enquiries to:&nbsp;&nbsp;<a href="mailto://stuart@ceng.me.uk?subject=ESP32 and Horticulture">Stuart A Spray C.Eng MIEE</a>
