.. _flinkto:

#######
link_to
#######

:doc:`Navigation-related functions </Reference/packages/Function/View/Navigation/index>`

*******
Summary
*******

.. include:: /Reference/libraries/globals/summary/link_to.rst

.. php:function:: link_to(Omeka_Record_AbstractRecord|string $record, string $action, string $text, array $props, array $queryParams)

    Return a link tag.
    
    :param Omeka_Record_AbstractRecord|string $record: The name of the controller to use for the link.  If a record instance is passed, then it inflects the name of the controller from the record class.
    :param string $action: The action to use for the link
    :param string $text: The text to put in the link.  Default is 'View'.
    :param array $props: Attributes for the <a> tag
    :param array $queryParams: the parameters in the uri query
    :returns: string HTML

*****
Usage
*****

.. include:: /Reference/libraries/globals/usage/link_to.rst

********
Examples
********

.. include:: /Reference/libraries/globals/examples/link_to.rst

********
See Also
********

.. include:: /Reference/libraries/globals/see_also/link_to.rst

