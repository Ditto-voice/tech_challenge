# Technical Challenge

As we train newer models, and collaborate with people in the team to improve our models. In Machine Learning, bugs may affect the distribution of possible models more than any particular instance, making traditional deterministic tests misleading. 

Because of this, a test-driven development framework for large ML models must account for the statistical nature of training. This is specially crucial when multiple researchers and engineers are contributing to the same model, as it's easy to silently introduce regressions to our codebase. 

We want to be able to use hyper-parameter sweeps or change some of the modular layers of our neural network. We have a config file, that allows uses to make ablations (A/B tests of changes) clear. Each config is essentially a new model definition (or new code 🙂). [Software 2.0](https://www.google.com/search?q=software+2.0&oq=software+2.0&aqs=chrome..69i57j0l2j69i60l2j69i61.2182j0j7&sourceid=chrome&ie=UTF-8) that is.


![Different Runs](https://www.notion.so/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2F61999c10-7880-434f-b035-d04e1c200b39%2F5d65a8941b07761910ac232f_SIt7zCz7MYI0UM1htCeinwqXsR8YW1A8-XRZpZLDLcQ74bhx-kRpbj67HqsdidEBqHCiXrw3kI6voTZpgfX8EIjkriV-a1sHs8_jBXMNKsBXmOxTRI0oO_nMHHqs6r8CpRSkDJ_4.png?table=block&id=d672ae1f-e9dc-4d2e-ad5d-cc01ff31e8fb&width=3200&cache=v2)
