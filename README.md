# Florida Rocket Lab — New Member Project

Andrew McGuigan | Vehicle Engineering | Fall 2026

Rocket design and analysis project for Florida Rocket Lab at the University of Florida. The project targets a 3,000 m apogee and covers vehicle configuration, flight modeling, thrust structure, recovery, and air-brake design.

## Preliminary Design Review (Group 2)

- [PDR presentation](Group2_PDR/GROUP%202%20PDR.pdf): 107-slide deck covering the thrust structure, recovery, airbrakes, and aerodynamics, with an appendix holding the bill of materials and all hand calculations.

Group 2 is a 4-person team: Andrew McGuigan, David Chertok, Cooper Boris, and Helen Garcia. I designed the thrust structure, recovery, and airbrakes subsystems.

**Vehicle:** CTI K1440 motor (54 mm, 1,828.9 N peak thrust, 2,372 N·s), 76.2 mm fiberglass airframe, 6.98 kg liftoff mass, thrust-to-weight ratio of 21.

**Thrust structure**
- Uses two independent load paths: a J-B Weld bond and 12 G10 fiberglass pins. Each one carries the full peak thrust by itself (bond FOS 8.2, pins FOS 5.3).
- Uses a G12 fiberglass motor tube held by three birch plywood centering rings. The lowest factor of safety is 2.55, from airframe Euler buckling, against a 2.0 requirement.
- Design changes made from analysis:
  - Plywood pins became G10 rod, raising pin shear FOS from 0.4 to 25.
  - A third centering ring cut the unsupported tube span from 530 mm to 259 mm.
  - A bond-line thermal check led to using J-B Weld (rated to 260 °C) on every bond near the motor.

**Recovery:** Dual deploy, with a drogue at apogee and the main near the ground. Both descent rates fall inside the FAR-OUT limits. The deck also covers parachute trade studies, opening and snatch loads, a link load check, black powder charge sizing, and bulkhead checks.

**Airbrakes:** Four panels run off a single crank, so drag stays symmetric, and a stepper motor drives the crank. The peak retract torque is 1.07 N·m against the 3.95 N·m the motor and gearbox can supply (FOS 3.9). The deck also covers the panel loads, linkage kinematics, and mounting.

**Aerodynamics:** Clipped delta fins with a semispan sized in MATLAB from Barrowman's equations, giving 1.58 calibers of stability in OpenRocket. Also flutter checks, nose cone selection, and a drag build-up compared against CFD.

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

- Guidance, navigation, and control (GNC) and the air-brake control law
- Critical design review, test plans, and fabrication

Additional deliverables will be added as the project progresses. Original deliverable folders and filenames are retained for traceability.

## Opening the files

Use OpenRocket for `.ork` files, Microsoft Excel for `.xlsx` files, and a PDF reader for the reports.
