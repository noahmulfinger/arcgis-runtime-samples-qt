# Display utility associations

Create graphics for utility associations in a utility network.

![](screenshot.png)

## Use case

Visualizing utility associations can help you to better understand trace results and the topology of your utility network. For example, connectivity associations allow you to model connectivity between two junctions that don't have geometric coincidence (are not in the same location); structural attachment associations allow you to model equipment that may be attached to structures; and containment associations allow you to model features contained within other features.

## How to use the sample

Pan and zoom around the map. Observe graphics that show utility associations between junctions.

## How it works

1. Create and load a `UtilityNetwork` with a feature service URL.
2. Add a `FeatureLayer` to the map for every `UtilityNetworkSource` of type `Edge` or `Junction`.
3. Create a `GraphicsOverlay` for the utility associations.
4. Add connection for the `ViewpointChanged` signal of the `MapView`.
5. When the sample starts and every time the viewpoint changes, do the following steps.
6. Get the geometry of the mapview's extent using `currentViewpointExtent.extent`.
7. Get the associations that are within the current extent using `associationsWithEnvelope(extent)`.
8. Get the `UtilityAssociationType` for each association.
9. Create a `Graphic` using the `Geometry` property of the association and a preferred symbol.
10. Add the graphic to the graphics overlay.

## Relevant API

* GraphicsOverlay
* UtilityAssociation
* UtilityAssociationType
* UtilityNetwork

## About the data

The [feature service](https://sampleserver7.arcgisonline.com/server/rest/services/UtilityNetwork/NapervilleElectric/FeatureServer) in this sample represents an electric network in Naperville, Illinois, which contains a utility network used to run the subnetwork-based trace.

## Additional information

Credentials:
* Username: viewer01
* Password: I68VGU^nMurF

## Tags

associating, association, attachment, connectivity, containment, relationships

