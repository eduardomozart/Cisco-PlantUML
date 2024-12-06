# CiscoCVD-PlantUML

This repository uses [Cisco Validated Design 3D Stencils](https://www.petenetlive.com/KB/Article/0001041) (Cisco_CVD_icons_png.zip) from Cisco.

The following projects were used to generate the images available in this repository:

* [libvisio2svg](https://github.com/kakwa/libvisio2svg) to convert Visio Stencils (*.vss) to SVG.
* Inkscape to convert SVG to PNG.
* ImageMagick to remove background alpha transparency from PNG files.
* PlantUML to convert white background PNGs to Sprites (.puml files). 

The scripts used to generate the images available in this repository are available in the post "[Instalação do libvisio2svg no macOS](https://eduardomozartdeoliveira.wordpress.com/2023/01/30/instalacao-do-libvisio2svg-no-macos/)" (in Portuguese).

## Getting Started

### Switches

![Basic usage - VSF](https://www.plantuml.com/plantuml/proxy?idx=0&src=https%3A%2F%2Fraw.githubusercontent.com%2Feduardomozart%2FCiscoCVD-PlantUML%2Fmain%2FSamples%2FSwitches.puml)

```csharp
@startuml
skinparam nodesep 150
skinparam defaultTextAlignment center
skinparam sequenceArrowThickness 1.5
skinparam rectangleRoundCorner 0

<style>
rectangle {
  LineColor transparent
  BackgroundColor transparent
  MinimumWidth 100
}
</style>

!define CiscoCVDPuml https://raw.githubusercontent.com/eduardomozart/Cisco-PlantUML/main
!include CiscoCVDPuml/puml/Layer_2_Switch.puml
!include CiscoCVDPuml/puml/Layer_3_Switch.puml

rectangle "<color:#121c22><$Layer_3_Switch>\n<b>Core" as SW1
rectangle "<color:#121c22><$Layer_2_Switch>\n<b>SW2" as SW2
rectangle "<color:#121c22><$Layer_2_Switch>\n<b>SW3" as SW3

SW1 --> SW2
SW1 --> SW3
@enduml
```
