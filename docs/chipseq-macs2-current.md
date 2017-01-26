### INPUTS:
1. **Files:**
  * Datafiles:
    * paired input: 2x FastQ files
  * Tool-Specific Config Files (gene model, list of adapters):
    * Dataset Specific
    * User/Instance Specific
  * Data Specific Config Files (sample grouping)
2. **Parameters:**
  * Defined by tool:
    * Allowed values: boolean, integer, etc.
  * Defined by Refinery instance:
    * Allowed values: ("runtime") e.g. genome build, genome index files
  * Defined by dataset:
    * Allowed values: e.g. "Select one or more attributes to use as tool labels"
    
### OUTPUTS:
1. **Files:**
  * Description, Name, Type
    * `MACS2_bed`: Tabular file
    * `MACS2_plot`: PDF file
    * `MACS2_bigwig`: BigWIG file
2. **Status:**
  * `RUNNING`, `FAILED`, `SUCCESS`
3. **State:** (For Vizualization Tools)
