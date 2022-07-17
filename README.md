# Run PyLint for Python Action

Runs `PyLint` for code in folder `src`. All the code is evaluated.

## Getting Started

### Inputs

| name              | Description | Required |
|-------------------|-------------|----------|
| source            | Directory where the source code is located. Defaults to current directory. | No |
| moduleOrPackage   | Module or package over which to run lintering. Defaults to all (*). | No |
| useConda          | Indicates if the tests will run using an specific conda environment. | No |
| condaEnvName      | Name of the conda environment to use. Required if `useConda` is `true`. | No | 
| disable           | Indicates which rules should not be checked. Coma separeted values are possible. Defaults `None`. | No |
| version           | PyLint library version. Defaults to `2.12.1`. | No |
| pkgWhitelist      | Indicates which packages should not be checked for lintering. Defaults `None`. | No |


### Example usage

**#1**
> Runs `PyLint` for code in folder `src`. All the code is evaluated. Rules `W1023` and `C0103` are not validated. Uses a conda environment named `cicd`. This environment should be created beforehand.

```yml
name: Running lintering
uses: pyrunit/pylint-action@v1.0.0
with:
    source: src
    useConda: true
    condaEnvName: cicd
    disable: W1203,C0103
```
