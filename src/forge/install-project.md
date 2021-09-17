---
summary: Get help installing components from Forge.
tags: forge; forge_support; forge_support_sharing
---

# Installing a Project

## Why am I being asked to download from the Forge website? Why can’t I just install the application from the development environment?

Automatic application installation is available only for projects that use the OutSystems Application Package format. For all other projects and formats, including those in the Forge, users are guided to a download and a manual installation process.

Occasionally a format is valid, but the target environment (version, stack, database) may not be compatible with the latest stable version of the requested project. In this case, go to the project's Versions tab in the Forge and look for a compatible application version. If a compatible version is not available, go to the project's Discussions tab in the Forge and request assistance from the project team.

## Why is dependency analysis telling me I cannot install because I have a customized version of the application?

OutSystems is able to recognize that this project has been downloaded and modified in the past. By installing a new version, you would lose all your work.

If your changes were mainly for experimentation purposes, and losing them won't matter in the long run, delete the currently installed application and retry the installation from the Forge.

If you want to keep the changes and take advantage of features, fixes, or both from a newer version, download the OutSystems Application Package file. Then, upload and publish it in the management console, and proceed to merge the changes.
