Is this sufficient?:
```
GET /visualization/?vis=igv&genome=hg38&uuid[]=1234&uuid[]=4567
returns HTML, and makes sure the docker instance which provides hierarchical clustering is available?
```
or do we need another layer?:
```
GET /api/visualization/?vis=igv&genome=hg38&uuid[]=1234&uuid[]=4567
returns {url: "/visualization/?vis=igv&genome=hg38&uuid[]=1234&uuid[]=4567"}
```
or will the argument structure be complex enough that we would want to pass JSON?

If there are extra servers which need to be started, or the visualization will not be immediately available
the API makes sense, but in some cases if may just be a thin wrapper.

If there are extra servers which need to be started, then the action is really more than a GET,
and there may not be a sharable link to the visualization itself?


### INPUTS:
1. **Files:**
  * Datafiles:
    * Flat list of UUIDs
    * or file paths / URLS?
    * Either approach could check file types... but I think that might be better left to the client downstream.
  * Tool-Specific Config Files (gene model, list of adapters):
  * Data Specific Config Files (sample grouping)
    * None
2. **Parameters:**
  * Tool-Specific:
    * none?
  * Instance-Specific:
    * genome build
    * list of columns to build track names from...
    * or specify datafiles along with custom names for each? 
  * Dataset Specific:
    * none?
    
### OUTPUTS:
1. **Files:**
  * None
2. **Status:**
  * NA?
3. **State:** (For Vizualization Tools)
  * URL which provides visualization
