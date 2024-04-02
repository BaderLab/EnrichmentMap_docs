What's New
==========

Release Notes
-------------

New in EnrichmentMap 3.4
~~~~~~~~~~~~~~~~~~~~~~~~

* New column, style mapping and chart for -log10(pvalue).
* Better support for latest version of AutoAnnotate.
* Default layout is now yFiles organic layout.
* UI changes to the EnrichmentMap create dialog.
* Bug fixes.


New in EnrichmentMap 3.3.5
~~~~~~~~~~~~~~~~~~~~~~~~~~

* Better support for AutoAnnotate summary networks. They now work with the Heat Map panel.
* 'enrichmentmap mastermap' command now has an argument for the GREAT filter.
* Bug fixes.


New in EnrichmentMap 3.3.4
~~~~~~~~~~~~~~~~~~~~~~~~~~

* Created an options menu next to the Data Set list and moved all the buttons that used to be next to the Data Set list into this menu.
* Added ability to synchronize data set list with network selection.
* Creating a subnetwork from an EnrichmentMap network will copy the EnrichmentMap data to the subnetwork.
* Bug fixes.


New in EnrichmentMap 3.3
~~~~~~~~~~~~~~~~~~~~~~~~

* An EnrichmentMap network can now be created from a STRING or GeneMania network.
* The colors used in the 'Color by DataSet' chart can be customized.
* It is no longer a strict error when gene sets are missing from the GMT file. The user may 
  choose to continue to create the network without the missing gene sets.
* The Heat Map panel can sort ranks automatically based on the leading edge.
* The Heat Map panel can filter Data Sets based on node/edge selection.
* The "Color by DataSet" chart is now filtered based on the selected Data Sets.
* Support for importing Enrichr files when creating an EnrichmentMap netwwork.
* New 'Create Command' button in the Create EnrichmentMap Dialog shows equivalent command for automation.
* Bug Fixes


New in EnrichmentMap 3.2
~~~~~~~~~~~~~~~~~~~~~~~~

* Requires Cytoscape 3.7
* Integration with other analysis tools:

  * GeneMania
  * STRING
  * Pathway Commons

* New commands for automating EnrichmentMap through CyREST.

  * Export PDF
  * Set chart options
  * Show abd hide datasets
  * Create an EM network from data in a table

* Column names are now prefixed with "EnrichmentMap::" to take advantage of
  the column namespace feature added to Cytoscape 3.7.
* `Bug fixes <https://github.com/BaderLab/EnrichmentMapApp/milestone/8?closed=1>`_


New in EnrichmentMap 3.1
~~~~~~~~~~~~~~~~~~~~~~~~

* Requires Cytoscape 3.5.1
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
* `Bug fixes <https://github.com/BaderLab/EnrichmentMapApp/milestone/7?closed=1>`_


New in EnrichmentMap 3.0
~~~~~~~~~~~~~~~~~~~~~~~~

EnrichmentMap 3.0 is a major release, with the following new features:

* Requires Cytoscape 3.4
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
* `Bug fixes <https://github.com/BaderLab/EnrichmentMapApp/milestone/6?closed=1>`_
