UnitySlippyMap
==============

A slippy map implementation written in C# for Unity3D.

It aims at helping developpers create 2D/3D maps working with a variety of online tile providers (OpenStreetMap, GoogleMaps, Yahoo! Maps, Bing Maps, ...) and offline sources (DBMap, MBTiles, ...) like [Route-me](https://github.com/route-me/route-me) (iOS) or [Leaflet](http://leaflet.cloudmade.com/) (HTML5), on every platform supported by Unity3D.

Hopefully, it will also be compliant with a number of popular [OGC](http://www.opengeospatial.org/) standards like WMS or GML.

Map objects (tiles, markers, ...) are placed in 3D space along X and Z axis. The idea is to be able to use 3D geometry as terrain or markers with a free camera.

Current status
--------------

UnitySlippyMap is in early alpha stage and currently supports [OSM tiles](http://wiki.openstreetmap.org/wiki/Slippy_map_tilenames) from providers such as [OpenStreetMap](http://www.openstreetmap.org/), [MapQuest](http://www.mapquest.com/) or [CloudMade](http://cloudmade.com/).

It is tested in Unity3D Editor, and on iOS and Android devices.

See the [TODO list](/jderrough/UnitySlippyMap#todo) if you want to contribute and don't know where to start.

License
-------

UnitySplippyMap is released under the [LGPL 3.0](http://www.gnu.org/licenses/lgpl.html).

TODO
----

Here is a short list of what could be fixed or added to UnitySlippyMap:

* Fix the voodooish way I implemented the camera elevation and tile positioning (see the comments in Map.cs)
* Handle device orientations properly when using the compass
* Add support for well known tile providers (derive from TileLayer.cs)
* Add new map objects (polygons, lines, ...)
* Add support for marker billboarding
* Add support for orthographic cameras
* Add a better zoom rounding (>80%, <20%?)
* Add a map constraint to a given 'size', bounce on limits
* Add movements inertia
* Implement inputs in a user oriented customizable way

* Optimise, use one material for the tiles to enable dynamic batching: tried and failed, merging textures on the fly is to costly (see TextureAtlasManager.cs)
