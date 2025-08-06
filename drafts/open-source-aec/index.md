---
title: Open Source in AEC
description: Work-in-progress research about open source in architecture and engineering design tools
categories: ["topic"]
tags: ["product management", "open source", "strategy"]

---
Here are many vectors to look at open source in architecture.

1) **Tools Layer** - the applications used by designers, engineers, architects, and myriad other AEC professionals to create and modify digital representations of their work-in-progress.

2) **Component Layer** - these are the building blocks of applications: kernel, libraries of algorythms, graphics and infrastructure pipelines. For example OpenCascade and CGAL are mature and LGPL licensed.

3) **Data Layer** - how designs are represented and persisted.  These vary widely by what application and what purpose: for example, saving designs natively by an application is quite different from creating an artifact for data exchange, or sharing a drawing.  There are open interchange formats, but is this sufficient?

4) **Information Layer** - meta level for discuss aspects such as IP and ethics, for example how should project data be shared for model training and how can inference services be remunerated?

5) **Commerce Layer** - considerations of economics and market, for exmaple how are competition and cooperation balanced in fostering software ecosystems?

### Questions
As the research expands, the following questions will nest into sections corresponding to the layers above.  For now, an open-ended list will suffice:
- Why is there no open source alternative rival to Revit as Blender is to Maya? The AEC industry has favored structural lock-in, as compared to other industries like media & entertainment, game dev, and industrial design. Some combination of structural factors--regulatory demands, development cost, switching costs--have hampered the success of open kernels, standards and tools.    
- Is there sufficient institutional scaffolding for the AEC industry to create and maintain its own tools for public benefit?  Is it possible to have enough industry adoption to make a difference?  
- Can examples of open standards from other industries, such automotive, aerospace, or telecom, be instructive for AEC?  How do initiatives balance the need for collaboration against the benefits of free market competition?
- Data ownership and access and proprietary files will pale in comparison to the problem of data access through other people's APIs.
- Warehousing data also affords the holder data mining.  Autodesk's incentive for firms to use its cloud drives has morphed from selling a service to using data to train the models behind their future services. Greg S. cites knowledge capture for this reason, and good on HOK for taking this on.  Firms would share amongst eachother even if not with a commercial firm.  AEC should leverage its cohesive internal goodwill to its collective benefit.
- What do the numbers look like?  Setting aside initial development, what do the economics of maintaining and incrementally improving a mature BIM stack, when done as a funded open source project?  What are the full range of options to first build it out (buy an existing company to transform it, build it from scratch, or partner with an existing allied firm to license a baseline)?
- There's a bunch of BIM 2.0 contenders at various stages.  While not open source, competition could change the landscape.
- At each layer of the CAD onion, there are some green shoots.  For example, OpenCascade is mature and open source for non-commercial use.  Blender is mature, fully free, and generally 3D has become commoditized.  BlenderBIM is a start, but its a long way from a complete solution for modeling, documenting, annotating, and issuing drawing sets.  Everyone just uses Rhino, obviously.  The tool layer is where open BIM is lacking most.  Once designs exist, the sharing and collaboration layer is well populated: Speckle, Bluebeam, IFC, there's lots to work with depending on what you're doing.

