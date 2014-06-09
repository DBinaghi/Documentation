-----------------
Omeka_Job_Factory
-----------------

.. php:class:: Omeka_Job_Factory

    Package: :doc:`Job\\Factory </Reference/packages/Job/Factory/index>`

    Factory for instantiating Omeka_Job instances.

    .. php:attr:: _options
    


    .. php:method:: __construct($options)
    
        :param unknown $options:

    .. php:method:: from(string $json)
    
        Decode a message from JSON and use the results to instantiate a new job 
        instance.
        
        :param string $json:

    .. php:method:: build($data)
    
        Instantiate a new job instance from the arguments given.
        
        :param unknown $data: