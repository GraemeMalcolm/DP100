# Run Experiments

Experiments are at the core of a data scientist's work. In Azure Machine Learning, an *experiment* is used to run a script or a pipeline, and usually generates outputs and records metrics. In this exercise, you will use the Azure Machine Learning SDK to run Python code as experiments.

## Before You start

If you have not already done so, complete the *[Create and Explore an Azure Machine Learning Workspace](01-create-a-workspace.md)* exercise to create an Azure Machine Learning workspace and compute instance, and clone the notebooks required for this exercise.

## Open Jupyter

While you can use the **Notebooks** page in Azure Machine Learning studio to run notebooks, it's often more productive to use a more fully-featured notebook development environment like *Jupyter*. Fortunately, your Azure Machine Learning compute instance includes an installation of Jupyter.

1. In [Azure Machine Learning studio](https://ml.azure.com), view the **Compute** page for your workspace; and on the **Compute Instances** tab, start your compute instance if it is not already running.
2. When the compute instance is running, click the **Jupyter** link to open the Jupyter home page in a new browser tab.

## Install the Azure Machine Learning SDK

The Azure Machine Learning SDK is installed by default on your compute instance, but it is updated frequently; so follow these steps to upgrade to the latest release.

1. In the Jupyter notebook environment, create a new **Terminal**. This will open a new tab with a command shell.
2. Enter the following command to update the Azure ML SDK:

    ```bash
    pip install --upgrade azureml-sdk
    ```

    You may see some warnings as the package dependencies are installed. You can ignore these.

3. The **azureml-sdk** SDK package provides the most important libraries needed to work with Azure Machine Learning> However, there are some additional packages that contain other useful libraries not included in the main SDK package. Use the following command to install the **azureml-widgets** package, which contains libraries for displaying Azure Machine Learning information in notebooks:

    ```bash
    pip install --upgrade azureml-widgets
    ```

4. When the installation is complete, you can close the **Terminal** tab and return to the tab containing the Jupyter home page.

> **More Information**: For more details about installing the Azure ML SDK and its optional components, see the [Azure ML SDK Documentation](https://docs.microsoft.com/python/api/overview/azure/ml/install?view=azure-ml-py).

## Run experiments in a notebook

Experiments in Azure Machine Learning need to be initiated from some sort of *control* layer; often a script or program. In this exercise, you'll use a notebook to control experiments.

1. In the Jupyter home page, browse to the **Users/DP100** folder where you cloned the notebook repository, and open the **Run Experiments** notebook.
2. Then read the notes in the notebook, running each code cell in turn.
3. When you have finished running the code in the notebook, on the **File** menu, click **Close and Halt** to close it and shut down its Python kernel. Then close all Jupyter browser tabs.

## Clean-up

If you're finished working with Azure Machine Learning for now, in Azure Machine Learning studio, on the **Compute** page, on the **Compute Instances** tab, select your compute instance and click **Stop** to shut it down. Otherwise, leave it running for the next lab.
