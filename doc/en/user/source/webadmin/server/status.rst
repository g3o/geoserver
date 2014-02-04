.. _status:

Status
======
The Server Status page provides a summary of server configuration parameters and runtime status. It provides a useful diagnostic tool in a testing environment. 

.. figure:: ../images/server_status.png
   :align: center
   
   *Status Page*

Status Field Descriptions
-------------------------

The following table describes the current status indicators.

.. list-table::
   :widths: 30 70 

   * - **Option**
     - **Description**
   * - Locks
     - A WFS (Web Feature Service) has the ability to lock features to prevent more than one person from updating the feature at one time.  If data is locked, edits can be performed by a single WFS editor. When the edits are posted, the locks are released and features can be edited by other WFS editors. A zero in the locks field means all locks are released. If locks is non-zero, then pressing "free locks," releases all feature locks currently help by the server, and updates the field value to zero. 
   * - Connections
     - Refers to the numbers of vector stores that Geoserver was able to connect. 
   * - Memory Usage
     - The amount of RAM currently used by GeoServer. Clicking on the "Free Memory" button,  cleans up memory marked for deletion by running the garbage collector.
   * - JVM Version
     - Denotes version and vendor of the JVM (Java Virtual Machine).
   * - Native JAI
     - GeoServer uses `Java Advanced Imaging <https://jai.dev.java.net>`_ (JAI) framework for image rendering and coverage manipulation. When properly installed (true), JAI makes WCS (Web Coverage Service) and WMS (Web Mapping Service) performance faster and more efficient.
   * - Native JAI ImageIO
     - GeoServer uses `JAI Image IO <https://jai-imageio.dev.java.net>`_ (JAI) framework for raster data loading and image encoding. When properly installed (true), JAI Image I/O makes WCS and WMS performance faster and more efficient. 
   * - JAI Maximum Memory
     - Expresses in MB the amount of memory available for tile cache.
   * - JAI Memory Usage
     - Amount of memory that is used at runtime for the tile cache. Clicking on the "Free Memory" button, clears available JAI memory by running the tile cache flushing.
   * - JAI Memory Threshold
     - Refers to the percentage (0.0%-100%), of cache memory to retain during tile removal.    
   * - Number of JAI Tile Threads
     - The number of parallel threads used by scheduler to handle tiles.  
   * - JAI Tile Thread Priority
     - Schedules the global tile scheduler priority (1-10). The priority value defaults to 5.   
   * - Update Sequence
     - Refers to how often the server configuration has been modified until now.
   * - Resource cache
     - GeoServer does not cache data, but it does cache connection to stores, feature type definitions, external graphics, font definitions and CRS (Coordinate Reference System) definitions as well. The "Clear" button clears those caches and makes GeoServer reopen the stores and re-read image and font information, as well as the custom CRS definitions stored in `${GEOSERVER_DATA_DIR}/user_projections/epsg.properties`.
   * - Configuration and catalog
     - GeoServer keeps in memory all of its configuration data. If for any reason that information gets out of sync with the persisted configuration  (e.g., an external utility has modified the configuration on disk) the "Reload" button will force GeoServer to reload all of its configuration from disk.
  

Timestamps Field Descriptions
-----------------------------

.. list-table::
   :widths: 20 80 

   * - **Option**
     - **Description**
 
   * - GeoServer
     - Currently a placeholder. Refers to the day and time of current GeoServer install.
   * - Configuration
     - Currently a placeholder. Refers to the day and time of last configuration change.
   * - XML
     - Currently a placeholder. 
     
     
   
   
   
   
   
   
   
   
   
   
