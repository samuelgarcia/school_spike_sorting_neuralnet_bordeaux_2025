# SpikeInterface Training Bordeaux November 2025

Material for the SpikeInterface Tutorial organized in Bordeaux during the GDR NeuralNet, November 2025 by Pierre Yger and Samuel Garcia

## Schedule


**Tuesday 25 9h00 - 12h00**

  * **Introduction to Spike Sorting** (1h30) [P. Yger]
  * **Introduction to `SpikeInterface`** (30min) [S. Garcia]
  * **Chek you install / download** 15min [both]


  * **Tutorial 1** Reading + Manipulation (20 min) [S. Garcia]
    - Read and visualise data
    - The importance of probes


**Tuesday 25 13h00 - 17h00**

  * **Tutorial 2** Preprocessing (45 min) [P. Yger]
    - Apply and visualize preprocessing 
    - Detect bad channels
    - Motion correction

  * **Tutorial 3** Spike sort (45 min) [S. Garcia]
    - Run a spike sorter
    - Compare spike sorter outputs

  * **Tutorial 4**  Analyze Sorting (45 min) [P. Yger]
    - Create a `SortingAnalyzer` to explore your sorting
    - Compute some extensions
    - Play with the extension outputs

  * **Tutorial 5**  Manual curation with Spikeinterface GUI (45min) [S. Garcia]
    - demo

  * **Tutorial 6**  Automaatic uration (45 min) [P. Yger]
    - Simple, threshold-based curation
    - Curation using ML models
    - Merging units

**Wednesday 26 9h00 - 12h00**

  * **Spike sorting on your own and/or other dataset** [both]



# Overview of available datasets

## In vivo

### M25_D23_2024-11-11_13-11-10_OF1

Neuropixels 2.0 dataset (384 channels) acquired with the Open Ephys GUI in binary format.
You can use the `spikeinterface.extractor.read_openephys()` function to read the data.

### 1544_2023-04-21_09-55-34_of

Recording with 16 channels organized in 4 tetrodes acquired with the Open Ephys GUI in "openephys" format.
You can use the `spikeinterface.extractor.read_openephys()` function to read the data.


### cambridgeNT_openephys

Recording with a Cambridge Neurotech [ASSY-236-H5](https://github.com/SpikeInterface/probeinterface_library/blob/main/cambridgeneurotech/ASSY-236-H5/ASSY-236-H5.png) probe and wired to the Open Ephys acquisition system via the 
Cambridge NeuroTech mini-amp-64.
You can use the `spikeinterface.extractor.read_openephys()` function to read the data.
The probe is available from the [probeinterface_library](https://github.com/SpikeInterface/probeinterface_library) (see [docs](https://probeinterface.readthedocs.io/en/main/examples/ex_10_get_probe_from_library.html) here) and the wiring is available in [`ProbeInterface`](https://probeinterface.readthedocs.io/en/main/examples/ex_11_automatic_wiring.html#).


## In vitro

### mouse_CTX_14D.brw

Primary mouse cortex for E18 embryos. Plated 80K on CorePlate 1W38/60 3Brain, recorded after 14 days in culture 
with 3Brain BioCAM system. 
You can use the `spikeinterface.extractor.read_biocam()` function to read the data. 


### human_ngn2_100K_c_55D.brw

Human glutamatergic neurons induced via ngn2 method. Plated 100k on CorePlate 1W38/60 3Brain, recorded after 55 days in 
culture with 3Brain BioCAM system. 
You can use the `spikeinterface.extractor.read_biocam()` function to read the data. 

> [!IMPORTANT]  
> The 3Brain BioCAM system saves the data in unsigned integers. You should convert it to signed integers for a smooth
> processing. See documentation [here](https://spikeinterface.readthedocs.io/en/latest/how_to/unsigned_to_signed.html). Note that the `bit_depth` for this system is 12!


Please download these datasets on your laptop from this link:


https://filesender.renater.fr/?s=download&token=f94a08b3-e779-4911-90bf-a312c3c34a01
