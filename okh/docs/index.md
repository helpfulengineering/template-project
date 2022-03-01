# Welcome to MkDocs

For full documentation visit [mkdocs.org](https://www.mkdocs.org).

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml      # The configuration file.
    docs/
        index.md    # The documentation homepage.
        about.md    # Context for this project
        

## Project Outline

#### Design Files
```
Fieldname: design-files
Purpose: Storage for design files such as CAD and vector files.
Reference:
    design-files:
    - path: /design-files       # Relative path from root of repo directory
        title: [string]         # filename, separated by commas if more than one
        format: [string]        # file extension and required software (if any)

Rules: Optional

Comments: The manifest may refer to URL where these files are stored, in which case this directory can be left empty.
```

#### Schematics
```
Fieldname: schematics
Purpose: Storage for schematics, wiring diagrams, and all other engineering drawings.
Reference:
    schematics:
    - path: /schematics      # Relative path from root of repo directory
        title: [string]      # filename, separated by commas if more than one
        format: [string]     # file extension and required software (if any)

Rules: Optional

Comments: 
```

#### Bill of Materials
```
Fieldname: bom
Purpose: Spreadsheet containing exhaustive list of all parts, components, products and materials needed to fully assemble the design.
Reference:
    bom:
    - path: /bom             # Relative path from root of repo directory
        title: [string]      # filename

Rules: Required

Comments: 

[notes] Should provide a template spreadsheet with template repo
```

#### Tool List
```
Fieldname: tool-list
Purpose: Document containing list of all tools required to manufacture and assemble the design.
Reference:
    tool-list:
    - path: /tool-list       # Relative path from root of repo directory
        title: [string]      # filename

Rules: Required

Comments: 
```

#### Making Instructions
```
Fieldname: making-instructions
Purpose: Documents detailing fabrication and assembly of design. 
Reference:
    making-instructions:
    - path: /making-instructions    # Relative path from root of repo directory
        title: [string]             # filename for main instruction document
        images: [path]              # relative path to folder where reference images are stored [Optional]
        video-URL: [string]         # link to video detailing assembly process. [Optional]

Rules: Required

Comments: May include written documents, images, or video. 
Video files should NOT be stored locally in this repo. 
Video files can be linked to from the main manifest.
```

#### Manufacturing Files
```
Fieldname: manufacturing-files
Purpose: Storage for files for digital fabrication.
Reference:
    manufacturing-files:
    - path: /manufacturing-files      # Relative path from root of repo directory
        title: [string]               # filename, separated by commas if more than one
        format: [string]              # file extension and required software (if any)

Rules: Optional

Comments: This is where you put any G-Code, STL files, anything meant to feed into CNC machines, 3d printers, etc.
```

#### Risk Assessment
```
Fieldname: risk-assessment
Purpose: Document detailing any known safety risks or hazards.
Reference:
    schematics:
    - path: /schematics      # Relative path from root of repo directory
        title: [string]      # filename, separated by commas if more than one
        format: [string]     # file extension and required software (if any)

Rules: Recommended but not required. 

Comments: Risk assessment may pertain to any or all of the following points in the objects lifecycle:
 - assembly
 - operation
 - maintenance
 - disposal
 - storage
```

#### Tool Settings
```
Fieldname: tool-settings
Purpose: Document detailing configuration and calibration settings for the tools described in tool-list.
Reference:
    tool-settings:
    - path: /tool-settings   # Relative path from root of repo directory
        title: [string]      # filename

Rules: Optional 

Comments: For any tool-list containing CNC machines, 3D printers, laser cutters or other computer controled tooling, tool-settings is also required. 
```

#### Quality Instructions
```
Fieldname: quality-instructions
Purpose: Document detailing quality control and testing for the design.
Reference:
    quality-instructions:
    - path: /quality-instructions   # Relative path from root of repo directory
        title: [string]             # filename, separated by commas if more than one

Rules: Optional

Comments: 
```

#### Operating Instructions
```
Fieldname: operating-instructions
Purpose: Document detailing operating procedures for the design.
Reference:
    operating-instructions:
    - path: /operating-instructions     # Relative path from root of repo directory
        title: [string]                 # filename, separated by commas if more than one

Rules: Required

Comments: Never assume operation is self-evident.
```

#### Maintenance Instructions
```
Fieldname: maintenance-instructions
Purpose: Document detailing maintenance and cleaning procedures for the design.
Reference:
    maintenance-instructions:
    - path: /maintenance-instructions   # Relative path from root of repo directory
        title: [string]                 # filename, separated by commas if more than one

Rules: Optional

Comments: 
```

#### Disposal Instructions
```
Fieldname: disposal-instructions
Purpose: Document detailing proper and safe disposal of design when broken or decommissioned. 
Reference:
    disposal-instructions:
    - path: /disposal-instructions      # Relative path from root of repo directory
        title: [string]                 # filename, separated by commas if more than one

Rules: Optional

Comments: 
```

#### Software
```
Fieldname: software
Purpose: Repository for all code required to operate the design.
Reference:
    software:
    - path: /software        # Relative path from root of repo directory

Rules: Optional

Comments: 
```
