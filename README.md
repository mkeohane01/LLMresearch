# LLMresearch

## HELM CLI package

Documentation for the package can be found [here](https://crfm-helm.readthedocs.io/en/latest/).

Helm website can be found [here](https://crfm.stanford.edu/helm/latest/?).

## Use
To install the package using pip
```bash
pip install crfm-helm
```

In order to run a helm evaluation. Need to update run_specs.conf accordingly.
```bash
helm-run --conf-paths run_specs.conf --suite <suite_name> --max-eval-instances <num>
```

To summarize results
```bash
helm-summarize --suite <suite_name>
```

To open Helm server locally
```bash
helm-server
```
