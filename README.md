# Assessessment of Operating Envelopes to Orchestrate DERs - OE Algorithm 1: Ideal

This repository is part of the project [Assessing the Benefits of Using Operating Envelopes to Orchestrate DERs Across Australia](https://electrical.eng.unimelb.edu.au/power-energy/projects/assessing-the-benefits-of-OEs-across-Australia) funded by CSIRO. This project provided key metrics and recommendations for distribution companies (known as Distribution Network Service Providers [DNSPs] in Australia) and AEMO (the Australian system operator) to assist them in their decision-making process when defining the most suitable Operating Envelope (OE) implementations in a given distribution area.

In this repository, we use interactive code via Jupyter Notebook and Python as well as a realistic residential low voltage (LV) network to demonstrate the process and necessary calculations for the *Ideal OE Algorithm* produced by The University of Melbourne. This demonstration is useful for different stakeholders (e.g., DNSPs, AEMO, CSIRO, regulators, consultancy companies, technology providers) as it can help them familiarise with the corresponding algorithm and the required inputs as well as the pros and cons.

## Ideal OE
The Ideal OE is the most advanced and, hence, the most accurate operating envelope approach as it uses power flows to carry out calculations. However, it needs a full electrical network model and full monitoring of customers, which makes its implementation complex. If the model and monitoring data are correct, it can guarantee the operation of the network within technical limits (i.e., voltage and thermal) as well as the maximum possible export and/or import limits. Therefore, this operating envelope is used as a benchmark for the simpler ones studied in the project.
- Required Monitoring: At the secondary of the transformer (aggregated P, aggregated Q, and voltages, all per phase), at all customers (net demand P and Q).
- Required Electrical Models: Full three-phase electrical network model.

For simplicity, the case study used to demonstrate the OE algorithm corresponds to a low voltage (LV) network without modelling the upstream high voltage (HV) network. Although some adaptations have been made to ensure realistic voltage fluctuations at the distribution transformer of the LV network, the results are not exactly the same as those presented in the Final Report of the project (which used an integrated HV-LV network model). Nevertheless, the behaviour of the OE algorithm and the qualitative nature of the results remain the same. 

## Run the Code
Choose one of the options below to run the code.

### A. Cloud Option ☁️: Google Colab
Just click on the badge <a target="_blank" href="https://colab.research.google.com/github/Team-Nando/OE1-Ideal/blob/main/OE1-Ideal.ipynb"> <img src="https://colab.research.google.com/assets/colab-badge.svg"/></a>. You don't need to install anything 🤓💪.

### B. Local Option 💻: Jupyter Notebook 
Make sure you have installed all the pre-requisites (Anaconda, dss_python, requirements). Otherwise, you will not be able to go through the repository.

1. Download all the files using the green **`<> Code`** button at the top right.
   - You will get a ZIP file with a folder that contains all the files.
   - Unzip the file and place the folder somewhere on your computer/laptop.
2. To open the Jupyter Notebook file (extension **`ipynb`**) you need to:
   - Open Anaconda Navigator
   - Click on Launch Jupyter Notebook (it will open in your browser)
   - Upload the unzipped folder (with all the corresponding files) to Jupyter Notebook (the location is up to you)
   - Go inside the folder and open the **`ipynb`** file

All the instructions will be in the **`ipynb`** file.

## Credits

Arthur Gonçalves Givisiez (a.goncalvesgivisiez@unimelb.edu.au) <br>
Andres Avila Rojas (aavilarojas@student.unimelb.edu.au)  
Nando Ochoa (luis.ochoa@unimelb.edu.au ; https://sites.google.com/view/luisfochoa)

## Acknowledgements
We acknowledge AusNet Services for providing the data listed below, which was essential to create this repository.
- Anonymised historical active power demand of some customers (smart meter data)
- The data (i.e., topology, impedances, distribution transformers) of one of their HV feeders (indirectly used by this repository)
 
We also acknowledge the Australian Bureau of Meteorology for providing the solar radiation data.

## Licenses

Since this repository uses dss_python which is based on OpenDSS, both licenses have been included. This repository uses the BSD 3-Clause "New" or "Revised" license. Check all corresponding files (`LICENSE-OpenDSS`, `LICENSE-dss_python`, `LICENSE`).
