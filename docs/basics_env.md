# MesoCraft Environment

Simple visual of the MesoCraft system

![](_media/MesoCraft_window.png)

The environment is based on the Qt GUI library. Individual windows can be relocated or hidden/shown. The main unit is Ångström (Å).

## Layouts

MesoCraft software functionality is separated into modules. Each module represents a set of functions relevant to the specific domain. These panels are accessible through the Widgets menu item. The user can select which panels are visible. The GUI layout can be stored via Views/Layouts/Save menu action. The layout is automatically stored into /layouts folder with the name representing the current datetime. Layout named default.json is applied automatically after the application starts.

![](_media/layout_manipulation.png)

Layouts manipulation can be done through the main menu.

## Manipulation with objects

**Left mouse** button click in the scene to select an object.
Holding **left mouse** button and moving with the mouse rotates the camera.
**Mouse wheel** performs zoom. The amount of zoom can by multiplied by holding Ctrl and/or Shift,
Using the gizmo to move (key **T**)|rotate (key **R**)|scale (key **S**) the object.

## Keyboard Shortcuts

| Key            | Action                                            |
|----------------|---------------------------------------------------|
| R              | Switches gizmo tool into Rotation mode            |
| S              | Switches gizmo tool into Scale mode               |
| T              | Switches gizmo tool into Translation mode         |
| O              | Rotates selected protein into default orientation |


## Multi-modalities rendering
## Input/Output
