------------
Builder_Item
------------

.. php:class:: Builder_Item

    Package: :doc:`Record\\Builder </Reference/packages/Record/Builder/index>`

    Build an item.

    .. php:const:: IS_PUBLIC
    


    .. php:attr:: _recordClass
    


    .. php:attr:: _settableProperties
    


    .. php:attr:: _elementTexts
    


    .. php:attr:: _fileMetadata
    


    .. php:method:: setElementTexts(array $elementTexts)
    
        Set the element texts for the item.
        
        :param array $elementTexts:

    .. php:method:: setFileMetadata(array $fileMetadata)
    
        Set the file metadata for the item.
        
        :param array $fileMetadata:

    .. php:method:: setRecordMetadata(array $metadata)
    
        Overrides setRecordMetadata() to allow setting the item type by name
        instead of ID.
        
        :param array $metadata: 
        :returns: void

    .. php:method:: _addElementTexts()
    
        Add element texts to a record.

    .. php:method:: _replaceElementTexts()
    
        Replace all the element texts for existing element texts.

    .. php:method:: _addTags()
    
        Add tags to an item (must exist in database).

    .. php:method:: addFiles(string|Omeka_File_Ingest_AbstractIngest $transferStrategy, string|array $files, $options)
    
        Add files to an item.
        
        <li>'Url|Filesystem' => string|array If a string is given, this representsthe source identifier of a single file (the URL representing the file, orthe absolute file path, respectively).  If an array is given, it assumesthat each entry in the array must be either an array or a string.  If itan array, there are several default keys that may be present:<ul><li>'source' => Any identifier that is appropriate to the transferstrategy in use.  For 'Url', this should be a valid URL.  For 'Filesystem',it must be an absolute path to the source file to be transferred.</li><li>'name' => OPTIONAL The filename to give to the transferredfile.  This can be any arbitrary filename and will be listed as theoriginal filename of the file.  This will also be used to generate thearchival filename for the file.  If none is given, this defaults to usingthe getOriginalFileName() method of the transfer adapter.</li><li>'metadata' => OPTIONAL This could contain any metadata that needs to beassociated with the file.  This should be indexed in the same fashionas for items.  See ActsAsElementText::addTextsByArray()</li></ul></li></ul>
        
        :param string|Omeka_File_Ingest_AbstractIngest $transferStrategy: This can either be one of the following strings denoting built-in transfer methods: 'Upload', 'Filesystem', 'Url' Or it could be an implemented Omeka_File_Ingest_AbstractIngest class.
        :param string|array $files: This can be a single string, an array of strings, or an array of arrays, depending on the parameters that are needed by the underlying strategy.  Expected parameters for the built in strategies are as follows:         
        
            .. raw:: html
        
               <ul>
                      <li>'Upload' => null|string If a string is given, it represents the 
                 POST parameter name containing the uploaded file(s).  If null is given,
                 all files in the POST will be ingested.</li>
        
        :param unknown $options: 
        :returns: array Set of File records ingested.  May be empty if no files were ingested.

    .. php:method:: _addIngestValidators(Omeka_File_Ingest_AbstractIngest $ingester)
    
        Add the default validators for ingested files.
        
        The default validators are whitelists for file extensions and MIME types,
        and those lists can be configured via the admin settings form.
        
        These default validators can be disabled by the 'disable_default_file_validation'
        flag in the settings panel.
        
        Plugins can add/remove/modify validators via the 'file_ingest_validators'filter.
        
        :param Omeka_File_Ingest_AbstractIngest $ingester: 
        :returns: void

    .. php:method:: _beforeBuild(Omeka_Record_AbstractRecord $record)
    
        :param Omeka_Record_AbstractRecord $record: