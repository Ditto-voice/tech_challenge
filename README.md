# Technical Challenge

As we train newer models, and collaborate with people in the team to improve our models. In Machine Learning, bugs may affect the distribution of possible models more than any particular instance, making traditional deterministic tests misleading. 

Because of this, a test-driven development framework for large ML models must account for the statistical nature of training. This is specially crucial when multiple researchers and engineers are contributing to the same model, as it's easy to silently introduce regressions to our codebase. 

We want to be able to use hyper-parameter sweeps or change some of the modular layers of our neural network. We have a config file, that allows uses to make ablations (A/B tests of changes) clear. Each config is essentially a new model definition (or new code 🙂). [Software 2.0](https://www.google.com/search?q=software+2.0&oq=software+2.0&aqs=chrome..69i57j0l2j69i60l2j69i61.2182j0j7&sourceid=chrome&ie=UTF-8) that is.


![Different Runs](https://www.notion.so/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2F61999c10-7880-434f-b035-d04e1c200b39%2F5d65a8941b07761910ac232f_SIt7zCz7MYI0UM1htCeinwqXsR8YW1A8-XRZpZLDLcQ74bhx-kRpbj67HqsdidEBqHCiXrw3kI6voTZpgfX8EIjkriV-a1sHs8_jBXMNKsBXmOxTRI0oO_nMHHqs6r8CpRSkDJ_4.png?table=block&id=d672ae1f-e9dc-4d2e-ad5d-cc01ff31e8fb&width=3200&cache=v2)


This image above shows a few parameter changes and the results, and how they compare to each other. We always want our models to improve over time, and therefore, determining how our model is performing at any single moment is extremely important. In this way we can run [hyper-parameter sweeps](https://docs.wandb.com/library/sweeps), or change different modules of our Neural network, and improve our results over-time.

## Setup

Whenever using generative models researchers calculate the distance between a set of generated media and the "real" media. Calculating distances between such  dimensional distributions in order to quantify how well a given model succeeds at a task is difficult. In the case of pictures, one could look at a few samples to gauge visual quality, but doing so for every model trained is not feasible.

In addition, these models tend to focus on a few modes of the overall target distribution, while completely ignoring others. For example, they may learn to generate only one type of object or only a select few viewing angles - for images. As a consequence, looking only at a limited number of samples from the model may not indicate whether the network learned the entire distribution successfully. To remedy this, a metric is needed that aligns well with human judgement of quality, while also taking the properties of the target distribution into account.

Given two set of audio waves, analyze different ways of comparing these sets of audio files, and write down a function that compares them objectively. Write down the difference between the different options that you considered and why you made the choice for a specific metric. Write down the function 

### Code Setup

Create a virtualenv and install the dependencies

    $ virtualenv venv # Create virtualenv venv
    $ source venv/bin/activate # Activate virtualenv
    $ pip install -r requirements.txt

### **Create test files and file lists**

This will generate a set of background test files (sine waves at different frequencies). And two test sets of sine waves with distortions.

    $ python -m gen_audio --test_files "test_audio"

### Distance

Calculate the distance between: `test1` and `background`, and `test2` and `background`
