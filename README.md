# wynncraft-GPS

wynncraft GPS for map coordinate

## install 
move .\gps  $pshome\modules
md c:\ex-sys
move .\xml c:\ex-sys

# sync:
add-place -wynncraft_place ;-teleportation_place; -survival_place ;-road

find-place -wynncraft_place -mycoordinate;-teleportation_place -mycoordinate;-survival_place -mycoordinate;-road

road -mycoordinate

teleportation-route -destination

road-route  -destination -dimention

search-place -wynncraft_place -mycoordinate;-teleportation_place -mycoordinate;-survival_place -mycoordinate;-road
# help 
get-help -name [name]
