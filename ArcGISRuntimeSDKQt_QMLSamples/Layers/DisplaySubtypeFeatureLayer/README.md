# Display subtype feature layer

Displays a composite layer of all the subtype values in a feature class.

![](screenshot.png)

## Use case

This is useful for controlling labeling, visibility and symbology of a given subtype as though they are distinct layers on the map.

## How to use the sample

The sample loads with the sublayer visible on the map. Toggle its visibility with the "Show sublayer" checkbox. Change the sublayer's renderer with the radio buttons, using "Show original renderer" or "Show alternative renderer", and set its minimum scale using the "Set sublayer minimum scale" button. This will set the sublayer's minimum scale to that of the current map scale. Zoom in and out to see the sublayer become visible based on its new scale range.

## How it works

1. Create a `SubtypeFeatureLayer` from a `ServiceFeatureTable` that defines a subtype, and add it to the `Map`.
2. Get a `SubtypeSublayer` from the subtype feature using its name.
3. Enable the sublayer's labels and define them with `LabelDefinitions`.
4. Set the visibility status by setting this sublayer's `visible` property.
5. Change the sublayer's symbology with `SubtypeSublayer.renderer`.
6. Update the sublayer's minimum scale value with `SubtypeSublayer.minScale`.

## Relevant API

* LabelDefinition
* ServiceFeatureTable
* SubtypeFeatureLayer
* SubtypeSublayer

## About the data

The [feature service layer](https://sampleserver7.arcgisonline.com/server/rest/services/UtilityNetwork/NapervilleElectric/FeatureServer/0) in this sample represents an electric network in Naperville, Illinois, which contains a utility network with asset classification for different devices.

## Additional information

Credentials:
* Username: viewer01
* Password: I68VGU^nMurF

## Tags

asset group, feature layer, labeling, sublayer, subtype, symbology, utility network, visible scale range
