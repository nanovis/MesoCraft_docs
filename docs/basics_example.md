# Examples of rules

In this chapter several examples are presented. These examples are to present the capabilities of the system. It is important to understand that these rules can be combined (where it makes sense) as this forms the strength of the system.

## Parent-child relative rule

This rule is used the bind an element to a proxy geometry – skeleton. Firstly, a skeleton and an instance need to be inserted into the scene. In the following example, a pentagonal skeleton and a protein instance (md.pdb) are presented.

![](_media/rules/parent-child_relative_rule.png ':size=50%')

After selecting the protein instance by mouse a moving it to the desired position in the proximity of the skeleton, the rule can be created. To create ***Parent-child (relative)*** rule, select the respective option in the ***Modeling menu*** and click on the ***Create Rule*** button. The relative position of the protein instance to the closest skeleton vertex is stored. This position is in the later phase replicated for selected amount of vertices of the skeleton.

![](_media/rules/parent-child_relative_rule2.png ':size=50%')

By default, the amount of elements when creating ***Parent-child (relative)*** rule is set to ***0***. To increase this amount go to the ***Edit dialog*** and change ***Max number of elements*** parameter.

![](_media/rules/parent-child_relative_rule3.png ':size=50%')

After applying the rule, the result should look like:

![](_media/rules/parent-child_relative_rule4.png ':size=50%')


## Parent-child distance rule

This rule is used for populating elements in the defined distance to the skeleton.

![](_media/rules/parent-child_distance_rule.png ':size=80%')

### Distances

At the rule definition phase, the exact distance to the skeleton is stored. This distance can be customized (by adding a standard deviation) in the ***Edit Rule*** dialog in the ***Distance Tab***. By selecting the green point with (*mouse left button* and moving) in the ***Distance Tab***, the user can adjust the distance. Using the *right mouse button* and moving the user can adjust the standard deviation.

![](_media/rules/parent-child_distance_rule1.png ':size=80%')


### Angle distribution

The user can specify (constrain) the areas where elements are being populated using the Angle distribution feature. In the ***Positions tabpage***, using the *left mouse button*, the user can draw in which regions the elements will be populated. The map represents spherical coordinates (longitude, latitude). Using the *right mouse button*, a portion of the painted path can be removed.

![](_media/rules/parent-child_distance_rule2.png ':size=80%')

?> Notice: Angle distribution is implemented so far only for the Distance rule!

## Siblings rule

Siblings rule is created to model the relationship between two elements. Rotation and translation are stored. The rule finds all relevant elements in the scene on which it can be applied. If some instances are selected, the rule is applied only on those.

![](_media/rules/siblings_rule.png ':size=80%')

The example of application the very same rule on two elements. First, they are in a row. Second, they are placed randomly in the scene.

![](_media/rules/siblings_rule1.png ':size=80%')

## Siblings-parent rule

![](_media/rules/siblings-parent_rule.png ':size=80%')

## Connection rule

Connection rule is used to create a polyline. There are currently two modes of the connection rule.

![](_media/rules/connection_rule.png ':size=80%')

### Creating one curve

By selecting an element, the user specifies a type. Then, all elements in the scene of this type are selected. The resulting curve (polyline) connects these points. 

Remark: the algorithm that searches for the connection does not necessarily uses all the points (< 10 can be not connected).

![](_media/rules/connection_rule_curve.png ':size=80%')

### Creating set of connections

By selecting two elements, the user specifies two types. Then, pairs of these types are identified in the scene and connected. Every type is on the different end of the curve (polyline). The length (0 for default) and type (Line, PolyLine, Curve) of the curve can be specified.

![](_media/rules/connection_rule_set_of_connections.png ':size=80%')

## Fill rule

Using Fill rule elements can be populated inside the 3D skeleton (box, icosahedron, custom triangle mesh). The number of elements can be modified in the ***Edit Rule*** dialog (30 by default)

![](_media/rules/fill_rule.png ':size=80%')


## Measurement

The distance between two elements can be measured by selecting both of the elements and clicking the ***Distance*** button in ***Alignment->Measurement*** groupbox. Additional measuring line tool is added into the scene. The tool is updated every time a respective element is moved. To measure the angle, three elements need to be selected following hitting the ***Angle*** button. The all measurement tools can be removed by hitting the ***Clear*** button.

![](_media/measurement.png ':size=80%')