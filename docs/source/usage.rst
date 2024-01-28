Usage
=====

.. _installation:

Installation
------------

To use ligacloud, first install it using pip:

.. code-block:: console

   (.venv) $ pip install ligacloud

Creating recipes
----------------

To retrieve a list of random ingredients,
you can use the ``ligacloud.get_random_ingredients()`` function:

.. autofunction:: ligacloud.get_random_ingredients

The ``kind`` parameter should be either ``"meat"``, ``"fish"``,
or ``"veggies"``. Otherwise, :py:func:`ligacloud.get_random_ingredients`
will raise an exception.

.. autoexception:: ligacloud.InvalidKindError

For example:

>>> import ligacloud
>>> ligacloud.get_random_ingredients()
['shells', 'gorgonzola', 'parsley']

