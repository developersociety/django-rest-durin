# Django-Rest-Durin

[![django-rest-durin on pypi](https://img.shields.io/pypi/v/django-rest-durin)](https://pypi.org/project/django-rest-durin/)
[![Build Status](https://travis-ci.com/Eshaan7/django-rest-durin.svg?branch=main)](https://travis-ci.com/Eshaan7/django-rest-durin)
[![codecov](https://codecov.io/gh/Eshaan7/django-rest-durin/branch/main/graph/badge.svg?token=S9KEI0PU05)](https://codecov.io/gh/Eshaan7/django-rest-durin/)
[![CodeFactor](https://www.codefactor.io/repository/github/eshaan7/django-rest-durin/badge)](https://www.codefactor.io/repository/github/eshaan7/django-rest-durin)
<a href="https://lgtm.com/projects/g/Eshaan7/django-rest-durin/context:python">
  <img alt="Language grade: Python" src="https://img.shields.io/lgtm/grade/python/g/Eshaan7/django-rest-durin.svg?logo=lgtm&logoWidth=18"/>
</a>

Per API client token authentication Module for [Django REST Framework](http://www.django-rest-framework.org/).

The idea is to provide one library that does token auth for multiple Web/CLI/Mobile API clients via one interface but allows different token configuration for each client.

Durin authentication is token based, similar to the `TokenAuthentication`
built in to DRF. However, it adds some extra sauce:

- Durin allows multiple tokens per user. But only one token each user per API client.

- Each user token is associated with an API Client. These API Clients are configurable via Django's Admin Interface.

- All Durin tokens have an expiration time. This expiration time can be different per API client.

- Durin provides an option for a logged in user to remove *all*
    tokens that the server has - forcing him/her to re-authenticate for all API clients.

- Durin tokens can be renewed to get a fresh expiry.

- Durin provides a `CachedTokenAuthentication` backend as well which uses memoization for faster look ups.

More information can be found in the [Documentation](https://django-rest-durin.readthedocs.io/).

## Django Compatibility Matrix

If your project uses an older verison of Django or Django Rest Framework, you can choose an older version of this project.

| This Project | Python Version | Django Version | Django Rest Framework |
|--------------|----------------|----------------|-----------------------|
| 0.1.*        | 3.5 - 3.9      | 2.2, 3.0, 3.1  | 3.7>=                 |

Make sure to use at least `DRF 3.10` when using `Django 3.0` or newer.

## Changelog / Releases

All releases should be listed in the [releases tab on github](https://github.com/Eshaan7/django-rest-durin/releases).

See [CHANGELOG.md](CHANGELOG.md) for a more detailed listing.

## License

This project is published with the [MIT License](LICENSE). See [https://choosealicense.com/licenses/mit/](https://choosealicense.com/licenses/mit/) for more information about what this means.

## Credits

Durin is inpired by the [django-rest-knox](https://github.com/James1345/django-rest-knox) and [django-rest-multitokenauth](https://github.com/anexia-it/django-rest-multitokenauth) libraries and includes some learnings and code from both.