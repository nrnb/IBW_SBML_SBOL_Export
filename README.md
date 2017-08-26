# SBML and SBOL Model Export from the Infobiotics Workbench
The Infobiotics Workbench (IBW) is a modeling tool that provides stochastic simulations that mimic the procession of complex biological pathways, verification of simulation rulesets, and biomatter compilation. More specifically, the process of biomatter compilation (biocompilation) includes arranging biological parts, fetching their DNA sequences, inserting cloning sites, and calculating optimal ribosome-binding sites based on user constraints of positioning. Simulations and biocompilation are driven by designs written in the domain-specific Infobiotics Language (IBL).
## My Work
To enhance its compatibility with biological modeling standards, I present two functions that are able to parse an Eclipse Modeling Framework model built from IBL into either a SBOL or SBML document. The SBOL model accurately captures high-level interactions and sequence and structural information, while the SBML model maintains functional components including amounts and kinetic laws. A combination of the two comprehensively captures every aspect of an IBL model. The EMF model to be converted can also be preprocessed via biocompilation or flattening, both of which I account for during conversion. The logical step forward is to implement an import functionality that will allow for the generation of IBL models from external SBOL and SBML documents.
* [Biocompiler.xtend](https://github.com/BoyDun/IBW_SBML_SBOL_Export/blob/master/Biocompiler.xtend) - I removed the original, bare-bones SBOL export code from this file. I updated the rest of the file to run on the version 2 SBOL library, and I implemented sequence fetching from the SynBioHub SBOL repository.
* [BypassGUI.xtend](https://github.com/BoyDun/IBW_SBML_SBOL_Export/blob/master/BypassGUI.xtend) - 
* [SBMLExportInterface.java](https://github.com/BoyDun/IBW_SBML_SBOL_Export/blob/master/SBMLExportInterface.java)
* [SBMLExportWizard.java](https://github.com/BoyDun/IBW_SBML_SBOL_Export/blob/master/SBMLExportWizard.java)
* [SBMLExportWizardPage.java](https://github.com/BoyDun/IBW_SBML_SBOL_Export/blob/master/SBMLExportWizardPage.java)
* [SBML_Export.java](https://github.com/BoyDun/IBW_SBML_SBOL_Export/blob/master/SBML_Export.java)
* [SBOLExportInterface.java](https://github.com/BoyDun/IBW_SBML_SBOL_Export/blob/master/SBOLExportInterface.java)
* [SBOLExportWizard.java](https://github.com/BoyDun/IBW_SBML_SBOL_Export/blob/master/SBOLExportWizard.java)
* [SBOLExportWizardPage.java](https://github.com/BoyDun/IBW_SBML_SBOL_Export/blob/master/SBOLExportWizardPage.java)
* [SBOL_Export.java](https://github.com/BoyDun/IBW_SBML_SBOL_Export/blob/master/SBOL_Export.java)
## Running the Code
These files won't be runnable until Infobiotics Workbench is made open-source pending publication. However, you can currently access the executable software at LINK. In order to use my conversion functionality in its native application, navigate to File->Export->SBOL/SBML.
## Examples
You can access example IBL documents in the "Example Conversions" directory. Simply open one in the IBW executable and follow the previous steps to convert it into an SBML or SBOL model. The subdirectories in "Example Conversions" contain the converted versions of the IBL example documents.
## Built With
* [libSBOLj 2.0](https://github.com/SynBioDex/libSBOLj)
* [JSBML](https://github.com/sbmlteam/jsbml)
## Authors
* Peter Dun, bodun@stanford.edu

You can view my GSoC blog at https://peterdun.wordpress.com/, where I documented my weekly progress on this project.
Feel free to reach out with any questions, comments, suggestions, bug reports, etc.
## License
This project is licensed under the MIT License - see the [LICENSE](https://github.com/BoyDun/IBW_SBML_SBOL_Export/blob/master/LICENSE) file for more details.
## Acknowledgments
* Harold Fellermann and Chris Myers, my mentors who advised me through the entire GSoC process
* Laurentiu Mierla, for creating the export UI skeleton
