 .. Licensed to the Apache Software Foundation (ASF) under one
    or more contributor license agreements.  See the NOTICE file
    distributed with this work for additional information
    regarding copyright ownership.  The ASF licenses this file
    to you under the Apache License, Version 2.0 (the
    "License"); you may not use this file except in compliance
    with the License.  You may obtain a copy of the License at

 ..   http://www.apache.org/licenses/LICENSE-2.0

 .. Unless required by applicable law or agreed to in writing,
    software distributed under the License is distributed on an
    "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
    KIND, either express or implied.  See the License for the
    specific language governing permissions and limitations
    under the License.

``apache-airflow-providers-amazon``
===================================

Content
-------

.. toctree::
    :maxdepth: 1
    :caption: Guides

    Connection types <connections/aws>
    Operators <operators/index>
    Secrets backends <secrets-backends/index>
    Logging for Tasks <logging/index>

.. toctree::
    :maxdepth: 1
    :caption: References

    Python API <_api/airflow/providers/amazon/index>

.. toctree::
    :maxdepth: 1
    :caption: Resources

    Example DAGs <https://github.com/apache/airflow/tree/main/airflow/providers/amazon/aws/example_dags>
    PyPI Repository <https://pypi.org/project/apache-airflow-providers-amazon/>

.. THE REMINDER OF THE FILE IS AUTOMATICALLY GENERATED. IT WILL BE OVERWRITTEN AT RELEASE TIME!


.. toctree::
    :maxdepth: 1
    :caption: Commits

    Detailed list of commits <commits>


Package apache-airflow-providers-amazon
------------------------------------------------------

Amazon integration (including `Amazon Web Services (AWS) <https://aws.amazon.com/>`__).


Release: 2.0.0

Provider package
----------------

This is a provider package for ``amazon`` provider. All classes for this provider package
are in ``airflow.providers.amazon`` python package.

Installation
------------

You can install this package on top of an existing airflow 2.* installation via
``pip install apache-airflow-providers-amazon``

PIP requirements
----------------

==============  ====================
PIP package     Version required
==============  ====================
``boto3``       ``>=1.15.0,<1.18.0``
``watchtower``  ``~=0.7.3``
==============  ====================

Cross provider package dependencies
-----------------------------------

Those are dependencies that might be needed in order to use all the features of the package.
You need to install the specified provider packages in order to use them.

You can install such cross-provider dependencies when installing from PyPI. For example:

.. code-block:: bash

    pip install apache-airflow-providers-amazon[apache.hive]


==============================================================================================================  ===============
Dependent package                                                                                               Extra
==============================================================================================================  ===============
`apache-airflow-providers-apache-hive <https://airflow.apache.org/docs/apache-airflow-providers-apache-hive>`_  ``apache.hive``
`apache-airflow-providers-exasol <https://airflow.apache.org/docs/apache-airflow-providers-exasol>`_            ``exasol``
`apache-airflow-providers-ftp <https://airflow.apache.org/docs/apache-airflow-providers-ftp>`_                  ``ftp``
`apache-airflow-providers-google <https://airflow.apache.org/docs/apache-airflow-providers-google>`_            ``google``
`apache-airflow-providers-imap <https://airflow.apache.org/docs/apache-airflow-providers-imap>`_                ``imap``
`apache-airflow-providers-mongo <https://airflow.apache.org/docs/apache-airflow-providers-mongo>`_              ``mongo``
`apache-airflow-providers-mysql <https://airflow.apache.org/docs/apache-airflow-providers-mysql>`_              ``mysql``
`apache-airflow-providers-postgres <https://airflow.apache.org/docs/apache-airflow-providers-postgres>`_        ``postgres``
`apache-airflow-providers-ssh <https://airflow.apache.org/docs/apache-airflow-providers-ssh>`_                  ``ssh``
==============================================================================================================  ===============

Downloading official packages
-----------------------------

You can download officially released packages and verify their checksums and signatures from the
`Official Apache Download site <https://downloads.apache.org/airflow/providers/>`_

* `The apache-airflow-providers-amazon 2.0.0 sdist package <https://downloads.apache.org/airflow/providers/apache-airflow-providers-amazon-2.0.0.tar.gz>`_ (`asc <https://downloads.apache.org/airflow/providers/apache-airflow-providers-amazon-2.0.0.tar.gz.asc>`__, `sha512 <https://downloads.apache.org/airflow/providers/apache-airflow-providers-amazon-2.0.0.tar.gz.sha512>`__)
* `The apache-airflow-providers-amazon 2.0.0 wheel package <https://downloads.apache.org/airflow/providers/apache_airflow_providers_amazon-2.0.0-py3-none-any.whl>`_ (`asc <https://downloads.apache.org/airflow/providers/apache_airflow_providers_amazon-2.0.0-py3-none-any.whl.asc>`__, `sha512 <https://downloads.apache.org/airflow/providers/apache_airflow_providers_amazon-2.0.0-py3-none-any.whl.sha512>`__)

 .. Licensed to the Apache Software Foundation (ASF) under one
    or more contributor license agreements.  See the NOTICE file
    distributed with this work for additional information
    regarding copyright ownership.  The ASF licenses this file
    to you under the Apache License, Version 2.0 (the
    "License"); you may not use this file except in compliance
    with the License.  You may obtain a copy of the License at

 ..   http://www.apache.org/licenses/LICENSE-2.0

 .. Unless required by applicable law or agreed to in writing,
    software distributed under the License is distributed on an
    "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
    KIND, either express or implied.  See the License for the
    specific language governing permissions and limitations
    under the License.


Changelog
---------

2.0.0
.....

Breaking changes
~~~~~~~~~~~~~~~~

* ``Auto-apply apply_default decorator (#15667)``

Features
~~~~~~~~

* ``Add Connection Documentation for the Hive Provider (#15704)``
* ``CloudwatchTaskHandler reads timestamp from Cloudwatch events (#15173)``
* ``remove retry for now (#16150)``
* ``Remove the 'not-allow-trailing-slash' rule on S3_hook (#15609)``

Bug Fixes
~~~~~~~~~

* ``Fix S3 Select payload join (#16189)``
* ``Fix spacing in 'AwsBatchWaitersHook' docstring (#15839)``
* ``Fix spelling (#15699)``
* ``MongoToS3Operator failed when running with a single query (not aggregate pipeline) (#15680)``

.. Below changes are excluded from the changelog. Move them to
   appropriate section above if needed. Do not delete the lines(!):
   * ``Check synctatic correctness for code-snippets (#16005)``
   * ``Bump pyupgrade v2.13.0 to v2.18.1 (#15991)``
   * ``Rename example bucket names to use INVALID BUCKET NAME by default (#15651)``
   * ``Docs: Replace 'airflow' to 'apache-airflow' to install extra (#15628)``

1.4.0
.....

Features
~~~~~~~~

* ``S3Hook.load_file should accept Path object in addition to str (#15232)``
* ``Add Connection Documentation for Providers (#15499)``

Bug fixes
~~~~~~~~~

* ``Fix 'logging.exception' redundancy (#14823)``
* ``Fix AthenaSensor calling AthenaHook incorrectly (#15427)``
* ``Update Docstrings of Modules with Missing Params (#15391)``
* ``Add links to new modules for deprecated modules (#15316)``
* ``Fixes doc for SQSSensor (#15323)``

1.3.0
.....

Features
~~~~~~~~

* ``A bunch of template_fields_renderers additions (#15130)``
* ``Send region_name into parent class of AwsGlueJobHook (#14251)``
* ``Added retry to ECS Operator (#14263)``
* ``Make script_args templated in AwsGlueJobOperator (#14925)``
* ``Add FTPToS3Operator (#13707)``
* ``Implemented S3 Bucket Tagging (#14402)``
* ``S3DataSource is not required (#14220)``

Bug fixes
~~~~~~~~~

* ``AWS: Do not log info when SSM & SecretsManager secret not found (#15120)``
* ``Cache Hook when initializing 'CloudFormationCreateStackSensor' (#14638)``

1.2.0
.....

Features
~~~~~~~~

* ``Avoid using threads in S3 remote logging upload (#14414)``
* ``Allow AWS Operator RedshiftToS3Transfer To Run a Custom Query (#14177)``
* ``includes the STS token if STS credentials are used (#11227)``

1.1.0
.....

Features
~~~~~~~~

* ``Adding support to put extra arguments for Glue Job. (#14027)``
* ``Add aws ses email backend for use with EmailOperator. (#13986)``
* ``Add bucket_name to template fileds in S3 operators (#13973)``
* ``Add ExasolToS3Operator (#13847)``
* ``AWS Glue Crawler Integration (#13072)``
* ``Add acl_policy to S3CopyObjectOperator (#13773)``
* ``AllowDiskUse parameter and docs in MongotoS3Operator (#12033)``
* ``Add S3ToFTPOperator (#11747)``
* ``add xcom push for ECSOperator (#12096)``
* ``[AIRFLOW-3723] Add Gzip capability to mongo_to_S3 operator (#13187)``
* ``Add S3KeySizeSensor (#13049)``
* ``Add 'mongo_collection' to template_fields in MongoToS3Operator (#13361)``
* ``Allow Tags on AWS Batch Job Submission (#13396)``

Bug fixes
~~~~~~~~~

* ``Fix bug in GCSToS3Operator (#13718)``
* ``Fix S3KeysUnchangedSensor so that template_fields work (#13490)``


1.0.0
.....


Initial version of the provider.
