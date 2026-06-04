# # ImportDocumentFromUrlModel

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Document name. | [optional]
**path** | **string** | Document location (folder path). | [optional]
**custom_fields** | **array<string,mixed>** | Document custom attributes. | [optional]
**type** | [**\Aurigma\AssetProcessor\Model\ImportDocumentType**](ImportDocumentType.md) | Document type. | [optional]
**format** | [**\Aurigma\AssetProcessor\Model\ImportDocumentFormatType**](ImportDocumentFormatType.md) | Document format. | [optional]
**source_url** | **string** | Document source file URL. | [optional]
**request_headers** | **array<string,string>** | Headers that will be used to download remote document by URL.  For example, &#x60;Authorization&#x60; header can be placed here to provide access to documents. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
