# ![LOGO](logo.png) Cloud Asset **flow**ground Connector

## Description

A generated **flow**ground connector for the Cloud Asset API (version v1beta1).

Generated from: https://api.apis.guru/v2/specs/googleapis.com/cloudasset/v1beta1/swagger.json<br/>
Generated at: 2019-05-23T12:13:04+03:00

## API Description

The cloud asset API manages the history and inventory of cloud resources.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Gets the latest state of a long-running operation.  Clients can use this<br/>
> method to poll the operation result at intervals as recommended by the API<br/>
> service.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - The name of the operation resource.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Batch gets the update history of assets that overlap a time window.<br/>
> For RESOURCE content, this API outputs history with asset in both<br/>
> non-delete or deleted status.<br/>
> For IAM_POLICY content, this API outputs history when the asset and its<br/>
> attached IAM POLICY both exist. This can create gaps in the output history.<br/>
> If a specified asset does not exist, this API returns an INVALID_ARGUMENT<br/>
> error.

*Tags:* `projects`

#### Input Parameters
* `assetNames` - _optional_ - A list of the full names of the assets. For example:
`//compute.googleapis.com/projects/my_project_123/zones/zone1/instances/instance1`.
See [Resource
Names](https://cloud.google.com/apis/design/resource_names#full_resource_name)
for more info.

The request becomes a no-op if the asset name list is empty, and the max
size of the asset name list is 100 in one request.
* `contentType` - _optional_ - Required. The content type.
    Possible values: CONTENT_TYPE_UNSPECIFIED, RESOURCE, IAM_POLICY.
* `parent` - _required_ - Required. The relative name of the root asset. It can only be an
organization number (such as "organizations/123"), a project ID (such as
"projects/my-project-id")", or a project number (such as "projects/12345").
* `readTimeWindow.endTime` - _optional_ - End time of the time window (inclusive).
Current timestamp if not specified.
* `readTimeWindow.startTime` - _optional_ - Start time of the time window (exclusive).
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Exports assets with time and resource types to a given Cloud Storage<br/>
> location. The output format is newline-delimited JSON.<br/>
> This API implements the google.longrunning.Operation API allowing you<br/>
> to keep track of the export.

*Tags:* `projects`

#### Input Parameters
* `parent` - _required_ - Required. The relative name of the root asset. This can only be an
organization number (such as "organizations/123"), a project ID (such as
"projects/my-project-id"), a project number (such as "projects/12345"), or
a folder number (such as "folders/123").
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

## License

**flow**ground :- Telekom iPaaS / googleapis-com-cloudasset-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
