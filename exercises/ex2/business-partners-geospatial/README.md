
# Apply Geo Spatial on _Business Partners_ View
In this exercise we will apply Geo Spatial configuration on the view _**V_BUSINESS_PARTNERS**_. 

1. Navigate to the Repository Explorer
2. Search and edit the view _**V_BUSINESS_PARTNERS**_
  <br><br>![](../images/create_business_partner_geospatial_01.png)

3. Select the *Projection Node* and add a new **Calculation Node** from the context menu
  <br><br>![](../images/create_business_partner_geospatial_02.png)
4. Add a new **Geo-Coordinates Column**.
  <br><br>![](../images/create_business_partner_geospatial_03.png)
5. Adjust the Calculated Column as following:
    - Business Name: **LOCATION**
    - Technical Name: **LOCATION**
    - Data Type: **hana.ST_GEOMETRY
    - Spatial Reference Identifier: **4326**
    - Latitude: **LATITUDE**
    - Longitude: **LONGITUDE** 
  <br><br>![](../images/create_business_partner_geospatial_04.png)

6. Click on <b>Deploy</b> button to deploy the view
  <br><br>![](../images/create_business_partner_geospatial_05.png)
