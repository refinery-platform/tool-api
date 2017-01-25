Is this sufficient?:
```
GET /visualization/?vis=heatmap-scatterplot&uuid=1234&format=tsv
(or could have the client guess the format?)
(or could support visualizing multiple files at once, assuming they have the same columns?)
returns HTML, and makes sure the docker instance which provides hierarchical clustering is available?
(though having a GET potentially start a server seems excessive)
```
or do we need another layer?:
```
GET /api/visualization/?vis=heatmap-scatterplot&uuid=1234
returns {url: "/visualization/?vis=heatmap-scatterplot&uuid=1234"}
```
or will the argument structure be complex enough that we would want to pass JSON?
```
POST ...
```

If there are extra servers which need to be started, then the action is really more than a GET,
and there may not be a sharable link to the visualization itself?

Here, there might be a docker container that spins up for clustering, but we don't need to wait on that for
the initial load. What does "status" mean, and who uses it?

### INPUTS:
1. **Files:**
  * Datafiles:
    * Flat list of UUIDs
    * or file paths / URLS?
    * Either approach could check file types... but I think that might be better left to the client downstream.
  * Tool-Specific Config Files (gene model, list of adapters):
    * None
  * Data Specific Config Files (sample grouping)
    * None
2. **Parameters:**
  * Tool-Specific:
    * none?
  * Instance-Specific:
    * none?
  * Dataset Specific:
    * none?
    
### OUTPUTS:
1. **Files:**
  * None
2. **Status:**
  * NA?
3. **State:** (For Vizualization Tools)
  * URL which provides visualization
  * URL for docker instance, which might not yet be available
