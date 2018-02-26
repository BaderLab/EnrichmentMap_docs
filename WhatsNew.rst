What's New
==========

EnrichmentMap 3.1
-----------------

* Redesigned Post-Analysis UI

  * Ability to preview signature gene sets before import
  * Ability to import GMT files from the web (download.baderlab.org)

* New Chart: Color by DataSet.
* Support for `g:profiler` 2-phenotype analysis.
* Heat Map: Compress expressions by class.
* Export Legend to PDF.
* Export Heat Map to PDF.
* Ability to specify the name of the EnrichmentMap network.
* Drag-and-Drop folders onto the Create EnrichmentMap Dialog.
* `Several bug fixes <https://github.com/BaderLab/EnrichmentMapApp/milestone/7?closed=1>`_
* Requires Cytoscape 3.5.1


EnrichmentMap 3.0
-----------------

EnrichmentMap 3.0 is a major release, with the following new features:

* EnrichmentMap networks can now be created from any number of enrichment data sets 
  (EnrichmentMap 2.0 supported maximum 2 data sets).
* New chart visualizations on nodes for visualizing NES scores, p-values or q-values. 
  Three new charts are available: radial heat-map, linear heat-map and heat-strips.
* New network creation dialog has the ability to scan a folder for files belonging to each dataset. 
  In most cases this removes the need to manually enter the required files.
* New control panel allows the contents and style of the network and charts to be updated 
  dynamically.
* New legend dialog.
* New streamlined HeatMap panel has the ability to summarize expression data.
* Several new commands that allow EnrichmentMap to be automated from external scripts and CyREST.
* `Several bug fixes <https://github.com/BaderLab/EnrichmentMapApp/milestone/6?closed=1>`_
* Requires Cytoscape 3.4
