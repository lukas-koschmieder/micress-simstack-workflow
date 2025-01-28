# MICRESS®Benchmark: Early-Stage Microstructure Growth from Liquid State – SimStack Workflow

This repository provides an exemplary workflow for the [SimStack](https://www.simstack.de) workflow management system, demonstrating how to combine multiple Workflow Active Nodes (WaNos) for a streamlined simulation and visualization pipeline using [MICRESS](https://www.micress.de) and [MicPy](https://docs.micress.de/micpy). The workflow integrates two WaNos: [`MICRESS-EarlyStageGrowth`](https://github.com/lukas-koschmieder/MICRESS-EarlyStageGrowth) for simulating the early-stage growth of materials and [`MICRESS-PlotPhaseFractions`](https://github.com/lukas-koschmieder/MICRESS-PlotPhaseFractions) for visualizing the resulting phase fraction data.

This workflow highlights how SimStack can be used to create a fully automated MICRESS process, from defining simulation parameters to visualizing results. Using SimStack's flow control elements, such as loops, this example demonstrates the flexibility to scale up simulations, perform parameter studies, and aggregate results. For example, users can run multiple instances of `MICRESS-EarlyStageGrowth` with varying initial conditions, and then use `MICRESS-PlotPhaseFractions` to visualize the trends across simulations.

## Getting Started

To set up and run this MICRESS workflow in your SimStack environment, follow the steps outlined below.

### Prerequisites

1. **Install SimStack:** Ensure that SimStack is installed on your system, with both the SimStack Client and SimStack Server configured. For detailed instructions, refer to the [SimStack documentation](https://simstack.readthedocs.io).
2. **Install MICRESS:** MICRESS must be installed on the SimStack Server. Note that MICRESS is commercial software and must be obtained separately from the [MICRESS website](https://www.micress.de).

### Installation

1. Download the latest release from this repository.
2. Copy the `MICRESS` folder (containing the workflow configuration) into your SimStack Workflow Workspace on the SimStack Client.
3. Use the `environment.yml` file provided in this repository to create a Conda environment on the SimStack Server: `conda env create -f environment.yml`
4. Ensure the MICRESS executable `MICRESS_noTQ.exe` is available in the system path on the SimStack Server. If this is not the case, you may need to adjust the `WaNoExecCommand` in the `MICRESS-EarlyStageGrowth.xml` configuration file.

Once these steps are completed, the workflow will be ready to use within your SimStack environment.
