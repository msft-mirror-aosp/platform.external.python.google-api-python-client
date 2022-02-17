# Google API Client

[![PyPI version](https://badge.fury.io/py/google-api-python-client.svg)](https://badge.fury.io/py/google-api-python-client)

This is the [Google API Python client library](https://cloud.google.com/apis/docs/client-libraries-explained#google_api_client_libraries)
for Google's discovery based APIs. To get started, please see the
[docs folder](https://github.com/googleapis/google-api-python-client/blob/main/docs/README.md).

This library is considered complete and is in maintenance mode. This means
that we will address critical bugs and security issues but will not add any
new features.

This library is officially supported by Google.  However, the maintainers of
this repository recommend using [Cloud Client Libraries for Python](https://github.com/googleapis/google-cloud-python),
where possible, for new code development. For more information, please visit
[Client Libraries Explained](https://cloud.google.com/apis/docs/client-libraries-explained).

## Version 2.0 Release
The 2.0 release of `google-api-python-client` includes a substantial reliability 
improvement, compared with 1.x, as discovery documents are now cached in the library 
rather than fetched dynamically. It is highly recommended to upgrade from v1.x to v2.x.

Only python 3.6 and newer is supported. If you are not able to upgrade python, then
please continue to use version 1.x as we will continue supporting python 2.7+ in
[v1](https://github.com/googleapis/google-api-python-client/tree/v1).

Discovery documents will no longer be retrieved dynamically when
you call `discovery.build()`. The discovery documents will instead be retrieved
from the client library directly. New versions of this library are released weekly.
As a result of caching the discovery documents, the size of this package is at least 
50 MB larger compared to the previous version. 

Please see the [Migration Guide](https://github.com/googleapis/google-api-python-client/blob/main/UPGRADING.md)
for more information.

## Documentation

See the [docs folder](https://github.com/googleapis/google-api-python-client/blob/main/docs/README.md) for more detailed instructions and additional documentation.

## Other Google API libraries

The maintainers of this repository recommend using
[Cloud Client Libraries for Python](https://github.com/googleapis/google-cloud-python),
where possible, for new code development due to the following reasons:

With [Cloud Client Libraries for Python](https://github.com/googleapis/google-cloud-python):
- There is a separate client library for each API, so you can choose
which client libraries to download. Whereas, `google-api-python-client` is a
single client library for all APIs. As a result, the total package size for
`google-api-python-client` exceeds 50MB.
- There are stricter controls for breaking changes to the underlying APIs
as each client library is focused on a specific API.
- There are more features in these Cloud Client Libraries as each library is
focused on a specific API, and in some cases, the libraries are owned by team
who specialized in that API.
- Developers will benefit from intellisense.

For more information, please visit
[Client Libraries Explained](https://cloud.google.com/apis/docs/client-libraries-explained).

Although there are many benefits to moving to
[Cloud Client Libraries for Python](https://github.com/googleapis/google-cloud-python),
the maintainers want to emphasize that `google-api-python-client` will continue
to be supported.

For Google Ads API, we recommend using [Google Ads API Client Library for Python](https://github.com/googleads/google-ads-python/).

For Google Firebase Admin API, we recommend using [Firebase Admin Python SDK](https://github.com/firebase/firebase-admin-python).

## Installation

Install this library in a [virtualenv](https://virtualenv.pypa.io/en/latest/) using pip. virtualenv is a tool to
create isolated Python environments. The basic problem it addresses is one of
dependencies and versions, and indirectly permissions.

With virtualenv, it's possible to install this library without needing system
install permissions, and without clashing with the installed system
dependencies.

### Mac/Linux

```
pip install virtualenv
virtualenv <your-env>
source <your-env>/bin/activate
<your-env>/bin/pip install google-api-python-client
```

### Windows

```
pip install virtualenv
virtualenv <your-env>
<your-env>\Scripts\activate
<your-env>\Scripts\pip.exe install google-api-python-client
```

## Supported Python Versions

Python 3.6, 3.7, 3.8, 3.9 and 3.10 are fully supported and tested. This library may work on later versions of 3, but we do not currently run tests against those versions.

## Unsupported Python Versions

Python < 3.6

## Third Party Libraries and Dependencies

The following libraries will be installed when you install the client library:
* [httplib2](https://github.com/httplib2/httplib2)
* [uritemplate](https://github.com/sigmavirus24/uritemplate)

For development you will also need the following libraries:
* [WebTest](http://webtest.pythonpaste.org/en/latest/index.html)
* [pyopenssl](https://pypi.python.org/pypi/pyOpenSSL)

## Contributing

Please see our [Contribution Guide](https://github.com/googleapis/google-api-python-client/blob/main/CONTRIBUTING.rst).
In particular, we love pull requests - but please make sure to sign
the contributor license agreement.
