Usage
=====

.. _installation:

Installation
------------

To use Lumache, first install it using pip:

.. code-block:: console

   (.venv) $ pip install lumache

Creating recipes
----------------

To retrieve a list of random ingredients,
you can use the ``lumache.get_random_ingredients()`` function:

.. autofunction:: lumache.get_random_ingredients

The ``kind`` parameter should be either ``"meat"``, ``"fish"``,
or ``"veggies"``. Otherwise, :py:func:`lumache.get_random_ingredients`
will raise an exception.

.. autoexception:: lumache.InvalidKindError

For example:

>>> import lumache
>>> lumache.get_random_ingredients()
['shells', 'gorgonzola', 'parsley']


To retrieve a list of ingredients from a given kind,
you can use the ``lumache.get_ingredients_by_kind()`` function:

.. autofunction:: lumache.get_ingredients_by_kind

The ``kind`` parameter should be either ``"meat"``, ``"chese"``,
or ``"random"``. Otherwise, :py:func:`lumache.get_ingredients_by_kind`
will raise an exception.

.. autoexception:: lumache.InvalidKindError

For example:

>>> import lumache
>>> lumache.get_ingredients_by_kind("cheese")
["mozzarela", "cheddar"]
