# Florida Rocket Lab — New Member Project

Andrew McGuigan | Vehicle Engineering | Fall 2026

Ongoing rocket design and analysis project for Florida Rocket Lab at the University of Florida. The project targets a 3,000 m apogee and covers vehicle configuration, flight modeling, thrust structure, recovery, and air-brake design.

## Deliverable 1 — Flight modeling

- [OpenRocket design](McGuiganA_Deliverable1/Deliverable1_RocketDesign.ork): rocket configuration and flight simulation.
- [Euler calculator](McGuiganA_Deliverable1/Euler%20Calculator.xlsx): Excel model predicting apogee and maximum dynamic pressure using Euler's method.
- [Model comparison](McGuiganA_Deliverable1/Euler-OpenRocket%20Comparison.pdf): results, plots, assumptions, and discussion of differences between the models.

| Quantity | Excel model | OpenRocket | Difference |
| --- | ---: | ---: | ---: |
| Apogee | 3,588.962 m | 3,341.552 m | 7.40% |
| Maximum dynamic pressure | 90.567 kPa | 79.990 kPa | 13.22% |

These are predicted results, not flight-test measurements. The Excel model uses an ascent-only, vertical-flight approximation with zero wind and a constant drag coefficient.

## Upcoming work

- Interface requirements and subsystem trade studies
- Air-brake mechanism, recovery system, and thrust structure CAD and load analysis
- Integrated vehicle design, bill of materials, test plans, and preliminary design review

Additional deliverables will be added as the project progresses. Original deliverable folders and filenames are retained for traceability.

## Opening the files

Use OpenRocket for `.ork` files, Microsoft Excel for `.xlsx` files, and a PDF reader for the report.
