.. image:: https://docs.pytest.org/en/latest/_static/pytest1.png
   :target: https://docs.pytest.org/en/latest/
   :align: center
   :alt: pytest


------

.. image:: https://img.shields.io/pypi/v/pytest.svg
    :target: https://pypi.org/project/pytest/

.. image:: https://img.shields.io/conda/vn/conda-forge/pytest.svg
    :target: https://anaconda.org/conda-forge/pytest

.. image:: https://img.shields.io/pypi/pyversions/pytest.svg
    :target: https://pypi.org/project/pytest/

.. image:: https://codecov.io/gh/pytest-dev/pytest/branch/master/graph/badge.svg
    :target: https://codecov.io/gh/pytest-dev/pytest
    :alt: Code coverage Status

.. image:: https://travis-ci.org/pytest-dev/pytest.svg?branch=master
    :target: https://travis-ci.org/pytest-dev/pytest

.. image:: https://dev.azure.com/pytest-dev/pytest/_apis/build/status/pytest-CI?branchName=master
    :target: https://dev.azure.com/pytest-dev/pytest

.. image:: https://img.shields.io/badge/code%20style-black-000000.svg
    :target: https://github.com/psf/black

.. image:: https://www.codetriage.com/pytest-dev/pytest/badges/users.svg
    :target: https://www.codetriage.com/pytest-dev/pytest

The ``pytest`` framework makes it easy to write small tests, yet
scales to support complex functional testing for applications and libraries.
（pytest框架使编写小型测试变得容易，但是可以扩展以支持应用程序和库的复杂功能测试。）

An example of a simple test:

.. code-block:: python

    # content of test_sample.py
    def inc(x):
        return x + 1


    def test_answer():
        assert inc(3) == 5


To execute it::

    $ pytest
    ============================= test session starts =============================
    collected 1 items

    test_sample.py F

    ================================== FAILURES ===================================
    _________________________________ test_answer _________________________________

        def test_answer():
    >       assert inc(3) == 5
    E       assert 4 == 5
    E        +  where 4 = inc(3)

    test_sample.py:5: AssertionError
    ========================== 1 failed in 0.04 seconds ===========================


Due to ``pytest``'s detailed assertion introspection, only plain ``assert`` statements are used. See `getting-started <https://docs.pytest.org/en/latest/getting-started.html#our-first-test-run>`_ for more examples.
（由于“pytest”的详细断言内省，只使用了简单的“assert”语句。请参见“入门<https://docs.pytest.org/en/latest/getting started.html”我们的第一次测试运行>``。）

Features（特征）
--------

- Detailed info on failing `assert statements <https://docs.pytest.org/en/latest/assert.html>`_ (no need to remember ``self.assert*`` names);
（关于失败的“assert语句”的详细信息（不需要记住“self.assert*”名称）；）

- `Auto-discovery
  <https://docs.pytest.org/en/latest/goodpractices.html#python-test-discovery>`_
  of test modules and functions;
  （自动发现<https://docs.pytest.org/en/latest/goodpractices.html“python测试发现”>`_测试模块和功能；）

- `Modular fixtures <https://docs.pytest.org/en/latest/fixture.html>`_ for
  managing small or parametrized long-lived test resources;
  （模块化夹具<https://docs.pytest.org/en/latest/fixture.html>``管理小型或参数化的长寿命测试资源；）

- Can run `unittest <https://docs.pytest.org/en/latest/unittest.html>`_ (or trial),
  `nose <https://docs.pytest.org/en/latest/nose.html>`_ test suites out of the box;
（可以运行“unittest<https://docs.pytest.org/en/latest/unittest.html>`（或trial），`nose<https://docs.pytest.org/en/latest/nose.html>``开箱即用的测试套件；）

- Python 3.5+ and PyPy3;

- Rich plugin architecture, with over 315+ `external plugins <http://plugincompat.herokuapp.com>`_ and thriving community;
（丰富的插件架构，拥有超过315个“外部插件”和欣欣向荣的社区；）

Documentation（文档）
-------------

For full documentation, including installation, tutorials and PDF documents, please see https://docs.pytest.org/en/latest/.
（有关完整的文档，包括安装、教程和PDF文档，请参见https://docs.pytest.org/en/latest/。）

Bugs/Requests（错误/请求）
-------------

Please use the `GitHub issue tracker <https://github.com/pytest-dev/pytest/issues>`_ to submit bugs or request features.
（请使用“GitHub issue tracker<https://GitHub.com/pytest dev/pytest/issues>``提交错误或请求功能。）

Changelog（变更日志）
---------

Consult the `Changelog <https://docs.pytest.org/en/latest/changelog.html>`__ page for fixes and enhancements of each version.
（请参阅“Changelog<https://docs.pytest.org/en/latest/Changelog.html>``页面，了解每个版本的修复和增强。）

Support pytest（支持pytest）
--------------

`Open Collective`_ is an online funding platform for open and transparent communities.
It provide tools to raise money and share your finances in full transparency.
（`“开放集体”是一个开放透明社区的在线融资平台。它提供了筹集资金和完全透明地分享财务的工具。）

It is the platform of choice for individuals and companies that want to make one-time or
monthly donations directly to the project.
（它是个人和公司选择的平台，希望一次性或每月直接向项目捐款。）

See more datails in the `pytest collective`_.

.. _Open Collective: https://opencollective.com
.. _pytest collective: https://opencollective.com/pytest


pytest for enterprise （企业版pytest）
---------------------

Available as part of the Tidelift Subscription.
（作为Tidelift订阅的一部分提供。）

The maintainers of pytest and thousands of other packages are working with Tidelift to deliver commercial support and
maintenance for the open source dependencies you use to build your applications.
Save time, reduce risk, and improve code health, while paying the maintainers of the exact dependencies you use.
（pytest和数千个其他软件包的维护人员正在与Tidelift合作，以提供商业支持和维护用于构建应用程序的开放源代码依赖项。
节省时间、降低风险和改善代码运行状况，同时向维护者支付使用的确切依赖项的费用。）

`Learn more. <https://tidelift.com/subscription/pkg/pypi-pytest?utm_source=pypi-pytest&utm_medium=referral&utm_campaign=enterprise&utm_term=repo>`_

Security （安全）
^^^^^^^^

pytest has never been associated with a security vunerability, but in any case, to report a
security vulnerability please use the `Tidelift security contact <https://tidelift.com/security>`_.
Tidelift will coordinate the fix and disclosure.
（pytest从未与安全漏洞关联，但无论如何，要报告安全漏洞请使用“Tidelift security contact<https://Tidelift.com/security>`”。
Tidelift将协调修复和披露。）

License （许可证）
-------

Copyright Holger Krekel and others, 2004-2019.
（版权所有Holger Krekel等人，2004-2019年。）

Distributed under the terms of the `MIT`_ license, pytest is free and open source software.
（pytest是根据“MIT”许可证的条款发布的，是免费的开源软件。）

.. _`MIT`: https://github.com/pytest-dev/pytest/blob/master/LICENSE
