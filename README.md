# Home Assistant - Solar Optimizer Solaredge - Floorplan
_This version has 24 Panels_

![Header](https://github.com/DeFlanko/hassio-package-panel-solar/blob/main/doc/Solar%20Panel.png)

I found that using Microsoft Visio was much easier to Design the layout than that of Inkscape. However _Inkscape was needed to then make the SVG_.

You can edit the SVG for your needs in Inkscape to adjust the layout. Be mindful that the text and the boxes are not grouped.

All the elements should be pre-named to match that of the yamls. (aka, it should just work)


**INSTALLATION**

1. Install the Integration [SolaredgeOptimizers](https://github.com/ProudElm/solaredgeoptimizers) <!-- omit in toc -->
   
   1a. If you get "unavialable" on any of the values -- you may need to edit the sensor.py, line 148, from 60 to 300.

2. Install the Integration [HA Floorplan](https://github.com/ExperienceLovelace/ha-floorplan) <!-- omit in toc -->

3. Copy the **pkg_panelsolar.yaml** and **secrets.yaml** file _(if it already exists copy the contents of your secrets.yaml)_ in the **"/config/packages"** folder and edit it following the instructions inside the **secrets.yaml** file.

4. In the **/www/floorplan/solar/** folder (create it if it doesn't exist) copy the **Solar_Layout.svg** file inside it and create a file with the name **panelsunpower.css** (for any CSS-type changes) 

5. In HA, create a new Dashboard (settings/dashboards "add dashboard"), open the new Dashboard created click on the 3 vertical dots at the top right to edit the Dashboard, click again on the 3 vertical dots for "Raw Configuration Editor" and copy the contents of **plan_panelsolar.yaml** file into it.
