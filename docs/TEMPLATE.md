### INPUTS:
1. **Files:**
  * Datafiles:
    * Grouping/relationships: (single/pairs)
    * File format/type
  * Tool-Specific Config Files (gene model, list of adapters):
    * Dataset Specific
    * User/Instance Specific
  * Data Specific Config Files (sample grouping)
2. **Parameters:**
  * Tool-Specific:
    * Allowed values: boolean, integer, etc.
  * Instance-Specific:
    * Allowed values: ("runtime") e.g. genome build, genome index files
  * Dataset Specific:
    * Allowed values: e.g. "Select one or more attributes to use as tool labels"
    
### OUTPUTS:
1. **Files:**
  * Description, Name, Type
2. **Status:**
  * `RUNNING`, `FAILED`, `SUCCESS`
3. **State:** (For Vizualization Tools)
