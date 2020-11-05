# Create and Explore an Azure Machine Learning Workspace

In this exercise, you will create and explore an Azure Machine Learning workspace.

## Create an Azure Machine Learning workspace

As its name suggests, a workspace is a centralized place to manage all of the Azure ML assets you need to work on a machine learning project.

1. In the [Azure portal](https://portal.azure.com), create a new **Machine Learning** resource, specifying a unique workspace name and creating a new resource group in the region nearest your location.
2. When the workspace and its associated resources have been created, view the workspace in the portal.

## Explore Azure Machine Learning studio

You can manage some workspace assets in the Azure portal, but for data scientists, this tool contains lots of irrelevant information and links that relate to managing general Azure resources. *Azure Machine Learning studio* provides a dedicated web portal for working with your workspace.

1. In the Azure portal blade for your Azure Machine Learning workspace, click the link to launch **Azure Machine Learning studio**; or alternatively, in a new browser tab, open [https://ml.azure.com](https://ml.azure.com). If prompted, sign in using the Microsoft account you used in the previous task and select your Azure subscription and workspace.

    > **Tip** If you have multiple Azure subscriptions, you need to choose the Azure *directory* in which the subscription is defined; then choose the subscription, and finally choose the workspace.

2. View the Azure Machine Learning studio interface for your workspace - you can manage all of the assets in your workspace from here.
3. In Azure Machine Learning studio, toggle the &#9776; icon at the top left to show and hide the various pages in the interface. You can use these pages to manage the resources in your workspace.

## Create a compute instance

One of the benefits of Azure Machine Learning is the ability to create cloud-based compute on which you can run experiments and training scripts at scale.

1. In Azure Machine Learning studio, view the **Compute** page. This is where you'll manage compute resources for your data science activities. There are four kinds of compute resource you can create:
    - **Compute Instances**: Development workstations that data scientists can use to work with data and models.
    - **Compute Clusters**: Scalable clusters of virtual machines for on-demand processing of experiment code.
    - **Inference Clusters**: Deployment targets for predictive services that use your trained models.
    - **Attached Compute**: Links to other Azure compute resources, such as Virtual Machines or Azure Databricks clusters.

    For this exercise, you'll create a compute instance so you can run some code in your workspace.

2. On the **Compute Instances** tab, add a new compute instance with the following settings. You'll use this as a workstation to run code in notebooks.
    - **Virtual Machine type**: CPU
    - **Virtual Machine size**: Standard_DS11_v2
    - **Compute name**: *enter a unique name*
    - **Enable SSL configuration**: Unselected
3. Wait for the compute instance to start and its status to change to **Running**.

## Clone and run a notebook

A lot of data science and machine learning experimentation is performed by running code in *notebooks*. Your compute instance includes fully featured Python notebook environments (*Jupyter* and *JuypyterLab*) that you can use for extensive work; but for basic notebook editing, you can use the built-in **Notebooks** page in Azure Machine learning studio.
<!-- Wait for Terminal to go public preview mid-November -->
1. In Azure Machine Learning studio, view the **Notebooks** page.
2. Open a **Terminal**, and ensure its **Compute** is set to your compute instance.
3. Enter the following command to clone a Git repository containing notebooks, data, and other files to your workspace:
    <!-- Update to MicrosoftDocs repo for release -->
    ```bash
    git clone https://github.com/GraemeMalcolm/DP100
    ```

4. When the command has completed, in the **My files** pane, click **&#8635;** to refresh the view and verify that a new folder named **DP100** has been created. This folder contains multiple **.ipynb** notebook files.
5. Close the terminal pane, terminating the session.
6. In the **DP100** folder, open the **Get Started with Notebooks** notebook. Then read the notes and follow the instructions it contains.

> **Tip**: To run a code cell, select the cell you want to run and then use the **&#9655;** button to run it.

## Stop your compute instance

If you've finished exploring Azure Machine Learning for now, you should shut down your compute instance to avoid incurring unnecessary charges in your Azure subscription.

1. In Azure Machine Learning studio, on the **Compute** page, select your compute instance.
2. Click **Stop** to stop your compute instance. When it has shut down, its status will change to **Stopped**.
