# Model file format specification

One of the possible outputs of MesoCraft is .model file format. This file contains information about the current model and it’s hierarchy. The description of the file format follows. 

Model file format is a mixed JSON text header and binary data file. The first 4 bytes specify the length of the JSON information (metadata describing the model). Following these 4 bytes, JSON is stored, following by the binary data (12*4 bytes per instance). The instance binary data represents one instance of structure loaded from a PDB in the scene. PDB files are not part of the file and are expected to be parsed separately and centered to the origin before application of transformations from .model file. Overall file structure can be seen in the following schematic drawing.

![](_media/format/model_format_specs.png ':size=80%')

## JSON specification (v. 1)

JSON header contains information about the number of elements of the model, their referencing PDB etc. The description follows:

The root node contains the amount of element (`count` - parameter necessary for parsing the binary data), name of the model and further metadata about the elements.

![](_media/format/json_specs.png ':size=80%')

In the *elements* array, metadata regarding every type (not instance!) are included. There are two main types of elements - *protein* and *model*. In the case of *protein* type, there is an attribute *pdb* this type refers to. 

![](_media/format/json_specs1.png ':size=80%')

## Binary instance info

Is formed by 48 bytes data chunk with the following layout:

![](_media/format/binary_instance_info.png ':size=80%')

Parameters:

- **index** - reference to the index field in the element node in the JSON metadata (can be understood as type id)

- **position** - 3D vector

- **rotation** - specified as a quaternion

- **id** - unique identifier of the instance of the given type. Thus, proteins and models have both unique number sequence (i.e. there might exist a protein and a model with the similar id - the type needs to be taken into account while parsing the file)

- **parent id** - id of a parent. Parent is always of type model (i.e. a parent cannot be a protein).
