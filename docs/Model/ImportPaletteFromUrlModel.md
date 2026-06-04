# # ImportPaletteFromUrlModel

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Palette name. | [optional]
**path** | **string** | Palette location (folder path). | [optional]
**palette_type** | [**\Aurigma\AssetProcessor\Model\ImportPaletteType**](ImportPaletteType.md) | Palette import file format. | [optional]
**custom_fields** | **array<string,mixed>** | Palette custom attributes. | [optional]
**preview_settings** | [**\Aurigma\AssetProcessor\Model\ImportPaletteFromUrlModelPreviewSettings**](ImportPaletteFromUrlModelPreviewSettings.md) |  | [optional]
**source_url** | **string** | Palette source file URL. | [optional]
**request_headers** | **array<string,string>** | Headers that will be used to download remote palette by URL.  For example, &#x60;Authorization&#x60; header can be placed here to provide access to palettes. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
