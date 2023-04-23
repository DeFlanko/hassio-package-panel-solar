# Home Assistant - Solar Optimizer Solaredge - Floorplan
_This version has 24 Panels_

![Header](https://github.com/DeFlanko/hassio-package-panel-solar/blob/main/doc/Solar%20Panel.png)

# **Author Notes**
I found that using Microsoft Visio was much easier to design the layout than that of Inkscape. 

However _**Inkscape was needed to then make the SVG**_.

You can edit the ```Solar_Layout.svg``` in Inkscape for your layout needs. Be mindful that the text and the boxes are not grouped.

However, all the elements should be pre-named to match that of the yamls. (aka, it should just work)

The Origional repo was in italian so I spent the effort in converting that to English -- please open any issues if you find anything that needs to be translated. 

# **Installation Steps**

1. Install the Integration [SolaredgeOptimizers](https://github.com/ProudElm/solaredgeoptimizers) <!-- omit in toc -->
   
   1a. If you get "unavialable" on any of the values -- you may need to edit the ```sensor.py```, [from 60 to 300](https://github.com/ProudElm/solaredgeoptimizers/issues/47).

2. Install the Integration [HA Floorplan](https://github.com/ExperienceLovelace/ha-floorplan) <!-- omit in toc -->

3. Copy the ```pkg_panelsolar.yaml``` and ```secrets.yaml``` file _(if it already exists copy the contents of your secrets.yaml)_ in the ```"/config/packages"``` folder and edit it following the instructions inside the ```secrets.yaml``` file.

4. In the ```/www/floorplan/solar/``` folder (create it if it doesn't exist) copy the ```Solar_Layout.svg``` file inside it and create a file with the name ```panelsunpower.css``` (for any CSS-type changes) 

5. In HA, create a new Dashboard (settings/dashboards "add dashboard"), open the new Dashboard created click on the 3 vertical dots at the top right to edit the Dashboard, click again on the 3 vertical dots for "Raw Configuration Editor" and copy the contents of ```plan_panelsolar.yaml``` file into it.

# **Post Edits**

1. Your SolarEdge panel numbers will vary from these install files. 
   
   a. For example, mine started at ```sensor.power_1_0_25``` because the previous 24 panels module devices were swapped out with new ones -- Tesla failed to update the SolaarEdge site (its odd, i know) -- Edit the entities in the ```plan_panelsolar.ymal``` accordingly.

2. Edit the ```Solar_Layout.svg``` in Inkscape to preserve the meta data elements and have the visual layout to match yours. 