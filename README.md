====================================
Python bindings for SpinRewriterPyt API
====================================

`Spin Rewriter <http://www.spinrewriter.com/bigcontentsearch>`_ is an online
service for spinning text (synonym substitution) that creates unique version(s)
of existing text. This package provides a way to easily interact with
`SpinRewriter API <http://www.spinrewriter.com/api>`_. Usage requires an
account, `get one here <http://www.spinrewriter.com/registration>`_.

* `Source code @ GitHub <https://github.com/s4birli/SpinRewriterPyt>`_
* `Releases @ PyPI <https://pypi.org/project/SpinRewritterPyt#downloads>`_


Install
=======

Install into your Python path using `pip` or `easy_install`::

    $ pip install SpinRewriterPyt
    $ easy_install SpinRewriterPyt


Usage
=====

After installing it, this is how you use it::

    Initialize SpinRewriterPyt.
    >>> text = u"This is the text we want to spin."
    >>> from SpinRewriterPyt import SpinRewriterPyt
    >>> rewriter = SpinRewriterPyt('username', 'api_key')

    Request processed spun text with spintax.
    >>> rewriter.text_with_spintax(text)
    u"{This is|This really is|That is|This can be} some text that we'd {like to
    |prefer to|want to|love to} spin."

    Request a unique variation of processed given text.
    >>> rewriter.unique_variation(text)
    u"This really is some text that we'd love to spin."