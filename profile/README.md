# iCorrVision

Open-source digital image correlation (DIC) software, a project of the [Department of Mechanical and Industrial Engineering](https://www.demi.fct.unl.pt/en) (DEMI) at [NOVA School of Science and Technology](https://www.fct.unl.pt/en) (NOVA FCT).

iCorrVision version 2 (2026) is a new implementation that shares no code with version 1 and separates the correlation engine from the interface. It began as the MSc thesis *iCorrVision 2.0: Development and Metrological Assessment of Modular Software for Two-Dimensional Digital Image Correlation* (João Pedro da Silva Duarte Récio, NOVA FCT, 2026), supervised by José Manuel Cardoso Xavier.

| Repository | What it is |
| --- | --- |
| [iCorrVision-2D](https://github.com/iCorrVision/iCorrVision-2D) | Subset-based 2D DIC engine, usable as a Python package, from the command line or through a PySide6 interface |
| [iCorrVision-Grabber](https://github.com/iCorrVision/iCorrVision-Grabber) | Image acquisition from one or two cameras, with a PySide6 interface; the series it records are read by iCorrVision-2D |

An iCorrVision 3D is planned.

Version 1 (2022) consists of two Tkinter applications, iCorrVision-2D and iCorrVision-3D, developed in the doctoral work of J. C. A. de Deus Filho and published as companion articles in *SoftwareX*. It remains available, unchanged, at [jcadf/iCorrVision_2D](https://github.com/jcadf/iCorrVision_2D) and [jcadf/iCorrVision_3D](https://github.com/jcadf/iCorrVision_3D).

## Contributing

Contributions are welcome. Please read the [contributing guide](https://github.com/iCorrVision/.github/blob/main/CONTRIBUTING.md) and the [Code of Conduct](https://github.com/iCorrVision/.github/blob/main/CODE_OF_CONDUCT.md), and report security problems privately as described in the [Security Policy](https://github.com/iCorrVision/.github/blob/main/SECURITY.md). The repositories are licensed under GPL-3.0-or-later.
