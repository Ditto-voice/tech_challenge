# Technical Challenge

As we train newer models, and collaborate with people in the team to improve our models. In Machine Learning, bugs may affect the distribution of possible models more than any particular instance, making traditional deterministic tests misleading. 

Because of this, a test-driven development framework for large ML models must account for the statistical nature of training. This is specially crucial when multiple researchers and engineers are contributing to the same model, as it's easy to silently introduce regressions to our codebase. 

We want to be able to use hyper-parameter sweeps or change some of the modular layers of our neural network. We have a config file, that allows uses to make ablations (A/B tests of changes) clear. Each config is essentially a new model definition (or new code 🙂). [Software 2.0](https://www.google.com/search?q=software+2.0&oq=software+2.0&aqs=chrome..69i57j0l2j69i60l2j69i61.2182j0j7&sourceid=chrome&ie=UTF-8) that is.
