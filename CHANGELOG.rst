=======
History
=======

11.2.0 (2023-05-10)
-------------------

* Upload_fileobj performance enhancements - thanks @JohnHBrock
* Contributing documentation updates - thanks @JohnHBrock

11.1.0 (2023-03-30)
-------------------

* Bumped aiobotocore to 2.5.0

11.0.1 (2023-03-06)
-------------------

* Fixed erroneous change to the minimum python version.

11.0.0 (2023-03-05)
-------------------

* Changed keyword arguments for S3Transfer config to match upstream.

10.4.0 (2023-01-31)
-------------------

* Bumped aiobotocore to 2.4.2
* Updated CI action versions

10.3.0 (2023-01-04)
-------------------

* Added support for async fileobjects in download_fileobj - thanks @prodeveloper0

10.2.0 (2022-12-03)
-------------------

* Updated S3 streaming example
* Bumped aiobotocore to 2.4.1

10.1.0 (2022-09-21)
-------------------

* Bumped aiobotocore to 2.4.0 - thanks @abivolmv

10.0.0 (2022-08-10)
-------------------

* Bumped aiobotocore to 2.3.4 - thanks @dacevedo12
* Fixed async pytest fixtures which now work in pytest-asyncio strict mode
* Fixed edge case in dynamodb batch writer loosing uncommitted writes - see #270, thanks @JamesVerrill

9.6.0 (2022-05-06)
------------------

* Bumped aiobotocore to 2.3.0

9.5.0 (2022-03-29)
------------------

* Bumped aiobotocore to 2.2.0 - thanks @dacevedo12
* Updated formatting in various places to match the boto3 equivalent

9.4.0 (2022-03-13)
------------------

* Bumped aiobotocore to 2.1.2
* Updated asyncio.wait usage to be compatible with py3.11 - thanks @noblepayne
* Fixed resource __aexit__ not being used properly - thanks @chrisBLIT
* Added S3 CopyFrom test coverage
* Bumped Moto to 3.1.0

9.3.1 (2022-01-10)
------------------

* Bumped aiobotocore to 2.1.0 - thanks @abivolmv

9.3.0 (2021-12-13)
------------------

* Bumped aiobotocore to 2.0.1 - thanks @mmaslowskicc

9.2.2 (2021-10-06)
------------------

* Fixed pyproject misconfiguration bringing in extra dependencies by default - thanks @and-semakin

9.2.1 (2021-10-05)
------------------

* Bumped aiobotocore to 1.4.2

9.2.0 (2021-07-22)
------------------

* Beta release promoted

9.2.0b0 (2021-07-19) Beta 0
---------------------------

* Experimental AWS Chalice added.

9.1.0 (2021-07-16)
------------------

* Switched to using Poetry for dependency management and setup.py replacement
* Bumped aiobotocore to 1.3.3 to fix some JSON parsing bugs on streams

9.0.0 (2021-06-27)
------------------

* Removed default session
* Bumped aiobotocore to 1.3.1 - thanks @slipovenko


8.3.0 (2021-03-24)
------------------

* Fixed S3.Bucket injected load method
* Updated CI

8.2.1 (2021-03-02)
------------------

* Better aiofiles support - thanks @frosthamster

8.2.0 (2020-12-02)
------------------

* Added file.read error handling in S3 upload_file/upload_fileobj

8.1.1 (2020-12-01)
------------------

* Fixed s3.ObjectSummary metadata properties loading

8.1.0 (2020-12-01)
------------------

* Bumped to use aiobotocore 1.1.2

8.0.5 (2020-07-08)
------------------

* @u-ashish Fixed a bug where ExtraArgs was ignored when doing s3.copy

8.0.4 (2020-07-07)
------------------

* @u-ashish Fixed a bug where ExtraArgs was ignored when doing s3.download_file/fileobj

8.0.3 (2020-04-25)
------------------

* Bumped aiobotocore version
* @compscidr Fixed a bug where upload_file callback returned the wrong amount of bytes

8.0.2 (2020-04-10)
------------------

* Bumped aiobotocore version

8.0.1 (2020-04-08)
------------------

* Bumped aiobotocore version
* Added aiohttp example

8.0.0 (2020-04-03)
------------------

* Major refactor to mirror boto3 file structure
* Updated to support aiobotocore 1.0.1, a few breaking changes.
* Switched to pipenv

7.1.0 (2020-03-31)
------------------

* Pinned aiobotocore version. Aiobotocore 1.0.0 requires changes.

7.0.0 (2020-03-12)
------------------

* Upgrade to aiobotocore 0.12
* Bumped minimum python version to 3.6, adding support for 3.8
* Eliminate use of deprecated loop arguments

6.5.0 (2020-02-20)
------------------

* @bact fixed some typos :)
* Asyncified the S3 resource Bucket().objects API and by extension, anything else in boto3 that uses the same object structure
* Bumped aiobotocore version so that eventstreams would now work

6.4.0 (2019-06-20)
------------------

* Updated ```upload_fileobj``` to upload multiple parts concurrently to make best use of the available bandwidth

6.2.0 (2019-05-07)
------------------

* @inadarei Added batch writing example
* Added waiter support in resources
* Made resource object properties coroutines and lazy load data when called

6.2.0 (2019-02-27)
------------------

* Added S3 Client side encryption functionality

6.1.0 (2019-02-13)
------------------

* nvllsvm cleaned up the packaging, requirements, travis, sphinx...
* Unvendored aiobotocore

6.0.1 (2018-11-22)
------------------

* Fixed dependencies

6.0.0 (2018-11-21)
------------------

* Fixed readthedocs
* Vendored aiobotocore for later botocore version

5.0.0 (2018-10-12)
------------------

* Updated lots of dependencies
* Changed s3.upload_fileobj from using put_object to doing a multipart upload
* Created s3.copy shim that runs get_object then does multipart upload, could do with a better implementation though.

4.1.2 (2018-08-28)
------------------

* updated pypi credentials

4.1.0 (2018-08-28)
------------------

* aiobotocore dependancy bump

4.0.2 (2018-08-03)
------------------

* Dependancy bump

4.0.0 (2018-05-09)
------------------

* Dependancy bump
* Now using aiobotocore 0.8.0
* Dropped < py3.5 support
* Now using async def / await syntax
* Fixed boto3 dependancy so it only uses a boto3 version supported by aiobotocore's max botocore dependancy
* Important, ```__call__``` in ```AIOServiceAction``` tries to yield from a coroutine in a non-coroutine, this code shouldn't be hit
  anymore but I can't guarantee that, so instead ```__call__``` was duplicated and awaited properly so "should" be fine.
  Credit goes to Arnulfo Solis for doing PR.

3.0.0 (2018-03-29)
------------------

* Dependancy bump
* Asyncified dynamodb Table Batch Writer + Tests
* Added batch writer examples
* Now using aiobotocore 0.6.0

2.2.0 (2018-01-24)
------------------

* Dependancy bump

2.1.0 (2018-01-23)
------------------

* Dependancy bump
* Fix bug where extras isn't packaged

2.0.0 (2017-12-30)
------------------

* Patched most s3transfer functions

1.1.2 (2017-11-29)
------------------

* Fixup of lingering GPL license texts

0.1.0 (2017-09-25)
------------------

* First release on PyPI.
