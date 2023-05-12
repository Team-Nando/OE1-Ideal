# Assessessment of Operating Envelopes to Orchestrate DERs - OE Algorithm 1: Ideal

This repository is part of the project [Assessing the Benefits of Using Operating Envelopes to Orchestrate DERs Across Australia](https://electrical.eng.unimelb.edu.au/power-energy/projects/assessing-the-benefits-of-OEs-across-Australia) funded by CSIRO. This project provided key metrics and recommendations for distribution companies (known as Distribution Network Service Providers [DNSPs] in Australia) and AEMO (the Australian system operator) to assist them in their decision-making process when defining the most suitable Operating Envelope (OE) implementations in a given distribution area.

In this repository, we use interactive code via Jupyter Notebook and Python as well as a realistic residential low voltage (LV) network to demonstrate the process and necessary calculations for the *Ideal OE Algorithm* produced by The University of Melbourne. This demonstration is useful for different stakeholders (e.g., DNSPs, AEMO, CSIRO, regulators, consultancy companies, technology providers) as it can help them familiarise with the corresponding algorithm and the required inputs as well as the pros and cons.

## Ideal OE
The Ideal OE is the most advanced and, hence, the most accurate operating envelope approach as it uses power flows to carry out calculations. However, it needs a full electrical network model and full monitoring of customers, which makes its implementation complex. If the model and monitoring data are correct, it can guarantee the operation of the network within technical limits (i.e., voltage and thermal) as well as the maximum possible export and/or import limits. Therefore, this operating envelope is used as a benchmark for the simpler ones studied in the project.
- Monitoring: At the secondary of the transformer (aggregated P, aggregated Q, and voltages, all per phase), at all customers (net demand P and Q).
- Electrical models needed: Full electrical network model.

It is important to notice that this interactive notebook is using a simple LV network model (without the HV part) for calculation of OEs and corresponding assessments, while the final report of the project is using the integrated HV-LV network model. To make the OEs calculated here closer to the ones in the report, the voltage variation along the day caused by the HV part is modelled here as a voltage source (following the measurements taken from the full HV-LV model). In addition, to represent the voltage rise/drop at the primary side of the distribution transformer, a fictitious line is created between the voltage source and the distribution transformer. Despite this effort, the OE values calculated in the final report will still not be the same as the ones calculated here. Nevertheless, the general qualitative nature of the OE is the same.

## Pre-Requisites
- Python (Anaconda) and Jupyter Notebook (comes with Anaconda). For download links and more info: https://www.anaconda.com/products/individual
- dss_python module. We use this Python-native module to run power flows based on OpenDSS (https://sourceforge.net/projects/electricdss/). To install, run "python -m pip install dss_python" in the Anaconda Prompt. For more info: https://github.com/Team-Nando/Tutorial-DERHostingCapacity-0-dss_python#part-0-using-dss_python

## Run the Code
Make sure you have installed all the pre-requisites (Anaconda and the dss_python module). Otherwise, you will not be able to go through the repository.

1. Download all the files using the green **`<> Code`** button at the top right.
   - You will get a ZIP file with a folder that contains all the files.
   - Unzip the file an place the folder somewhere in your computer/laptop.
3. To open the Jupyter notebook file (extension **`ipynb`**) you need to:
   - Open Anaconda Navigator
   - Click on Launch Jupyter notebook (it will open in your browser)
   - Upload the unzipped folder (with all the corresponding files) to Jupyter Notebook (the location is up to you)
   - Go inside the folder and open the **`ipynb`** file

All the instructions will be in the **`ipynb`** file.

## Credits

Arthur Gonçalves Givisiez (a.goncalvesgivisiez@unimelb.edu.au)

Nando Ochoa (luis.ochoa@unimelb.edu.au ; https://sites.google.com/view/luisfochoa)

## Licenses

Since this repository uses dss_python which is based on OpenDSS, both licenses have been included. This repository uses the BSD 3-Clause "New" or "Revised" license. Check all corresponding files (`LICENSE-OpenDSS`, `LICENSE-dss_python`, `LICENSE`).
