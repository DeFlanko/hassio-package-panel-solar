# Package Panel Solar Optimizer Solaredge Home-Assistant 
_This version has 24 Panels_

![Header](https://github.com/DeFlanko/hassio-package-panel-solar/blob/main/svg/Solar_Layout.svg)

**INSTALLATION**

1. copy the **pkg_panelsolar.yaml** and **secrets.yaml** file _(if it already exists copy the contents of your sectrets.yaml)_ in the **"/config/packages"** folder and edit it following the instructions inside the **secrets.yaml** file.

2. install the Integration [SolaredgeOptimizers](https://github.com/ProudElm/solaredgeoptimizers) <!-- omit in toc -->

3. install the Integration [HA Floorplan](https://github.com/ExperienceLovelace/ha-floorplan) <!-- omit in toc -->

4. in the **/www/floorplan/solar/** folder (create it if it doesn't exist) copy the **Solar_Layout.svg** file inside it and create a file with the name **panelsunpower.css** (for any CSS-type changes) 

5. in HA create a new Dashboard (settings/dashboards "add dashboard"), open the new Dashboard created click on the 3 vertical dots at the top right to edit the Dashboard, click again on the 3 vertical dots for textual configuration editor and copy the **plan_panelsolar.yaml** file into it
