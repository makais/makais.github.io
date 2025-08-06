---
title: "MicroStation 3D Modeling Tools"
description: "Design of a new parametric solids modeling system"
categories: ["project"]
tags: ["parametric modeling", "design tools", "product management", "2012"]
cover:
    image: parametric-bridge-sections-cover.jpg
    alt: Drawings of parametric bridge sections
    relative: true
---

A comprehensive set of Parasolid-based 3D solid modeling tools was created, leveraging D-Cubed 2D and 3D solvers.  I oversaw the modeling system's design, development, and testing, as well running go-to-market with beta user community, creating content, and supporting user events.

- Dimension-driven constraints for 2D sketches and 3D assemblies
- Works on all elements in the design file
- A design a system for parametric cells and templated placement
- Variables and parameters system
- In-model manipulation, precise input, integration with Accudraw and snapping

{{<figure src="parametric-bridge-section.jpg" alt="Screenshot of MicroStation CONNECT Edition showing parametric 2D bridge section drawing" title="Constraints and variables" caption="Driving key parameters through variables allows creation of reusable parametric components.">}}

Before the new tools, MicroStation had two completely separate 3D modeling toolkits: one that was conventional 3D modeling, and one called Feature Modelling, a comprehensive but archaic set of parametric 3d solids with its own sketcher (folded back into MicroStation after the cancellation of the stand-alone MicroStation Modeler product). We produced a new, unified set of tools, making them seamlessly integrated within the core of MicroStation.

{{<figure src="bridge-section-extrusion.jpg" alt="3D model of a concrete bridge piece" title="Parametric solids" caption="The tree of modeling operations is retained, so profiles for operations such as this extrusion remain editable.">}}

We continued the project, extending development of history-aware parametric modeling to NURBS curves and surfaces, to allow real-time trimming and editing of the underlying profile curves.  The 3D modeling tools we developed remain the current core system in Bentley MicroStation used globally by AEC users.

