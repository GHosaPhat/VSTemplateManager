# Visual Studio Template Manager

While tools for creating and using templates for individual projects currently exist in Microsoft's Visual Studio environment, they are not currently capable of automating the creation of templates for an entire solution containing multiple projects.  Additionally, the manual process of creating solution templates (found in the MSDN article, *[How to: Create Multi-Project Templates](https://msdn.microsoft.com/en-us/library/ms185308.aspx?f=255&MSPPError=-2147217396)*) is limited by the fact that a solution template cannot include a reference to an existing project.  Any solution created from a template constructed in this way will create a new and separate copy of every project in the template.

This last limitation can be problematic if the user wants to be able to, for example, have a template that contains a UI project template and then a "link" to an existing project for a common library which could require updates for the new application. The desired result in this case would be that, when the solution template is used, a new copy of the files from the UI template are created in the appropriate folders along with the .sln file. However, the existing common project ***is not duplicated*** in the solution folder. Instead, a reference is automatically created to the common project in the new UI project.

The Visual Studio Template Manager extends the capabilities of the template and project creation tools available in Microsoft's Visual Studio to include:

* Automated creation of templates for both **Projects** *and* **Solutions**
* Automated creation of both **Projects** *and* complete **Solutions** from existing templates

When working with **Solution Templates**, both of these features can be customized to either create copies of all projects in the solution, or to simply create a reference to one or more of the projects in the solution.

***NOTE:** While this is a work-in-progress, it is intended to be a very simple utility for users of Microsoft's Visual Studio to simplify template creation and use.*
