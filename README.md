# Microsoft Azure Kusto  (Azure Data Explorer) SDK  for Python

[*azure-kusto-data*]("https://github.com/Azure/azure-kusto-python/tree/master/azure-kusto-data") Package provides the capability to query Kusto clusters with Python.<br>
[![PyPI version](https://badge.fury.io/py/azure-kusto-data.svg)](https://badge.fury.io/py/azure-kusto-data)
[![Downloads](https://pepy.tech/badge/azure-kusto-data)](https://pepy.tech/project/azure-kusto-data)<br>
[*azure-kusto-ingest*]("https://github.com/Azure/azure-kusto-python/tree/master/azure-kusto-ingest") Package allows sending data to Kusto service - i.e. ingest data.<br>
[![PyPI version](https://badge.fury.io/py/azure-kusto-ingest.svg)](https://badge.fury.io/py/azure-kusto-ingest)
[![Downloads](https://pepy.tech/badge/azure-kusto-ingest)](https://pepy.tech/project/azure-kusto-ingest)<br>

**A new addition to the family (still in alpha):**

https://github.com/Azure/azure-kusto-ingestion-tools/tree/master/kit

[*azure-kusto-ingestion-tools*]("https://github.com/Azure/azure-kusto-ingestion-tools/tree/master/kit")  a simple toolkit to help with ingestions, available here<br>

[![PyPI version](https://badge.fury.io/py/azure-kusto-ingestion-tools.svg)](https://badge.fury.io/py/azure-kusto-ingestion-tools)
[![Downloads](https://pepy.tech/badge/azure-kusto-ingestion-tools)](https://pepy.tech/project/azure-kusto-ingestion-tools)<br>

## Install
### Option 1: Via PyPi
To install via the Python Package Index (PyPI), type:

* `pip install azure-kusto-data`
* `pip install azure-kusto-ingest`

### Option 2: Source Via Git
To get the source code of the SDK via git just type:

```python
git clone git://github.com/Azure/azure-kusto-python.git
cd ./azure-kusto-python/azure-kusto-data
python setup.py install
cd ../azure-kusto-ingest
python setup.py install
```

### Option 3: Source Zip
Download a zip of the code via GitHub or PyPi. Then follow the same instructions in option 2.

### Optionals:
* [_Pandas_](http://pandas.pydata.org/) - Package provides extra functionality for use with pandas. Since these are optional dependencies, install with pandas:
    * `pip install azure-kusto-data[pandas]`
    * `pip install azure-kusto-ingest[pandas]`

## Minimum Requirements
* Python 3.5 and above
* See setup.py for dependencies

## Authentication methods:

* AAD Username/password - Provide your AAD username and password to Kusto client (**check the notice below**).
* AAD application - Provide app ID and app secret to Kusto client.
* AAD code - Provide only your AAD username, and authenticate yourself using a code, generated by ADAL.

**<!> IMPORTANT NOTICE <!>**:
User authentication (using username and password) has a major caveat:
Sometimes users are required to use Multi-Factor Authentication. In such a case, this flow won't work for them.
It is a limitation of the AAD library we are using under the hood. There are [several bugs reported](https://github.com/AzureAD/azure-activedirectory-library-for-python/issues?utf8=%E2%9C%93&q=is%3Aissue+mfa).

There is also a feature request for the adal team to work on implementing IWA (Intergrated Windows Auth) so that signed in users won't have to authenticate. Feel free to [upvote](https://github.com/AzureAD/microsoft-authentication-library-for-python/issues/31) if it is relevant in your case.

Another Alternative that is planned, is adding pass trough auth based on azure-cli. 
[Upvote](https://github.com/Azure/azure-kusto-python/issues/139) if that is relevant for you.


## Samples:

* [Kusto query sample](https://github.com/Azure/azure-kusto-python/blob/master/azure-kusto-data/tests/sample.py)

* [Data ingest sample](https://github.com/Azure/azure-kusto-python/blob/master/azure-kusto-ingest/tests/sample.py)


## Need Support?
- **Have a feature request for SDKs?** Please post it on [User Voice](https://feedback.azure.com/forums/915733-azure-data-explorer) to help us prioritize
- **Have a technical question?** Ask on [Stack Overflow with tag "azure-data-explorer"](https://stackoverflow.com/questions/tagged/azure-data-explorer)
- **Need Support?** Every customer with an active Azure subscription has access to [support](https://docs.microsoft.com/en-us/azure/azure-supportability/how-to-create-azure-support-request) with guaranteed response time.  Consider submitting a ticket and get assistance from Microsoft support team
- **Found a bug?** Please help us fix it by thoroughly documenting it and [filing an issue](https://github.com/Azure/azure-kusto-python/issues/new).

## Looking for SDKs for other languages/platforms?
- [Node](https://github.com/azure/azure-kusto-node)
- [Java](https://github.com/azure/azure-kusto-java)
- [.NET](https://docs.microsoft.com/en-us/azure/kusto/api/netfx/about-the-sdk)


# Contribute

We gladly accept community contributions.

- Issues: Please report bugs using the Issues section of GitHub
- Forums: Interact with the development teams on StackOverflow or the Microsoft Azure Forums
- Source Code Contributions: If you would like to become an active contributor to this project please follow the instructions provided in [Contributing.md](CONTRIBUTING.md).

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

For general suggestions about Microsoft Azure please use our [UserVoice forum](http://feedback.azure.com/forums/34192--general-feedback).
