**INFOS**

EasySos is a quite easy-to-use and expand implementation of the OGC <a href="http://www.opengeospatial.org/standards/sos" target="_blank">Sensor Observation Service (SOS)</a>, <a href="http://www.opengeospatial.org/standards/om" target="_blank">O&M</a> and  <a href="http://www.opengeospatial.org/standards/sensorml" target="_blank">SensorML</a> specifications (a subset of SWE framework). It get to be useful for sharing observations (e.g. Open Data portals) in a standard way.

EasySos is based on the 52North database for PostgreSQL and PostGIS. I added CRUD operations by PHP YII Framework for Administrator create, read, update and delete operations. The SOS service is based on a REST service written using the PHP <a href="http://php.net/manual/en/book.xmlwriter.php" target="_blank">Xml Writer</a> library.


<BR />
**DOCUMENTATION**

1) Create the database using the file named "database.sql" using the postgis template - tested on PostgreSQL 8.3/9.0 and PostGIS 1.5

2) The best way to proceed is using the sample data provided. This stage is useful to understand easily how the system works (you can skip this stage, anyway). So, fill the database using the file "pop_izsve"

3) Put all the folders inside "htdocs" folder on Apache http server - tested on Apache 2.2 and YII 1.1.12-1.1.13

4) Open the file protected->config->main.php, find the line 'db' and insert db name, username and password to access the database

5) Open the file service->db.php and insert db name, username and password to access the database

6) Point your web browser to http://localhost/index.php

7) Create, read, update and delete data is quite easy, it needn't more training. To log in use: admin admin (you will change your password later)

8) Click on GetCapabilities, DescribeSensor or GetObservation links to display the server response metadata (just the GetObservation operation is available for now)

9) If you need, you can modify XML metadata inside service->get.php. It's just a "startElement", "writeAttribute", "endElement" matter. Refer at PHP <a href="http://php.net/manual/en/book.xmlwriter.php" target="_blank">Xml Writer</a> documentation

10) You will need to create a proper client side editing the file protected->views->site->index.php

11) Get involved in developing EasySos