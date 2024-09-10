# Local Setup

This guide will take you step-by-step through the process of fine-tuning BERT on
the SQuAD dataset. You can run the code locally on your machine, or use a GPU
Notebook server, such as [Google Colab](https://colab.research.google.com/), to
speed up the training process.

## What you'll need

Before you start, make sure you have the following installed on your machine:

- Python 3.8 or higher

## Procedure

1. Clone the repository:

    ```console
    user:~$ git clone https://github.com/dpoulopoulos/bert-qa-finetuning.git
    ```

1. Navigate to the project directory:

    ```console
    user:~$ cd bert-qa-finetuning
    ```

1. Create a Python virtual environment:

    ```console
    user:~/bert-qa-finetuning$ python -m venv .venv
    ```

1. Activate the virtual environment:

    ```console
    user:~/bert-qa-finetuning$ source .venv/bin/activate
    ```

1. Install the required packages:

    ```console
    user:~/bert-qa-finetuning$ pip install -r requirements.txt
    ```

1. Run the Jupyter Notebook server and select the `bert-squad.ipynb` file:

    ```console
    user:~/bert-qa-finetuning$ jupyter notebook
    ```

1. Follow the instructions in the notebook to fine-tune BERT on the SQuAD
   dataset.

## Next steps

Congratulations! You've successfully fine-tuned BERT on the SQuAD dataset. You
can now use the model to solve Question-Answering tasks on your own data.

If you have access to a Kubeflow cluster, you can also leverage
[Kubeflow Pipelines](https://www.kubeflow.org/docs/components/pipelines/) to
scale and automate the experiment. Check the
[Kubeflow Pipelines](kubeflow-pipelines.md) guide for more information.

