## Getting started

To download the latest version (not tested) of the example project to your computer, you can either:

* [Click here](https://github.com/qualisys/paf-enable-markerless-example/archive/refs/heads/main.zip) to download it as a zip file.
<br>_— or —_
* Clone this repository to your computer.

To download a release version (tested), please [Click here](https://github.com/qualisys/paf-enable-markerless-example/releases)

## Preparing Qualisys data for ENABLE processing

ENABLE is a markerless engine developed by the Southwest Research Institute (https://www.swri.org/industry/biomechanics-human-performance/markerless-motion-capture-laboratory).
1. Contact enable@swri.org to get the ENABLE installer, license file and installation information.
2. Run the installer and follow the instructions.
3. In QTM, set Project Options > Miscellaneous > Folder Options for "ENABLE" to ```C:\Program Files (x86)\ENABLE\enable.exe``` (adapt if installed at different location).
4. Download data from Qualisys File Library (https://qfl.qualisys.com/#!/project/theiaexample)
5. Extract Jack Doe from the downloaded .zip file into the projects data folder "ENABLE Markerless Example\Data".
6. To process the data, click on **Start Processing**.
7. When the processing is done:
   - skeleton data are exported into c3d and tsv files and can be used for further analysis with the software of your choice (for example Python or Matlab)
   - mot and osim files are exported to be used in OpenSim. Note that Edit > Preferences > Geometry Search Path will have to point to ```C:\Program Files (x86)\ENABLE\utils\opensim_files\Geometry```

Note: You can automatically create an `Overlays` folder containing video overlays. However, it is significantly slowing down the processing performance. To do so, modify the following line in Settings.paf to add the `--overlays` option:  
`Arguments: [--input-dir, $WorkingDirectory$, --calib, qualisys_ex, --overlays]`

## Resources for using the Qualisys Project Automation Framework (PAF)

The purpose of the ***Project Automation Framework*** (PAF) is to streamline the motion capture process from data collection to the final report. This repository contains an example project that illustrate how PAF can be used to implement custom automated data collection in [Qualisys Track Manager (QTM)](http://www.qualisys.com/software/qualisys-track-manager/), and how QTM can be connected to a processing engine. 

### PAF Documentation

The full documentation for PAF development is available here: [PAF Documentation](https://github.com/qualisys/paf-documentation).


### PAF Examples

Our official examples for various processing engines:

- [ENABLE](https://github.com/qualisys/paf-enable-markerless-example)
- [Excel](https://github.com/qualisys/paf-excel-example)
- [Matlab](https://github.com/qualisys/paf-matlab-example)
- [OpenSim](https://github.com/qualisys/paf-opensim-example)
- [Python](https://github.com/qualisys/paf-python-example)
- [Theia Markerless](https://github.com/qualisys/paf-theia-markerless-example)
- [Theia Markerless Comparison](https://github.com/qualisys/paf-theia-markerless-comparison-example)
- [Theia Markerless True Hybrid](https://github.com/qualisys/paf-theia-markerless-true-hybrid-example)
- [Visual3D](https://github.com/qualisys/paf-visual3d-example)

_As of QTM version 2.17, the official Qualisys PAF examples can be used without any additional license. Note that some more advanced analysis types require a license for the "PAF Framework Developer kit" (Article number 150300)._
