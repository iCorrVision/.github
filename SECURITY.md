# Security Policy

This policy applies to all the repositories of the iCorrVision organization (iCorrVision-2D,
iCorrVision-Grabber and future ones).

## Supported versions

Security fixes are applied to the latest version on `main` of each repository and, once published, to its
latest release. Version 1 (`jcadf/iCorrVision_2D`) is frozen and receives no fixes.

## Reporting a vulnerability

Please do not open a public issue for a security problem. Write privately to
**jmc.xavier@fct.unl.pt** with:

- the repository and a description of the problem and its impact;
- the iCorrVision version or commit, the Python version and the operating system;
- steps or a small example that reproduce it.

You will receive an acknowledgement as soon as possible. We will work with you on a fix and agree on
when to disclose the problem publicly.

## Scope

The iCorrVision tools are desktop and command-line applications that read image files and configuration
(TOML) files, and that control cameras (iCorrVision-Grabber). Reports about unsafe handling of such input
files, about camera or acquisition code, or about the build and release process, are welcome.
